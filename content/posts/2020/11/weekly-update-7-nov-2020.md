---
weight: 1
title: "What am I working on this week?"
date: 2020-11-07T00:00:00+08:00
lastmod: 2020-11-07T00:00:00+08:00
draft: false
author: "Cody"
authorLink: "https://theredone.io"
description: "What am I working on this week?"
tags: ["update"]
categories: ["misc"]
lightgallery: false
toc:
  auto: true
---

# What am _I_ working on?

Today is just a check-in and status update on some of the projects from last week. The summary below and some next steps for these projects. As I work through these I will try to keep a log and link to these blog entries so that you can follow along my path or suggest improvements!

## Past

- [ ] Research suppliers on Alibaba that can manufacture a few [ESP32][1] based smart plugs

  - I need to research which board type is best

  - Initial thoughts were to use the BLE addresses of our various devices to track which room we are in at a given time and [Home-Assistant][1] would then be able to react based on this information. 

    - We are are an Apple iOS household and iOS randomizes BLE MAC addresses rendering tracking unusable. This project may be DOA.

- [ ] Move more of my [Home-Assistant][1] [config][2] to my new server

  - In progress, check out my [git repo][2]!

- [ ] Update some of my [Home-Assistant][1] [UI][2] and start creating a _tabletized_ version to mount on the wall

  - On hold, since I need to determine what size tablet, how many, and where and how they will be mounted

## Future

- [ ] Build out a few more of the services that I [self host][3] on the Proxmox cluster in the colocation

  - Priority will be [influxdb][4] and configure [Home-Assistant][1] to leverage it

- [ ] Continue moving configuration from existing [Home-Assistant][1]

- [ ] Research tablets for the tablet version of my [Home-Assistant][1] [UI][2]

  - Research mounting options that allow the table to be removed easily

- [ ] Build a [link shortener][5] for this blog

  - [Shlink][6] looks promising after some quick research

<!-- External Links -->
[1]: https://www.home-assistant.io/
[2]: https://github.com/claughinghouse/home-assistant-config
[3]: https://github.com/claughinghouse/infra
[4]: https://hub.docker.com/_/influxdb
[5]: https://github.com/claughinghouse/infra/blob/88bd6a1068f8de667519289687ddd3e8c8963809/hosts.ini#L4
[6]: https://github.com/shlinkio/shlink
