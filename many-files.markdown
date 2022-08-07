---
layout: wikipage
permalink: /many-files.html
---
# Sharing more than 100,000 files

The MuWire standalone client has been reported to work fine with around 500,000 shared files while using 2-3 GB of RAM.  The MuWire plugin however is limited to how much memory it can use by default.  With the default settings it can handle up to around 100,000 shared files. If you want to share many more than that, you should consider these tips:

### Tips for the plugin
* Increase the maximum memory of your I2P router.  That value is found in the `wrapper.config` file, the `wrapper.java.maxmemory` setting.  Default value is 256, and it is recommended to increase it by 256 for every 100,000 files you want to share.  You need to do a full router shutdown, exit, and start again after editing that file. 
* Do not try to view your shared files as a table because that will likely kill your browser.  Viewing them as a tree is much more efficient.

### Tips for both plugin and standalone
* Put your MuWire settings directory on an SSD, that will speed up initial loading significantly as many small files need to be processed.
* Set the following Linux kernel parameters:
  * `vm.swappiness=0` ( avoid swapping until we really run out of ram )
  * `vm.dirty_background_ratio=25` ( when to start considering flush pages to disk - helps coalesce writes and reduces write load )
  * `vm.dirty_ratio=50` ( at 50% page cache stop accepting new requests - avoids 'freezing' and the disc needs time absorb pages )
  * `vm.cache_pressure=1` ( keep pages cached - e.g. read blocks from a HDD - as long as possible - speeds up re-reads )
  * `vm.overcommit_memory=2`
  * `vm.overcommit_ratio=95`
  * `vm.min_free_kbytes=65536` (with high vm dirty ratios you need to make sure that the kernel itself has enough ram to handle memory management)
* Set ext4 mount option `noatime, nodiratime` ( disables read access logging of EVERY inode - only needed for security audits) 

### The MuWire settings directory
On the plugin it is inside the I2P settings directory under `plugins/MuWire`.  On the standalone:
* On Windows it is `C:\Users\username\AppData\Roaming\MuWire`
* On Mac it is `/Users/username/Library/Application Support/MuWire`
* On Linux it is `$HOME/.config/MuWire`

Happy sharing!
