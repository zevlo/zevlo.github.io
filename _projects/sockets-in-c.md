---
layout: post
title: "Sockets in C"
date: 2025-11-14
description: "A daytime server, a chat room, and an HTTP server built on raw sockets in C"
github_url: "https://github.com/zevlo/sockets"
demo_url: "/assets/images/sockets-demo.png"
---

## About This Project

Three TCP servers built in C, each one layer above the last: a daytime
server, a multi-client chat room using select(), and a static HTTP web
server that serves files from www/ with request parsing and a traversal guard.

Source: [github.com/zevlo/sockets](https://github.com/zevlo/sockets)

Screenshot: [the web server's self-referential index page](/assets/images/sockets-demo.png)

### Technologies Used

- C
- BSD sockets API
- select() I/O multiplexing
- pthreads
- HTTP/1.1
