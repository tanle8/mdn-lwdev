# What is the difference between webpage, website, web server, and search engine?

[Original post](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Pages_sites_servers_and_search_engines)

In this article we describe various web-related concepts: `web pages`, `websites`, `web servers`, and `search engines`. These terms are often confused by newcomers to the web, or are incorrectly used. Let's learn what they each mean!

- Prerequisites: You should know [how the Internet works](https://developer.mozilla.org/en-US/Learn/How_the_Internet_works).
- Objective: Be able to describe the differences between a web page, a website, a web server, and a search engine.

## Summary

As with any area of knowledge, the web comes with a lot of jargon. Don't worry, we won't overwhelm you with all of it (we have a [glossary](https://developer.mozilla.org/en-US/docs/Glossary) if you're curious). However, there are a few basic terms you need to understand at the outset, since you'll hear these expressions all the time as you read on. It's easy to confuse these terms sometimes, since they refer to related but different functionalities. In fact, you'll sometimes see these terms misused in news reports and elsewhere, so getting them mixed up is understandable!

We'll cover these terms and technologies in more detail as we explore further, but these quick definitions will be a great start for you:

__web page__

A __document__ which can be displayed in a web browser such as _Firefox_, _Google Chrome_, _Opera_, _Microsoft Internet Explorer_ or _Edge_, or _Apple's Safari_. These are also often called just "pages."

__website__

A __collection of web pages__ which are grouped together and usually connected together in various ways. Often called a "web site" or simply a "site."

__web server__

A computer that hosts a website on the Internet.

__search engine__

A website that helps you __find other web pages__, such as _Google_, _Bing_, or _Yahoo_.

Let's look at a simple analogy — a public library. This is what you would generally do when visiting a library:

1. Find a search index and look for the title of the book you want.
2. Make a note of the catalog number of the book.
3. Go to the particular section containing the book, find the right catalog number, and get the book.

Let's compare the library with a web server:

The library is like a `web server`. It has several sections, which is similar to a web server hosting multiple websites.
The different sections (science, math, history, etc.) in the library are like `websites`. Each section is like a unique website (two sections do not contain same books).
The books in the sections are like webpages. One website may have several webpages, e.g., the Science section (the website) will have books on heat, sound, thermodynamics, statics, etc. (the webpages).
The search index is like the `search engine`. Each book has its own unique location in the library (two books cannot be kept at the same place) which is specified by the catalog number.
Similarly, webpages also have __unique addresses__. These unique addresses are used to retrieve a webpage from a web server by typing the address in the address bar of a web browser (Mozilla Firefox, Safari, Google chrome, etc).

## Deeper dive

So, let's dig deeper into how those four terms are related and why they are sometimes confused with each other.

### web page

A `web page` is a simple __document__ displayable by a browser. Such document is written in the HTML language (which we look into in more detail in [other articles](https://developer.mozilla.org/en-US/docs/Web/HTML)). A web page can embed a variety of different types of resources such as:

- style information — controlling a page's look-and-feel
- scripts — which add interactivity to the page
- media — images, sounds, and videos.

__Note__: Browsers can also display other documents such as `PDF` files or `images`, but the term `web page` specifically refers to HTML documents. Otherwise we only use the term `document`.

All web pages available on the web are reachable through a unique address. To access a page, just type its address in your browser address bar:

[Example of a web page address in the browser address bar](https://mdn.mozillademos.org/files/8529/web-page.jpg)

A `website` is a collection of _linked_ `web pages` (plus their associated resources) that share a unique domain name. Each web page of a given website provides explicit links — most of the time in the form of clickable portion of text—that allow the user to move from one page of the website to another.

To access a website, type its domain name in your browser address bar, and the browser will display the website's main web page, or _homepage_ (casually referred as "the home"):

![Example of a web site domain name in the browser address bar](https://mdn.mozillademos.org/files/8531/web-site.jpg)

The ideas of a `web page` and a `website` are especially easy to confuse for a website that contains only one `web page`. Such a website is sometimes called a `single-page website`.

### Web server

A _web server_ is a computer hosting one or more websites. "Hosting" means that all the web pages and their supporting files are available on that computer. The web server will send any web page from the website it is hosting to any user's browser, per user request.

Don't confuse websites and web servers. For example, if you hear someone say, "My website is not responding", it actually means that the web server is not responding and therefore the website is not available. More importantly, since a web server can host multiple websites, the term web server is never used to designate a website, as it could cause great confusion. In our previous example, if we said, "My web server is not responding", it means that no websites on that web server are available.

### Search engine

Search engines are a common source of confusion on the web. A search engine is a special kind of website that helps users find `web pages` from _other websites_.

There are plenty out there: Google, Bing, Yandex, DuckDuckGo, and many more. Some are generic, some are specialized about certain topics. Use whichever you prefer.

Many beginners on the web confuse search engines and browsers. Let's make it clear:

- A __browser__ is a piece of software that retrieves and displays web pages;
- a __search engine__ is a website that helps people find web pages from other websites.

The confusion arises because, the first time someone launches a browser, the browser displays a search engine's homepage. This makes sense, because, obviously, the first thing you want to do with a browser is to find a web page to display. Don't confuse the `infrastructure` (e.g., the browser) with the `service` (e.g., the search engine). The distinction will help you quite a bit, but even some professionals speak loosely, so don't feel anxious about it.

Here is an instance of Firefox showing a Google search box as its default startup page:

![Example of Firefox nightly displaying a custom Google page as default](https://mdn.mozillademos.org/files/8533/search-engine.jpg)

## Next steps

Dig deeper: [What is a web server](https://developer.mozilla.org/en-US/docs/Learn/What_is_a_web_server)
See how web pages are linked into a web site: [Understanding links on the web](https://developer.mozilla.org/en-US/docs/Learn/Understanding_links_on_the_web)