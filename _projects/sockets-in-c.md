---
layout: post
title: "Sockets in C"
date: 2025-11-14
description: "A daytime server, a chat room, and an HTTP server built on raw sockets in C"
github_url: "https://github.com/zevlo/sockets"
demo_url: "/assets/images/sockets-demo.png"
---

## About This Project

This project is three small servers written in C on the raw BSD sockets API.
Each server adds one idea on top of the last.

The daytime server does one thing: connect to it and it sends back the current
date and time, then hangs up. The chat room lets several people talk at once;
one select() loop watches every connection and hands each message to everyone
else. The web server serves files from its www/ folder over HTTP: it reads each
request, refuses paths that try to escape the folder, and sends back the
matching file or an error page.

Source: [github.com/zevlo/sockets](https://github.com/zevlo/sockets)
Screenshot: [the web server's self-referential index page](/assets/images/sockets-demo.png)

### Technologies Used

- C
- BSD sockets API
- select() I/O multiplexing
- pthreads
- HTTP/1.1
