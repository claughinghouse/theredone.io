---
weight: 1
title: "What am I working on this week? - 14th Nov 2020 Edition"
date: 2020-11-14T00:00:00+08:00
lastmod: 2020-11-14T00:00:00+08:00
draft: false
author: "Cody"
authorLink: "https://theredone.io"
description: "What am I working on this week? - 14th Nov 2020 Edition"
tags: ["update"]
categories: ["misc"]
lightgallery: false
toc:
  auto: true
---

# What am _I_ working on this week?

Checking again for this week. I hope in the coming week to research more tablet mounting options and tablets with the hope that I can snag one during the holiday sales coming up. My largest project ended up not being viable so I have decided to scrap it and focus on some other outstanding tasks.


## From last week

- ~~[x] Research suppliers on Alibaba that can manufacture a few ESP-32 based smart plugs~~

  - ~~I need to research which board type is best~~

  - ~~Initial thoughts were to use the BLE addresses of our various devices to track which room we are in at a given time and [Home-Assistant][1] would then be able to react based on this information.~~ 

    - ~~We are are an Apple iOS household and iOS randomizes BLE MAC addresses rendering tracking unusable. This project may be DOA.~~

    - Turns out this _as expected DOA. Looks like I will be dropping this project for now and just going with standard ESP-8266 based plugs

- [ ] Move more of my [Home-Assistant][1] [config][2] to my new server

  - In progress, check out my [git repo][2]!

    - I need to finish sanitizing the files and push. _Soon_ I promise!

- [ ] Update some of my [Home-Assistant][1] [UI][2] and start creating a _tabletized_ version to mount on the wall

  - On hold, since I need to determine what size tablet, how many, and where and how they will be mounted

  - I plan to create another post and link it here with the different models that I have researched

- [x] Build out a few more of the services that I [self-host][3] on the Proxmox cluster in the colocation

  - Priority will be [influxdb][4] and configure [Home-Assistant][1] to leverage it

  - [Syncthing][5] and [Resilio Sync][6] are finished

- [ ] Continue moving configuration from existing [Home-Assistant][1]

- [ ] Research tablets for the tablet version of my [Home-Assistant][1] [UI][2]

  - Research mounting options that allow the table to be removed easily

- [ ] Build a [link shortener][7] for this blog

  - [Shlink][8] looks promising after some quick research

## This upcoming week

I plan to spend the upcoming week learning about different tablets and mounting methods. At a high level here are some initial requirements:

- [ ] 10+ inch screen 

- [ ] 1080p or higher resolution

  - Ideally, I would be able to find an [AMOLED][9] screen since I am a fan of the [Amoled Theme][10] for [Home-Assistant][1]

- [ ] Wireless charging so that I can recess the charger in the wall and lift it away without dealing with wires

- [ ] 5GHz WiFi support


<!-- External Links -->
[1]: https://www.home-assistant.io/
[2]: https://github.com/claughinghouse/home-assistant-config
[3]: https://github.com/claughinghouse/infra/blob/master/hosts.ini
[4]: https://hub.docker.com/_/influxdb
[5]: https://hub.docker.com/r/linuxserver/syncthing
[6]: https://hub.docker.com/r/linuxserver/resilio-sync
[7]: https://github.com/claughinghouse/infra/blob/master/hosts.ini#L4
[8]: https://shlink.io/
[9]: https://github.com/home-assistant-community-themes/amoled
[10]: https://en.wikipedia.org/wiki/AMOLED
