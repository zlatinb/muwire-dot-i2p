---
layout: wikipage
permalink: /plugin-migration.html
---

# Migrating from standalone to plugin

### Files to copy

These files are in your `$HOME/.MuWire` directory

* key.dat
* MuWire.properties
* the `files` directory 
* the `filefeeds` directory
* downloads.json
* trusted
* distrusted
* mesh.json
* the `filecerts` directory

### Migration process

To migrate your existing identity to the plugin, follow these steps

1. Install the plugin and stop it right away
2. Copy all the files from the list above to `$HOME/.i2p/plugins/MuWire`
3. Start the plugin

### Running standalone and plugin at the same time

To run the plugin and standalone at the same time, you need to use different identities.  Follow these steps to create a new identity with the same shared files

1. Install the plugin and stop it right away
2. Copy all the files from the list above **except** `key.dat` to `$HOME/.i2p/plugins/MuWire`
3. If you want to use a different nickname, edit `MuWire.properties` and change the line that starts with `nickname=`.  MuWire will run fine with the same nickname because the cryptographic identity will be different.
4. Start the plugin.
