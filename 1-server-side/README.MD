# Server-side website programming

The __Dynamic Websites – Server-side programming__ topic is a series of modules that show:

- how to create dynamic websites;
- websites that deliver customised information in response to HTTP requests.
- The modules provide a generic introduction to `server-side programming`, along with specific beginner-level guides on how to use the `Django` (Python) and `Express` (Node.js/JavaScript) web frameworks to create basic applications.

-----

Most major websites use some kind of server-side technology to dynamically display different data as required. For example, imagine how many products are available on Amazon, and imagine how many posts have been written on Facebook? Displaying all of these using completely different static pages would be completely inefficient, so instead such sites display static templates (built using
 [HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML),
 [CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS), and
 [JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript), and then dynamically update the data displayed inside those templates when needed, e.g. when you want to view a different product on Amazon.

In the modern world of web development, learning about server-side development is __highly recommended__.

-----

## Learning pathway

[Original Post](https://developer.mozilla.org/en-US/docs/Learn/Server-side)

Getting started with server-side programming is usually easier than with client-side development, because dynamic websites tend to perform a lot of very similar operations:

- __retrieving data__ from a `database` and displaying it in a page,
- __validating__ _user-entered_ `data` and __saving__ it in a database,
- __checking__ `user permissions` and __logging__ `users` in,
- etc.

and they are constructed using web frameworks that make these and other common `web server` operations `easy`.

A basic knowledge of programming concepts (or of a particular programming language) is useful, but not essential. Similarly, expertise in `client-side` coding is not required, but a basic knowledge will help you work better with the developers creating your `client-side` web front end.

You will need to understand __"how the web works"__. We recommend that you first read the following topics:

1. [What is a `web server`](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server)
2. [What `software` do I need to build a website?](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_software_do_I_need)
3. [How do you `upload files` to a `web server`?](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Upload_files_to_a_web_server)

With that basic understanding you'll be ready to work your way through the modules in this section.

-----

## Modules

This topic contains the following modules. You should start with the first module, then go on to one of the following modules, which show how to work with two very popular `server-side` languages using appropriate `web frameworks`.

1. [Server-side website programming first steps](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps)

    This module provides server-technology-agnostic information about __server-side website programming__, including:
    - answers to __fundamental__ questions about `server-side programming` —
        - "what it is",
        - "how it differs from client-side programming", and
        - "why it is so useful"
    - an overview of some of the more popular server-side `web frameworks` and guidance on _how to select_ the most suitable for your site.
    - Lastly we provide an __introductory__ section on `web server security`.

2. [Django Web Framework (Python)](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django)

    `Django` is an extremely popular and _fully featured_ server-side `web framework`, written in Python.

    The module explains:
    - why `Django` is such a good web server framework,
    - how to set up a `development environment` and
    - how to perform common tasks with it.

3. [Express Web Framework (Node.js/JavaScript)](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs)

    `Express` is a popular `web framework`, written in JavaScript and hosted within the node.js runtime environment.

    The module explains:
    - some of the __key benefits__ of this framework,
    - how to set up your development environment and
    - how to perform common `web development` and `deployment` tasks.

-----

## See also

1. [Node server without framework](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Node_server_without_framework)

    This article provides a simple static file server built with pure `Node.js`, for those of you not wanting to use a framework.