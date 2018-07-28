# What is a web server

In this article we go over:

- what web servers are,
- how they work, and
- why they're important

-----

## Prerequisites

You should already know:

1. [how the Internet works](https://developer.mozilla.org/en-US/docs/Learn/How_the_Internet_works), and
2. [understand the difference between a `web page`, a `web site`, a `web server` and a `search engine`](https://developer.mozilla.org/en-US/docs/Learn/page_vs_site_vs_server_vs_search_engine).

## Objective

1. You will learn what a `web server` is and
2. Gain a general understanding of how it works.

-----

## Summary

`"Web server"` can refer to hardware or software, or both of them working together.

1. On the __hardware side__,

    - a `web server` is __a computer__ that stores `web server software` and a `website's component files` (e.g. HTML documents, images, CSS stylesheets, and JavaScript files).
    - It is connected to the Internet and supports physical data interchange with other devices connected to the web.

2. On the __software side__,

    - a `web server` includes several parts that control how `web users` access hosted files, at minimum an HTTP server.
    - An `HTTP server` is __a piece of software__ that understands [`URLs`](https://developer.mozilla.org/en-US/docs/Glossary/URL) (web addresses) and [`HTTP`](https://developer.mozilla.org/en-US/docs/Glossary/HTTP) (the __protocol__ your browser uses to view webpages).
    - It can be accessed through the `domain names` (like _mozilla.org_) of websites it stores, and delivers their content to the `end-user's device`.

At the most basic level, whenever a `browser` needs a `file` which is hosted on a `web server`, the browser requests the file via `HTTP`. When the request reaches the correct web server (hardware), the __HTTP server__ (software) accepts request, finds the requested document (if it doesn't then a [404](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404) response is returned), and sends it back to the browser, also through HTTP.

![](https://mdn.mozillademos.org/files/8659/web-server.svg)

To publish a website, you need either a static or a dynamic web server.

A __static web server__, or stack, consists of a computer (hardware) with an HTTP server (software). We call it "static" because the server sends its hosted files "as-is" to your browser.

A __dynamic web server__ consists of a static web server plus extra software, most commonly an _application server_ and a _database_. We call it "dynamic" because the application server updates the hosted files before sending them to your browser via the HTTP server.

For example, to produce the final webpages you see in the browser, the application server might fill an HTML template with contents from a database. Sites like MDN or Wikipedia have many thousands of webpages, but they aren't real HTML documents, only a few HTML templates and a giant database. This setup makes it easier and quicker to maintain and deliver the content.

-----

## Deeper dive

To fetch a webpage, as we already said, your browser sends a request to the `web server`, which proceeds to search for the requested file in its own storage space. On finding the file, the server __reads__ it, __processes__ it as needed, and __sends__ it to the browser. Let's look at those steps in more detail.

### Hosting files

A `web server` first has to store the `website's files`, namely all HTML documents and their related assets, including images, CSS stylesheets, JavaScript files, fonts, and videos.

Technically, you could host all those files on your own computer, but it's far more convenient to store them all on a dedicated web server that

- is always up and running
- is always connected to the Internet
- has the same IP address all the time (not all ISPs provide a fixed IP address for home lines)
- is maintained by a third-party provider

For all these reasons, finding a good hosting provider is a key part of building your website. Dig through the various services companies offer and choose one that fits your needs and your budget (services range from free to thousands of dollars per month). You can find more details [in this article](https://developer.mozilla.org/en-US/Learn/How_much_does_it_cost#Hosting).

Once you set up a web hosting solution, you just have to [upload your files to your web server](https://developer.mozilla.org/en-US/docs/Learn/Upload_files_to_a_web_server).

### Communicating through HTTP

### Static vs. dynamic content

-----

## Next steps

Now that you are familiar with web servers, you could:

- read up on [how much it costs to do something on the web](https://developer.mozilla.org/en-US/docs/Learn/How_much_does_it_cost)
- learn more about [various software you need to create a website](https://developer.mozilla.org/en-US/docs/Learn/What_software_do_I_need)
- move on to something practical like [how to upload files on a web server](https://developer.mozilla.org/en-US/docs/Learn/Upload_files_to_a_web_server).
