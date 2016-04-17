---
layout: post
title:  "A Short Introduction: What is Web Security?"
date:   2016-04-11 14:42:02 +0800
categories: jekyll update
---

In this post, I will be giving a short introduction of web security.

#### **The Web**
Before diving into web security, let's have a common understanding of the Web. 

**What is it**<br>
As defined by W3C's publishment - [Architecture of the World Wide Web, Volume One][w3c-publishment], "The World Wide Web (WWW, or simply Web) is an information space in which the items of interest, referred to as resources, are identified by global identifiers called Uniform Resource Identifiers (URI)". More specifically, the Web is an information-sharing model that is part of the Internet. This model is an system of interconnected networks that provides information and services to its users. 

The underlying IT infrastructure of the Web consists of: 

- Standardised Protocols 
- Document Formats 
- Software Components  

**Standardised Protocols and Data Formats**<br>
One common transport protocol used between client and server is the Hypertext Transfer Protocol (HTTP). The communication between the client and server follows a request/response paradigm. The client sends HTTP requests to the server and each request includes a method to be performed on a resource stored in the server. For instance, the client may use the GET method to retrieve information from the server. 

The request headers of the HTTP request sent by the client may look similar to this: 
{% highlight text %}
GET / HTTP/1.1
Host: www.comp.nus.edu.sg
Connection: keep-alive
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/49.0.2623.112 Safari/537.36
Accept-Encoding: gzip, deflate, sdch
Accept-Language: en-US,en;q=0.8,zh-CN;q=0.6,zh-TW;q=0.4
{% endhighlight %}

Upon receiving the request, the server sends the HTTP responses to the client. Each response may contain different elements that make up the web page requested by the client. Some data formats of the elements include HyperText Markup Language (HTML), Cascading Style Sheets (CSS), forms, images and frames.  

**Software Component**<br>

To support the communication between the client and server described above, the Web also consists of some software components. At the client side, we have a web browser performs various functions such as display the web page, manage sessions, perform access control and send HTTP requests. At the server side, we have a web server that receives the client requests. After which, it proceeds to extract input from the client data and constructs requests to the back-end server and return resources requested by the client. 

A image that summarizes the interactions of a simple architecture: 
![web-interaction]({{ site.url }}/assets/web-interation.PNG)

#### **Web Security** 

After establishing what is the Web, we can now explore the idea of Web Security. 

We can see from the brief introduction to the Web above that the Web is quite complex - it consists of various components that work together. Hence, one would think that Web Security is also a rather complex topic since the technology it is trying to secure is complicated.

The fact that the Web is made up of various components may allow for different attack surfaces. Hence, Web Security may include aspects from other fields of security. It includes aspects of network security as we can see from the introduction above, the client and server spends much of their time communicating with each other. Hence, it is of their interest that the communication channel (the network) is free of eavesdropping and reliable in the sense that the transmissions between them cannot be modified by an unauthorized entity.

The user may interact the web using a web browser. Hence, the web browser is a possible attack surface. An adversary can find vulnerabilities in the web browsers and exploit the vulnerability to obtain confidential information of an unsuspecting user. Hence, web security also includes aspects of software security. 

Furthermore, the Web is evolving everyday - new technologies emerge and old technologies become unpopular. Web applications are becoming more dynamic in the way they are reacting with user input and the way the applications can be composed. Hence, I believe that on top of knowing various techniques for securing web servers, web users, and their surrounding organizations, it is very important for a web security professional to keep up with the latest developments in web developments.

In conclusion, web security is a complex topic that can comprise of aspects from other fields such as network security and software security. 

[w3c-publishment]: https://www.w3.org/TR/webarch/ 



