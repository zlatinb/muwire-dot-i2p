---
layout: wikipage
permalink: /sidecar-files.html
---
# Sidecar files

Sidecar files are text files that you can use to automatically add comments to your shared files.  The sidecar files themselves are not shared, but their content is added as a comment to the corresponding shared file.  If the searcher has not disabled searching in comments, any word present in a comment will trigger search results.  

### Requirements
* The sidecar file is a regular text file, but it will be loaded as UTF-8 so you can use foreign languages.
* The sidecar file must be present in the same directory as the corresponding shared file and have the same name but with the added extension of ".mwcomment"
* The maximum length of a comment is 32kb.  If a sidecar file is longer than that, it will be ignored.
* You need to share the sidecar file for it to be processed.  It will not appear in your list of shared files, but the corresponding shared file will be updated to have a comment.

### Notes about editing comments manually
If you are using sidecar files it's best not to edit comments manually through the UI afterwards.  If you want to change a comment, change it in the sidecar file and then re-share the sidecar file.

### Deleting comments
If you want to completely remove the comment from a shared file you need to 
1. Delete the sidecar file
2. Delete the comment through the UI

Without both of these steps the comment may re-appear after restart.

### Note about symlinks
MuWire resolves all symlinks.  If you use symlinks for your shared files or sidecar files, the final resolved path of the sidecar file and the shared file  must be the same in order for the sidecar file to be processed.
