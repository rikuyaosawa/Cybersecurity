# HTTP in Detail

Table of Contents

- [HTTP in Detail](#http-in-detail)
  - [Overview](#overview)
  - [Request and Responses](#request-and-responses)
  - [HTTP Methods](#http-methods)
  - [Headers](#headers)
  - [Cookies](#cookies)

## Overview

**What is HTTP? (HyperText Transfer Protocol)**

HTTP is what's used whenever you view a website, developed by Tim Berners-Lee and his team between 1989-1991. HTTP is the set of rules used for communicating with web servers for the transmitting of webpage data, whether that is HTML, Images, Videos, etc.

**What is HTTPS? (HyperText Transfer Protocol Secure)**

HTTPS is the secure version of HTTP. HTTPS data is encrypted so it not only stops people from seeing the data you are receiving and sending, but it also gives you assurances that you're talking to the correct web server and not something impersonating it.

## Request and Responses

**What is a URL? (Uniform Resource Locator)**

If you’ve used the internet, you’ve used a URL before. A URL is predominantly an instruction on how to access a resource on the internet. The below image shows what a URL looks like with all of its features (it does not use all features in every request).

- Scheme: This instructs on what protocol to use for accessing the resource such as HTTP, HTTPS, FTP (File Transfer Protocol).

- User: Some services require authentication to log in, you can put a username and password into the URL to log in.

- Host: The domain name or IP address of the server you wish to access.

- Port: The Port that you are going to connect to, usually 80 for HTTP and 443 for HTTPS, but this can be hosted on any port between 1 - 65535.

- Path: The file name or location of the resource you are trying to access.

- Query String: Extra bits of information that can be sent to the requested path. For example, /blog?id=1 would tell the blog path that you wish to receive the blog article with the id of 1.

- Fragment: This is a reference to a location on the actual page requested. This is commonly used for pages with long content and can have a certain part of the page directly linked to it, so it is viewable to the user as soon as they access the page.

## HTTP Methods

HTTP methods are a way for the client to show their intended action when making an HTTP request. There are a lot of HTTP methods but we'll cover the most common ones, although mostly you'll deal with the GET and POST method.

- **GET** Request: This is used for getting information from a web server.
- **POST** Request: This is used for submitting data to the web server and potentially creating new records
- **PUT** Request: This is used for submitting data to a web server to update information
- **DELETE** Request: This is used for deleting information/records from a web server.

## Headers

Common Request Headers

These are headers that are sent from the client (usually your browser) to the server.

- **Host**: Some web servers host multiple websites so by providing the host headers you can tell it which one you require, otherwise you'll just receive the default website for the server.

- **User-Agent**: This is your browser software and version number, telling the web server your browser software helps it format the website properly for your browser and also some elements of HTML, JavaScript and CSS are only available in certain browsers.

- **Content-Length**: When sending data to a web server such as in a form, the content length tells the web server how much data to expect in the web request. This way the server can ensure it isn't missing any data.

- **Accept-Encoding**: Tells the web server what types of compression methods the browser supports so the data can be made smaller for transmitting over the internet.

- **Cookie**: Data sent to the server to help remember your information (see cookies task for more information).

Common Response Headers

These are the headers that are returned to the client from the server after a request.

- **Set-Cookie**: Information to store which gets sent back to the web server on each request (see cookies task for more information).

- **Cache-Control**: How long to store the content of the response in the browser's cache before it requests it again.

- **Content-Type**: This tells the client what type of data is being returned, i.e., HTML, CSS, JavaScript, Images, PDF, Video, etc. Using the content-type header the browser then knows how to process the data.

- **Content-Encoding**: What method has been used to compress the data to make it smaller when sending it over the internet.

## Cookies

You've probably heard of cookies before, they're just a small piece of data that is stored on your computer. Cookies are saved when you receive a "Set-Cookie" header from a web server. Then every further request you make, you'll send the cookie data back to the web server. Because HTTP is stateless (doesn't keep track of your previous requests), cookies can be used to remind the web server who you are, some personal settings for the website or whether you've been to the website before. Let's take a look at this as an example HTTP request:

<img src="https://tryhackme-images.s3.amazonaws.com/user-uploads/5c549500924ec576f953d9fc/room-content/a2117dc267fbb169e38be77c7af44027.png" alt="cookies"/>

Cookies can be used for many purposes but are most commonly used for website authentication. The cookie value won't usually be a clear-text string where you can see the password, but a token (unique secret code that isn't easily humanly guessable).
