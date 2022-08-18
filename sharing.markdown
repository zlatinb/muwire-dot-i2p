---
layout: wikipage
permalink: /sharing.html
---
# Sharing files
MuWire is all about sharing information.

## Initial Setup
There are several steps to sharing files with other users of MuWire:

### 1. Choose or create folders holding the shared files.
These can be anywhere on your computer.  Local directories may be better than network drives
because the system facility for 'watching' changes to a file is not automatic for networked drives.  You can set an option to use periodic checks by MuWire instead.

### 2. Tell MuWire about the folders and files
You do this in the **Library** view by dragging and dropping folders and files into the upper panel.

 ![Alt text](library.png)

### 3. Optionally add comments
You can add comments to your shared files explaining what they are.  These comments will appear to a searcher if they right-click on a discovered file and select "View Details".
You do this by adding a [Sidecar File](sidecar-files).


### 4. Optionally add a certificate
When you certify a file, you create a proof that you shared this file.  Even if you later delete the certificate, others may already have it so think carefully about whether you want to do this.

### 5. Optionally group into collections
A collection is an *optional* logical grouping of files that exists independently from the shared directories layout.  It is merely another organizing tool.
To create a collection, first share some files, then right-click on those files which you wish to include in the collection, and under "Other Actions" choose "Create Collection".

The collection is hierarchical and will try to find a common ancestor of the shared files.  Below that common ancestor the structure of the collection mimics what's on the filesystem.

The "Review" step is there to see exactly what the hierarchy looks like.

### 6. Optionally create a feed
While any MuWire user can browse your published files or locate them using *Search*, you can choose to set up a [*feed* of new files](file-feeds).  Other MuWire users can then *subscribe* to this feed and be automatically informed of additions you make.

### 7. Restrict access
Starting in MuWire version 0.8.13 it will be possible to restrict which users can see
which files are inside a folder.

## Monitoring downloads
Of course you will want to know if anybody is reading your stuff.

* If you look at the **Collections** view, you can see how many times your collection has turned up in a search.
* If you look in the **Feeds** view you can see how many times your files have been downloaded.
* If you right-click on a file in the **Library** view and choose "Show file details" you can see how many searches have discovered the file, the keyword that matched, and who downloaded it.

## Tips
* MuWire keeps track of files by a hash of their contents, not the file *name*.  Once a file has been published, you should avoid modifying it.

* There are [performance issues](many-files) if you are sharing a large number of files.
