# What are Hyperlinks?

[Original Post](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_are_hyperlinks)

In this article, we'll go over what hyperlinks are and why they matter.

- Prerequisites: You should know:
    - [how the Internet works](https://developer.mozilla.org/en-US/Learn/How_the_Internet_works) and be familiar with
    - [the difference between a webpage, a website, a web server, and a search engine](https://developer.mozilla.org/en-US/docs/Learn/page_vs_site_vs_server_vs_search_engine).
- Objective: Learn about links on the web and why they matter.

## Summary

Hyperlinks, usually called links, are a foundational concept behind the Web. To explain what links are, we need to step back to the very basics of Web architecture.

Back in 1989, Tim Berners-Lee, the Web's inventor, spoke of the three pillars on which the Web stands:

1. URL, an `address system` that keeps track of Web documents
2. HTTP, a `transfer protocol` to find documents when given their `URLs`
3. HTML, a `document format` allowing for embedded _`hyperlinks`_

As you can see in the `three_ pillars`, everything on the Web revolves around `documents` and how to __access__ them. The `Web's original purpose` was to provide an easy way to __reach__, __read__, and __navigate__ through `text documents`.

Since then, the Web has evolved to provide __access__ to `images`, `videos`, and `binary data`, but these improvements have hardly changed the `three pillars`.

Before the Web, it was quite hard to access documents and move from one to another. Being _human-readable_, `URLs` already made things easier, but it's hard to type a long URL whenever you want to access a document. This is where `hyperlinks` revolutionized everything. `Links` can correlate any `text string` with a `URL`, such that the user can instantly reach the target document by activating the link.

`Links` stand out from the surrounding text by being _underlined_ and in _blue text_. Tap or click a link to activate it, or if you use a keyboard, press Tab until the link is in focus and hit Enter or Spacebar.

![Example of a basic display and effect of a link in a web page](https://mdn.mozillademos.org/files/8625/link-1.png)

Links are the breakthrough that made the Web so useful and successful. In the rest of this article, we discuss the various types of links and their importance to modern Web design.

## Deeper dive  

As we said, __a link is a text string tied to a URL__, and we use links to allow easy jumping from one `document` to `another`. That said, there are some nuances worth considering:

### Types of links

- __Internal link__:
    A link between two webpages, where both webpages belong to your website, is called an `internal link`. Without internal links, there's no such thing as a website (unless, of course, it's a one-page website).

- __External link__:
    A link from your webpage to someone else's webpage. Without external links, there is no `Web`, since the Web is a network of webpages. Use external links to provide information besides the content available through your webpage.

- __Incoming links__:
    A link from someone else's webpage to your site. It's the opposite of an external link. Note that you don't have to link back when someone links to your site.

When you're building a website, focus on `internal links`, since those make your site usable. Find a good balance between having too many links and too few. We'll talk about designing website navigation in another article, but as a rule, whenever you add a new webpage, make sure at least one of your other pages links to that new page. On the other hand, if your site has more than about ten pages, it's _counter-productive_ to link to every page from every other page.

When you're starting out, you don't have to worry about `external` and `incoming links` as much, but they are very important if you want `search engines` to find your site. (See below for more details.)

### Anchors

Most _links tie two webpages together_. __Anchors tie two sections of one document together__. When you follow a link pointing to an anchor, your browser jumps to another part of the current document instead of loading a new document. However, you make and use anchors the same way as other links.

[Example of a basic display and effect of an anchor in a web page](https://mdn.mozillademos.org/files/8627/link-2.png)

### Links and Search Engines

`Links` matter both to your users and to `search engines`. Every time `search engines` __crawl a webpage__, they index the website by following the links _available on the webpage_. Search engines not only follow links to discover the various pages of the website, but they also use the link's visible text to determine which search queries are appropriate for reaching the target webpage.

Links influence how __readily__ a `search engine` will link to your site. The trouble is, it's hard to measure search engines' activities. Companies naturally want their sites to rank highly in search results.  We know the following about how search engines determine a site's rank:

- A link's visible text influences which search queries will find a given URL.
- The more `incoming links` a webpage can boast of, the higher it ranks in search results.
- `External links` influence the search ranking both of source and target webpages, but it is unclear by how much.
- [`SEO`](http://en.wikipedia.org/wiki/Search_engine_optimization) (search engine optimization) is the study of how to make websites rank highly in `search results`. Improving a website's use of links is one helpful SEO technique.

## Next steps

Now you'll want to set up some webpages with links.

To get some more theoretical background, learn about [URLs and their structure](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_URL), since every link points to a URL.
Want something a bit more practical? The [Creating hyperlinks](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks) article of our [Introduction to HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML) module explains how to implement links in detail.
