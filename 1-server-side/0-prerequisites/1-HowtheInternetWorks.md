# How does the Internet work?

[Original post](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work)

This article discusses what the Internet is and how it works.

- Prerequisites: None, but we encourage you to read the [Article on setting project goals](https://developer.mozilla.org/en-US/docs/Learn/Thinking_before_coding) first
- Objective:
    - You will learn the basics of the technical `infrastructure of the Web` and
    - the difference between `Internet` and the `Web`.

## Summary

The __Internet__ is the backbone of the Web, the technical `infrastructure` that makes the Web possible. At its most basic, the Internet is a __large network of computers__ which communicate all together.

[The history of the Internet is somewhat obscure](http://en.wikipedia.org/wiki/Internet#History). It began in the 1960s as a US-army-funded research project, then evolved into a public infrastructure in the 1980s with the support of many public universities and private companies. The various technologies that support the Internet have evolved over time, but the way it works hasn't changed that much: Internet is a way to connect computers all together and ensure that, whatever happens, they find a way to stay connected.

## Deeper dive

### A simple network

When two computers need to communicate, you have to _link_ them, either physically (usually with an Ehthernet cable) or wirelessly (for example with WiFi or Bluetooth systems). All modern computers can sustain any of those connections.

__Note__: For the rest of this article, we will only talk about physical cables, but wireless network works the same.

![Two computers linked together](https://mdn.mozillademos.org/files/8441/internet-schema-1.png)

Such a network is not limited to two computers. You can connect as many computers as you wish. But it gets complicated quickly. If you're trying to connect, say, ten computers, you need 45 cables, with __nine__ plugs per computer!

![Ten computers all together](https://mdn.mozillademos.org/files/8443/internet-schema-2.png)

To solve this problem, each computer on a network is connected to a special tiny computer called a `router`. This `router` has only one job: like a signaler at a railway station, it makes sure that a `message` sent from a given computer arrives at the ___right___ destination computer. To send a message to computer `B`, computer `A` must send the message to the router, which in turn forwards the message to computer `B` and makes sure the message is not delivered to computer `C`.

Once we add a router to the system, our network of 10 computers only requires 10 cables: a single plug for each computer and a router with 10 plugs.

![Ten computers with a router](https://mdn.mozillademos.org/files/8445/internet-schema-3.png)

## A network of networks

So far so good. But what about connecting _hundreds_, _thousands_, _billions_ of computers? Of course a single `router` can't scale that far, but, if you read carefully, we said that a `router` is a computer like any other, so what keeps us from connecting two routers together? Nothing, so let's do that.

![Two routers linked together](https://mdn.mozillademos.org/files/8447/internet-schema-4.png)

By connecting computers to routers, then routers to routers, we are able to scale infinitely.

![[outers linked to routers](https://mdn.mozillademos.org/files/8449/internet-schema-5.png)

Such a network comes very close to what we call the Internet, but we're missing something. We built that network for our own purposes. There are other networks out there: your friends, your neighbors, anyone can have their own network of computers. But it's not really possible to set cables up between your house and the rest of the world, so how can you handle this? Well, there are already cables linked to your house, for example, `electric power` and `telephone`. The telephone infrastructure already connects your house with anyone in the world so it is the perfect wire we need. To connect our network to the telephone infrastructure, we need a special piece of equipment called a `modem`. This `modem` turns the information from our network into information manageable by the telephone infrastructure and vice versa.

![A router linked to a modem](https://mdn.mozillademos.org/files/8451/internet-schema-6.png)

So we are connected to the `telephone infrastructure`. The next step is to send the messages from our network to the network we want to reach. To do that, we will connect our network to an `Internet Service Provider` (ISP). An `ISP` is a company that 

- __manages some special routers that link all together__ and
- __can also access other ISPs' routers__.

So the message from our network is carried through the network of `ISP networks` to the destination network. The Internet consists of this whole infrastructure of networks.

![Full Internet stack}(https://mdn.mozillademos.org/files/8453/internet-schema-7.png    )

### Finding computers

If you want to send a message to a computer, you have to specify which one. Thus any computer linked to a network has a unique address to identify it, called an `"IP address"` (where IP stands for _Internet Protocol_). It's an address made of a series of four numbers separated by dots, for example: `192.168.2.10`.

That's perfectly fine for computers, but we human beings have a hard time remembering that sort of address. To make things easier, we can __alias__ an IP address with a human readable name called a _domain name_. For example, `google.com` is the domain name used on top of the IP address `173.194.121.32`. So using the domain name is the easiest way for us to reach a computer over the Internet.

![Show how a domain name can alias an IP address](https://mdn.mozillademos.org/files/8405/dns-ip.png)

### Internet and the web

As you might notice, when we browse the Web with a Web browser, we usually use the domain name to reach a website. Does that mean the Internet and the Web are the same thing? It's not that simple. As we saw, the Internet is a technical infrastructure which allows billions of computers to be connected all together. Among those computers, some computers (called _Web servers_) can send messages intelligible to web browsers. The _Internet_ is an infrastructure, whereas the _Web_ is a service built on top of the `infrastructure`. It is worth noting there are several other services built on top of the Internet, such as email and IRC.

## Next step

- [How the Web works](https://developer.mozilla.org/en-US/Learn/Getting_started_with_the_web/How_the_Web_works)
- [Understanding the difference between a web page, a web site, a web server and a search engine](https://developer.mozilla.org/en-US/docs/Learn/page_vs_site_vs_server_vs_search_engine)
- [Understanding domain names](https://developer.mozilla.org/en-US/docs/Learn/Understanding_domain_names)