# What is a domain name?

In this article we discuss domain names:

- what they are,
- how they are structured, and
- how to get one.

- Prerequisites: First you need to know
    - [how the Internet works](https://developer.mozilla.org/en-US/docs/Learn/How_the_Internet_works) and
    - understand [what URLs are](https://developer.mozilla.org/en-US/Learn/Understanding_URLs).

- Objective:
    - Learn what domain names are,
    - how they work, and
    - why they are important.

## Summary

Domain names are a key part of the Internet infrastructure. __They provide a human-readable address for any web server available on the Internet__.

Any _Internet-connected_ computer can be reached through a _public_ `IP Address`,

- which consists of 32 bits for `IPv4` (they are usually written as four numbers between 0 and 255, separated by dots (e.g., `173.194.121.32`) or
- which consists of 128 bits for IPv6 (they are usually written as eight groups of 4 `hexadecimal numbers`, separated by colons (e.g., `2027:0da8:8b73:0000:0000:8a2e:0370:1337`).

Computers can handle those addresses easily, but people have a hard time finding out who's running the `server` or what `service` the website offers. IP addresses are hard to remember and might change over time. To solve all those problems we use `human-readable addresses` called domain names.

## Deeper dive

### Structure of domain names

A `domain name` has a simple structure made of several parts (it might be one part only, two, three...), separated by dots and read from __right to left__:

[Anatomy of the MDN domain name](https://mdn.mozillademos.org/files/11229/structure.png)

Each of those  parts provides specific information about the whole domain name.

1. __TLD (Top-Level Domain).__

    The `TLD` provides the most generic information. TLDs tell users the general purpose of the service behind the domain name.
        - The most generic TLDs (`.com`, `.org`, `.net`) don't require web services to meet strict criteria, but some TLDs enforce stricter policies. For example, local TLDs such as `.us`, `.fr`, or `.sh` can require the service to be __provided__ in a _given language_ or __hosted__ in a _certain country_.

2. __Label (or component)__

    The `labels` are what follow the `TLD`.
        -A label can be anything, from one letter to a full sentence.
        - The label located right before the `TLD` can also be referred as a __S__econdary __L__evel __D__omain (`SLD`).
        - A domain name can have many `labels` (or `components`), it is not mandatory nor necessary to have 3 labels to form a domain name. For instance, `www.inf.ed.ac.uk` is a correct domain name.
        - When controlling the "upper" part of a domain name (e.g. [mozilla.org](https://mozilla.org/)), one can create other domain names (sometimes called `subdomains`) (e.g. [developer.mozilla.org](https://developer.mozilla.org/)).

### Buying a domain name

1. Who owns a domain name?

    - __You cannot _"buy a domain name"_.__
        - _You pay for the right to use a domain name for one or more years_.
        - You can renew your right, and your renewal has priority over other people's applications. But you never own the domain name.

    - Companies called registrars use domain name registries to keep track of technical and administrative information connecting you to your domain name.

    __Note__: For some domain name, it might not be a registrar which is in charge of keeping track. For instance, every domain name under `.fire` is managed by __Amazon__.

2. Finding an available domain name

    To find out whether a given domain name is available,

    - Go to a domain name `registrar's website`. Most of them provide a “whois” service that tells you whether a domain name is available.
    - Alternatively, if you use a system with a built-in shell, type a `whois` command into it, as shown here for `mozilla.org`:

    ```bash
    $ whois mozilla.org
    Domain Name:MOZILLA.ORG
    Domain ID: D1409563-LROR
    Creation Date: 1998-01-24T05:00:00Z
    Updated Date: 2013-12-08T01:16:57Z
    Registry Expiry Date: 2015-01-23T05:00:00Z
    Sponsoring Registrar:MarkMonitor Inc. (R37-LROR)
    Sponsoring Registrar IANA ID: 292
    WHOIS Server:
    Referral URL:
    Domain Status: clientDeleteProhibited
    Domain Status: clientTransferProhibited
    Domain Status: clientUpdateProhibited
    Registrant ID:mmr-33684
    Registrant Name:DNS Admin
    Registrant Organization:Mozilla Foundation
    Registrant Street: 650 Castro St Ste 300
    Registrant City:Mountain View
    Registrant State/Province:CA
    Registrant Postal Code:94041
    Registrant Country:US
    Registrant Phone:+1.6509030800
    ```
    As you can see, I can't register `mozilla.org` because the __Mozilla Foundation__ has already registered it.

    On the other hand, let's see if I could register `afunkydomainname.org`:

    ```bash
    $ whois afunkydomainname.org
    NOT FOUND
    ```

3. Getting a domain name

    The process is quite straightforward:

    1. Go to a `registrar`'s website.
    2. Usually there is a prominent "Get a domain name" call to action. Click on it.
    3. Fill out the form with all required details. Make sure especially that you have not misspelled your desired domain name. Once it's paid for, it's too late!
    4. The registrar will let you know when the `domain name` is properly registered. Within a few hours, all `DNS servers` will have received your `DNS information`.

    __Note__: In this process the `registrar` asks you for your real-world address. Make sure you fill it properly, since in some countries registrars may be forced to close the domain if they cannot provide a __valid__ address.

4. DNS refreshing

    `DNS databases` are stored on every `DNS server` worldwide, and all these servers refer to a few ones called "authoritative name server" or "top-level DNS servers." Whenever your `registrar` __creates__ or __updates__ any information for a given domain, the information must be refreshed in every `DNS database`.
        - Each `DNS server` that knows about a given domain stores the information for some time before it is automatically invalidated and
        - then refreshed (the `DNS server` queries an _authoritative_ server again).
        - Thus, it takes some time for `DNS servers` that know about this domain name to get the up-to-date information.

    __Note__: This time is often called propagation time. However this term is not precise since the update is not propagating itself (top → down). `DNS servers` queried by your computer (down) are the ones that fetch the information from the authoritative server (top) when they need it.

### How does DNS request work?

As we already saw, when you want to display a webpage in your browser it's easier to type a domain name than an IP address. Let's take a look at the process:

1. Type `mozilla.org` in your browser's location bar.
2. Your `browser` asks your `computer` if it already recognizes the `IP address` identified by this `domain name` (using a _local_ `DNS cache`). If it does, the name is translated to the IP address and the `browser` negotiates contents with the `web server`. End of story.
3. If your `computer` does not know which `IP` is behind the `mozilla.org` name, it goes on to ask a `DNS server`, whose job is ___precisely___ to tell your computer which `IP address` matches each registered `domain name`.
4. Now that the computer knows the requested `IP address`, your `browser` can negotiate contents with the `web server`.

![DNS request](https://mdn.mozillademos.org/files/8961/2014-10-dns-request2.png)

## Next step

Okay, we talked a lot about processes and architecture. Time to move on.

- If you want to get hands-on, it's a good time to start digging into design and explore [the anatomy of a web page](https://developer.mozilla.org/en-US/Learn/Anatomy_of_a_web_page).
- It's also worth noting that some aspects of building a website cost money. Please refer to [how much it costs to build a web site](https://developer.mozilla.org/en-US/docs/Learn/How_much_does_it_cost).
- Or read more about [Domain Name](http://en.wikipedia.org/wiki/Domain_name) on Wikipedia.
