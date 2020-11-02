---
weight: 1
title: "Break the bond"
date: 2020-10-31T00:00:00+08:00
lastmod: 2020-10-31T00:00:00+08:00
draft: false
author: "Cody"
authorLink: "https://theredone.io"
description: "Break a Cisco LACP Bond and recreate it later"
tags: ["cisco", "3750X", "lacp", "openvswitch", "proxmox", "pve"]
categories: ["how-to"]
toc:
  auto: false
---

# Mistakes were made 🤦🏻‍♂️

Recently I needed to edit the network configuration on my [Proxmox][1] cluster in the colocation. This process resulted in reconfiguring all network interfaces on all nodes because of a mistake I made. In the process, I needed to break the [LACP bond][2] to the [OpenVSwitch][3] to make a couple changes and then recreate the bond.

## Current State

Thank you port descriptions on Cisco switches. All 4 PVE nodes are configured the same and the interfaces are also in the same order. The commands and examples are for a Cisco `WS-C3750X-48T-S` Just to preface the below: this is more for my reference for when I inevitably make a mistake in the future.

```console
interface GigabitEthernet2/0/28
 description pve-eno3-bond0
 switchport trunk encapsulation dot1q
 switchport mode trunk
 channel-group Y mode active
end
```

## Break it

To break the bond and enable the `eno3` interface to act as a standard switchport:

```console
interface GigabitEthernet2/0/28
 no channel-group
 switchport native vlan XX
```

From here the switchport acts like a standard trunk port on the VLAN specified.

## Un-break it

To re-enable:

```console
interface GigabitEthernet2/0/28
 no switchport native vlan XX
 channel-group Y mode active
```

And there you have it. We were able to break the bond, assign the port to a default VLAN, and then return everything to normal.

Hopefully, this helps!

<!-- External Links -->
[1]: https://proxmox.com/en/proxmox-ve
[2]: https://en.wikipedia.org/wiki/Link_aggregation
[3]: https://pve.proxmox.com/wiki/Open_vSwitch
