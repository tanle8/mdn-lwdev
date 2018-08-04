# How do you upload files to a web server?

[Original Post](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Upload_files_to_a_web_server)

This article shows how to publish your site online with FTP tools.

- Prerequisites: You must know what a web server is and how domain names work. You must also know how to set up a basic environment and how to write a simple webpage.
- Objective: Learn how to push files to a server using FTP.

## Summary

If you have built a simple web page (see HTML basics for an example), you will probably want to put it online, on a web server. In this article we'll discuss how to do that using FTP.

Getting to grips with an FTP client: FileZillaEdit
There are several FTP clients out there. Our demo covers FileZilla, since it's free and available for Windows, macOS and Linux. To install FileZilla go to the FileZilla downloads page, click the big Download button, then install from the installer file in the usual way.

Note: Of course there are lots of other options. See Publishing tools: FTP clients for more information.

Open the FileZilla application; you should see something like this:



Link to sectionLogging in
For this example, we'll suppose that our hosting provider (the service that will host our HTTP web server) is a fictitious company "Example Hosting Provider" whose URLs look like this: mypersonalwebsite.examplehostingprovider.net.

We have just opened an account and received this info from them:

Congratulations for opening an account at Example Hosting Provider.

Your account is: demozilla

Your website will be visible at demozilla.examplehostingprovider.net

To publish to this account, please connect through FTP with the following credentials:

FTP server: ftp://demozilla.examplehostingprovider.net
Username: demozilla
Password: quickbrownfox
To publish on the web, put your files into the Public/htdocs directory.
Let's first look at http://demozilla.examplehostingprovider.net/ — as you can see, so far there is nothing there:

Our demozilla personal website, seen in a browser: it's empty

Note: Depending on your hosting provider, most of the time you'll see a page saying something like “This website is hosted by [Hosting Service].” when you first go to your web address.

To connect your FTP client to the distant server, follow these steps:

Choose File > Site Manager... from the main menu.
In the Site Manager window, press the New Site button, then fill in the site name as demozilla in the provided space.
Fill in the FTP server your host provided in the Host: field.
In the Logon Type: drop down, choose Normal, then fill in your provided username and password in the relevant fields.
Your window should look something like this:



Now press Connect to connect to the FTP server. When trying to connect to a real hosting server, you might have to provide other information such as a specific port number, or connecting via SFTP (secure FTP) instead of plain old FTP. Your hosting provider should tell you exactly what you need to use in any case.

Link to sectionHere and there: local and remote view
Once connected, your screen should look something like this (we've connected to an example of our own to give you an idea):



Let's examine what you're seeing:

On the center left pane, you see your local files. Navigate into the directory where you store your website (e.g. mdn).
On the center right pane, you see remote files. We are logged into our distant FTP root (in this case, users/demozilla)
You can ignore the bottom and top panes for now. Respectively, these are a log of messages showing the connection status between your computer and the FTP server, and a live log of every interaction between your FTP client and the server.
Link to sectionUploading to the server
Our example host instructions told us "To publish on the web, put your files into the Public/htdocs directory." You need to navigate to the specified directory in your right pane. This directory is effectively the root of your website — where your index.html file and other assets will go.

Once you've found the correct remote directory to put your files in, to upload your files to the server you need to drag-and-drop them from the left pane to the right pane.

Link to sectionAre they really online?
So far, so good, but are the files really online? You can double-check by going back to your website (e.g. http://demozilla.examplehostingprovider.net/) in your browser:

Here we go: our website is live!

And voilà! Our website is live!

Link to sectionOther methods to upload files
The FTP protocol is one well-known method for publishing a website, but not the only one. Here are a few other possibilities:

Web interfaces. An HTML interface acting as front-end for a remote file upload service. Provided by your hosting service.
GitHub (advanced). Upload through git with a combination of commit/push methods. See our Publishing your website articles from our Getting started with the Web guide.
Rsync (advanced). A local-to-remote file synchronizing system.
WebDAV. An extension of the HTTP protocol to allow more advance file management.