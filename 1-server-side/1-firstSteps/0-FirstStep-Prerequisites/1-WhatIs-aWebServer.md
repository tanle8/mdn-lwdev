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

    - a `web server` includes several parts that control how `web users` access hosted files, at minimum an _HTTP server_.
    - An `HTTP server` is __a piece of software__ that understands [`URLs`](https://developer.mozilla.org/en-US/docs/Glossary/URL) (web addresses) and [`HTTP`](https://developer.mozilla.org/en-US/docs/Glossary/HTTP) (the __protocol__ your browser uses to view webpages).
    - It can be accessed through the `domain names` (like _mozilla.org_) of websites it stores, and delivers their content to the `end-user's device`.

At the most basic level, whenever a `browser` needs a `file` which is hosted on a `web server`, the browser requests the file via `HTTP`. When the request reaches the correct web server (hardware), the __HTTP server__ (software) accepts request, finds the requested document (if it doesn't then a [404](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404) response is returned), and sends it back to the browser, also through HTTP.

![](https://mdn.mozillademos.org/files/8659/web-server.svg)

To publish a website, you need either a static or a dynamic web server.

A __static web server__, or stack, consists of a computer (hardware) with an `HTTP server` (__software__). We call it "static" because the server sends its hosted files "as-is" to your browser.

A __dynamic web server__ consists of a static web server plus extra software, most commonly an _application server_ and a _database_. We call it "dynamic" because the application server updates the `hosted files` before sending them to your browser via the HTTP server.

For example, to produce the final webpages you see in the browser, the application server might __fill__ an `HTML template` with contents from a `database`. Sites like MDN or Wikipedia have many thousands of webpages, but they aren't real HTML documents, only a few HTML templates and a giant database. This setup makes it _easier_ and _quicker_ to __maintain__ and __deliver__ the content.

-----

## Deeper dive

To fetch a webpage, as we already said, your `browser` __sends a request__ to the `web server`, which __proceeds to search__ for the `requested file` in its own `storage` space. On finding the file, the server:

- __reads__ it,
- __processes__ it as needed, and
- __sends__ it to the browser.

Let's look at those steps in more detail.

### Hosting files

A `web server` first has to store the `website's files`, namely all HTML documents and their related assets, including images, CSS stylesheets, JavaScript files, fonts, and videos.

Technically, you could host all those files on your own computer, but it's far more convenient to store them all on a dedicated `web server` that

- is always up and running
- is always connected to the Internet
- has the same IP address all the time (not all ISPs provide a fixed IP address for home lines)
- is maintained by a third-party provider

For all these reasons, finding a good `hosting provider` is a _key part_ of building your website. Dig through the various services companies offer and choose one that fits your needs and your budget (services range from free to thousands of dollars per month). You can find more details [in this article](https://developer.mozilla.org/en-US/Learn/How_much_does_it_cost#Hosting).

Once you set up a web hosting solution, you just have to [upload your files to your web server](https://developer.mozilla.org/en-US/docs/Learn/Upload_files_to_a_web_server).

### Communicating through HTTP

Second, a `web server` provides support for HTTP (__H__ypertext __T__ransfer __P__rotocol). As its name implies, HTTP specifies how to transfer `hypertext` (i.e., linked web documents) between two computers.

A `Protocol` is a __set of rules__ for communication between two computers. `HTTP` is a _textual_, _stateless_ protocol.

- __Textual__
    - All commands are plain-text and human readable.

- __Stateless__
    - Neither the server nor client remember previous communications. For example, replying on HTTP alone, a server cannot remember a password you typed or what step you're on in a transaction. You need an application server for tasks like that. (We'll cover that sort of technology in further articles)

HTTP provides clear rules for how a client and server communicate. We'll cover HTTP itself in a technical article later on. For now, just be aware of these things:

- __Only__ `clients` can make `HTTP requests`, and then only to `servers`. `Servers` can only respond to a client's __`HTTP request`__.
- When requesting a file via `HTTP`, clients must provide the `file's URL`.
- The `web server` must answer every `HTTP request`, at least with an `error message`.

On a `web server`, the __`HTTP server`__ is responsible for __processing__ and __answering__ _incoming_ `requests`.

1. On __`receiving a request`__, an `HTTP server` first checks whether the `requested URL` matches an `existing file`.
2. If so, the `web server` sends the `file content` back to the browser. If not, an `application server` __builds__ the necessary `file`.
3. If _neither_ process is possible, the web server returns an error message to the browser, most commonly "404 Not Found". (That error is so common that many web designers spend quite some time designing [404 error pages](http://www.404notfound.fr/).)

### Static vs. Dynamic content

Roughly speaking, a server can serve either `static` or `dynamic` content. "Static" means __"served as-is"__. `Static websites` are the _easiest_ to __set up__, so we suggest you make your first site a `static site`.

`"Dynamic"` means that the `server` __processes__ the content or even __generates__ it on the fly from a `database`. This solution provides more __flexibility__, but the technical stack becomes more difficult to handle, making it dramatically more complex to build the website.

Take for example the page you're reading right now. On the `web server` hosting it, there is an `application server` that takes article content from a `database`, formats it, puts it inside some `HTML templates`, and sends you the results. In this case, the `application server` is called [Kuma](https://developer.mozilla.org/en-US/docs/MDN/Kuma) and is built with Python (using the [Django](https://www.djangoproject.com/) framework). The Mozilla team built Kuma for the specific needs of MDN, but there are many similar applications built on many other technologies.

There are so many application servers that it's pretty hard to suggest a particular one. Some `application servers` cater to specific website categories like `blogs`, `wikis` or `e-shops`; others, called __`CMSs`__ (__C__ontent __m__anagement __s__ystems), are more generic. If you're building a dynamic website, take the time to choose a tool that fits your needs. __Unless you want to learn some `web server` programming (which is an exciting area in itself!), you don't need to create your own `application server`. That's just [reinventing the wheel]__(https://en.wikipedia.org/wiki/reinventing%20the%20wheel).

-----

## Next steps

Now that you are familiar with web servers, you could:

- read up on [how much it costs to do something on the web](https://developer.mozilla.org/en-US/docs/Learn/How_much_does_it_cost)
- learn more about [various software you need to create a website](https://developer.mozilla.org/en-US/docs/Learn/What_software_do_I_need)
- move on to something practical like [how to upload files on a web server](https://developer.mozilla.org/en-US/docs/Learn/Upload_files_to_a_web_server).
