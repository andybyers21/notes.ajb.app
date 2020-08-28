---
layout: note
title: What happens when you search for content on the web?
parent: Web Infrastructure
nav_exclude: true
---

# What happens when you search for content on the web?
A query string may be added to your request (it will follow a question mark at the end of the path, e.g. /?q=something that I'm searching for). The server receives this request and uses the data in the query string. When the server has calculated the search results it will bundle it up into HTML and return it to you. 

> Many of the things you’ve seen in the request/response cycle are not actually the responsibility of a programmer writing web code. The network layer – the requests to DNS, the HTTPS messages being sent over the internet – is handled by your computer’s operating system and the infrastructure of the internet itself. A web developer just has to place HTML code on a web server somewhere on the internet.