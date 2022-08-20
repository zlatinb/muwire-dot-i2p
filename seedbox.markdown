---
layout: wikipage
permalink: /seedbox.html
---

<style>
div.download-container {
  display: block;
  border: 0.25em solid black;
  border-radius: .8em;
  margin : 1em;
  padding : 0.2em;
}

a.get-muwire {
   display: inline-block;
  top: 50%;
  padding: .4em;
  margin: .2em;
  line-height: 1em;
  font-size: 1.8em;
  color: white;
  font-family: Arial, Helvetica, sans-serif;
  font-weight: bold;
  text-transform: uppercase;
  text-decoration: none;
  text-align: center;
  //background: green;
  background-image : radial-gradient(#3fb97a 30%, green);
  border-radius: .3em;
  text-shadow: 1px 1px 1px rgba(0,0,0,.2);
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3), 1em 3em 2em 0.5em rgba(255, 255, 255, 0.3) inset, inset -.2em -.5em 1em -0em rgba(0,0,0,.3);
  border : 3px solid black;
}
a.get-muwire:hover {
  color: #333333
}
</style>

# MuWire Seedbox Daemon (ALPHA)

If you have a lot of files that you just want to share and are not interested in any of the search, download or communication functionality MuWire offers, a "SeedBox" solution may be right for you,

<center>
<div class="download-container">
<h2>MuWire Seedbox Daemon</h2>
You need to have a Linux system with Java 11 or newer.<br/>
(Download size 37 MB)<br/>
<a class="get-muwire" href="/downloads/muwire-seedbox-daemon-0.0.1.jar">Executable JAR file</a>
</div>
</center>

## Quick Start
1. Download the .jar file and mark it as executable
2. Create a file called `application.properties` in the current working directory.

The following configuration options should be included in that file

|Name|Description|Required|
|---|---|---|
|i2p.host|Host where the I2P or I2Pd router is running|yes|
|i2p.port|Port on which the I2CP interface is listening|yes|
|i2p.tunnelLength|How long should the tunnels be |yes|
|i2p.tunnelQuantity|How many tunnels to build|yes|
|i2p.tunnelName|Name of the tunnel to report to the I2P router | No|
|muwire.nickname|NIckname to use on the MuWire network|Yes|
|muwire.workDir|Directory to use for storing file indices and others|Yes|
|rpc.iface|Interface on which to bind the JSON-RPC endpoint|Yes|
|rpc.port|Port on which to bind the JSON RPC endpoint|Yes|


<br/>
Now you can launch the .jar file.  It will print a lot of stuff on `stdout`, that is normal.

## Try some commands

Assuming that you bound the rpc interface to localhost:12345

To check the current status of the seedbox daemon:
```
curl  -d '{"id":0,"method":"status"}' http://localhost:12345/seedbox
```

To share a file or directory on the local filesystem:
```
curl  -d '{"id":0,"method":"share", "params":["/absolute/path"]}' http://localhost:12345/seedbox
```

To un-share a file or directory that is currently shared:
```
curl  -d '{"id":0,"method":"unsharePath", "params":["/absolute/path"]}' http://localhost:12345/seedbox
```

To shut down the daemon gracefully:
```
curl  -d '{"id":0,"method":"shutdown"}' http://localhost:12345/seedbox
```

