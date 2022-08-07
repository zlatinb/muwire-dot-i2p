---
layout: default
permalink: /cli-options.html
---
# CLI Configuration Options

### Core Options

These go in $HOME/.MuWire/MuWire.properties

* *allowUntrusted* (true/false) Whether to allow connections not marked as trusted.  Default is true.  If you set this to false MuWire will only connect to peers marked as "Trusted"
* *searchExtraHop* (true/false) If you set "allowUntrusted" to false, your queries will only travel to those whom you've marked trusted and are directly connected to.  This option allows you to send your queries one hop further.  It may reach nodes you have not marked as Trusted though.
* *allowTrustLists* (true/false) Whether to allow others to subscribe to your trust list.  Default is true.
* *trustListInterval* (integer) How often to check the trust lists you're subscibed to for updates.  Value is in hours.  Default is 1 hour.
* *downloadRetryInterval* (integer) How often to retry failed downloads.  Value is in seconds.  Default is 60 seconds.
* *downloadLocation* (path) Absolute path to directory where downloaded files should be saved.  Defaults to $HOME
* *incompleteLocation* (path) Absolute path to directory where downloads in progress should be stored.  Defaults to $HOME/.MuWire/incompletes
* *updateCheckInterval* (integer) How often to check for MuWire updates.  Value is in hours.  Default is 24 hours.
* *autoDownloadUpdate* (true/false) Whether to download new MuWire updates automatically.  If set to false, you will only receive a notification that a new version is available.  Default is true
* *shareDownloadedFiles* (true/false) Whether to automatically share files you have downloaded.  Default is true.
* *shareHiddenFiles* (true/false) Whether to share hidden files.  Default is false.
* *searchComments* (true/false) Whether to search in the comments of shared files for keywords matching your query.  Default is true.
* *browseFiles* (true/false) Whether to allow others to browse your files.  Default is true.
* *totalUploadSlots* (integer) How many uploads to allow overall.  -1 means unlimited.  Default is -1.
* *uploadSlotsPerUSer* (integer) How many uploads to allow to any given user.  -1 means unlimited.  Default is -1
* *startChatServer* (true/false) Whether to start the chat server on startup.  Default is false
* *maxChatConnections* (integer) Maximum number of chat connections to allow.  -1 means unlimited.  Default is -1
* *advertiseChat* (true/false) Whether to advertise chat ability in search results.  Default is true
* *chatWelcomeFile* (path) Absolute path to the file whose contents are to be displayed in the welcome message.  Default none (shows default welcome message)

### UI Options

These go in $HOME/.MuWire/cli.properties

* *clearCancelledDownloads* (true/false) Whether to automatically remove cancelled downloads from the download list.  Default is true.
* *clearFinishedDownloads* (true/false) Whether to automatically remove finished downloads from the download list.  Default is false.
* *clearUploads* (true/false) Whether to automatically remove finished uploads from the upload list.  Default is false.
