---
layout: wikipage
permalink: /security.html
---
# MuWire Security

This page describes security issues involved with running MuWire.  It also lists security vulnerabilities as they are discovered.

## General MuWire plugin security

Currently the plugin makes heavy use of the in-line javascript `onclick` event handlers and the `innerHTML` method for DOM manipulation. Effort is underway to transition to events in script files and `innerText()` so that input is effectively sanitized and a more strict CSP header policy can be enforced, but until then it is recommended that you:

1. Set a password to the router console via the I2P UI Configuration page, which is usually at `http://127.0.0.1:7657/configui`
2. Open MuWire tabs only in "private" window or use idk's Firefox plugin for "I2P In Private Browsing" which has a dedicated container tab for MuWire.
<hr/>
## Vulnerabilities

### Deanonymization via message

* Affects: MuWire desktop client
* Reported by: zlatinb
* Date: 07 Jul 2021
* Affects: 0.8.7 and older
* Fix version: 0.8.8

Description:

Clearnet link: [CVE-2021-32750](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-32750)

An attacker can send a message with a subject like
```
<html><img src="https://my.tracking.server.com/pixel.png"/></html>
```
MuWire would try to fetch the image via clearnet, exposing the IP address of the user.


### Arbitrary JS execution in `/FileDetails` page

* Affects: MuWire plugin
* Reported by: Beardog from VoidNet `hq2eu32pgrk2hjjwbhidevgo2yz2ka5aoy7ur5csjxqpwpu7kz754lid.onion`
* Date: 04 Jul 2021
* Affects: 0.8.7-b0 and older
* Fix version: 0.8.7-b1

Description:

An attacker can craft a link that will cause the browser to execute arbitrary Javascript if an affected MuWire plugin is installed.  This can lead to deanonymization, sharing of arbitrary file from the filesystem where the browser or the plugin are running, and gain access to all functions that are available in the router console.

Test:

To see if your MuWire plugin is susceptible to this attack, <a href="http://127.0.0.1:7657/MuWire/FileDetails?path=Lw==,PGltZyBzcmM9InRlc3QiIG9uZXJyb3I9ImphdmFzY3JpcHQ6YWxlcnQoMSkiPgo=">click here</a>.  If you see a Javascript alert popup you should update your plugin immediately.
