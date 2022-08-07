---
layout: wikipage
permalink: /file-feeds.html
---
# File Feeds
With MuWire you can publish the files you share to your personal feed, and subscribe to the feeds of other users.  You can configure each individual feed separately, for example to download all files published by someone else.  This is very similar to following someone on a social network.

Personal feed options:
* Enable File Feed - whether to enable or disable your personal feed.  Default is enabled
* Advertise Feed In Search Results - whether to let other MuWire users know you have a feed.  Default is enabled
* Automatically Publish Shared Files - if enabled, every file you share or download will be published to your feed right away.  Default is disabled

Each subscription to someone else's feed can be configured the following way:
* Automatically Download - whether to download all new files published to the feed automatically.  Default is false
* Sequential Download - whether to download each file sequentially.  This makes previewing media files work better.  Default is false
* Items To Keep On Disk - how many of the items published to the feed to remember across restarts of MuWire.  If you set this value to -1 MuWire will remember all items published to the feed.  Default is 1000.
* Feed Update Frequency - how often to check the feed for new files.  Value is in minutes, default is one hour.

### Note about unpublishing

You can un-publish a file from your personal feed.  Anyone who is subscribed to your feed and has not yet seen the file you unpublish will not see it in their list.  However, if they have already seen the file you unpublish, it will not be removed from their list.

If you unshare a file you've published it is similar - anyone who is subscribed to your feed and has already seen the file will continue to see it.  They will not be able to download it though.
