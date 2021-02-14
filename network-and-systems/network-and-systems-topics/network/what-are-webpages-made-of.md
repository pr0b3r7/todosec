# What are webpages made of?

**Loading some content**

Once the browser [knows the server's IP address](domain-name-system-wip.md), it can ask the server for the web page. This is done with a HTTP GET request. GET is an example of a HTTP verb, which are the different types of request \(More on these later\). The server will respond to the GET request with the web page content. If the web page is loading extra resources, like JavaScript, images, or CSS files, those will be retrieved in separate GET requests.![](https://i.imgur.com/R04qcso.png)

Wireshark showing the HTTP requests that load a website \(neverssl.com\)

For most websites now, these requests will use HTTPS. HTTPS is a secure \(encrypted\) version of HTTP, it works in more or less the same way. This uses TLS 1.3 \(normally\) encryption in order to communicate without:

* Other parties being able to read the data
* Other parties being able to modify the data

Imagine if someone could modify a request to your bank to send money to your friend. That'd be disastrous! Also, that communication would lack **confidentiality** and **integrity**. 

A web server is software that receives and responds to HTTP\(S\) requests. Popular examples are Apache, Nginx and Microsoft's IIS. 

By default, HTTP runs on port 80 and HTTPS runs on port 443. 

Many CTFs are based around websites, so it's useful to know that if port 80 is open, there's likely a web server listening that you can attack and exploit.

The actual content of the web page is normally a combination of **HTML**, **CSS** and **JavaScript**. 

HTML defines the structure of the page, and the content. 

CSS allows you to change how the page looks and make it look fancy. 

JavaScript is a programming language that runs in the browser and allows you to make pages interactive or load extra content.

