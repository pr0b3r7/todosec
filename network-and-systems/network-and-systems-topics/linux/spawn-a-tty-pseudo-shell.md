# Spawn a TTY/Pseudo Shell

A terminal is a physical device with a keyboard and screen connected to a computer running various OS types. 

A _**tty**_ is the UNIX device name for a physical/virtual terminal. 

A _**shell**_ is the Unix command interpreter. 

A _**console**_ is a generic term for a primary i/o device or interface. In **UNIX, console** is where the boot/startup messages are sent to. After bootup the console effectively becomes a _**terminal**_.

```erlang
//===========================\\
||          Terminal         ||
||             |-----------| ||
|| Keyboard--->|   Input   |-++->|---|   |-------|
||             |-----------| ||  |tty|<=>| shell |       
||         |---------|<------++--|---|   |-------|
|| Print<--|  Output |       ||
||         |---------|       ||
||                           ||
\\===========================//
```

When you SSH into the machine the SSH program is acting as the terminal, connecting with yet another tty:

```erlang
//===========================\\
||            SSH            ||
||              |----------| ||
|| STDIN------->|  Network |-++->|---|   |-------|
||              |----------| ||  |tty|<=>| shell |       
||          |---------|<-----++--|---|   |-------|
|| STDOUT<--| Network |      ||
||          |---------|      ||
||                           ||
\\===========================//
```

When you open a terminal on linux a lot of the time you are opening a graphic program which comes with the environment you are. For gnome this would be gnome-terminal:

```erlang
//===========================\\
||      gnome-terminal       ||
||              |----------| ||
|| GDK_p------->| File Wrt |-++->|---|   |-------|
||              |----------| ||  |tty|<=>| shell |       
||          |---------|<-----++--|---|   |-------|
|| Screen <-| File Rd |      ||
||          |---------|      ||
||                           ||
\\===========================//
```

[More](https://unix.stackexchange.com/questions/4126/what-is-the-exact-difference-between-a-terminal-a-shell-a-tty-and-a-con), [Source](https://www.reddit.com/r/programming/comments/41u5hw/what_is_the_exact_difference_between_a_terminal_a/)

