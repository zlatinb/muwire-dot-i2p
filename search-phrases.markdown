---
layout: wikipage
permalink: /search-phrases.html
---

# Searching with MuWire

## Keywords
The simplest form of search on MuWire is for keywords.  Just enter one or more keywords into the search box and MuWire will search for files whose names match those keywords.  If you enter more than one keyword, all keywords must match for a result to be returned.

By default MuWire will search in the names of the folders that contain shared files and in any comments the user has left for the files.  You can disable that behavior in the options.

## Regular Expressions
As of version 0.8.12 (currently available as [beta](/beta.html)) MuWire can search for regular expressions.  Regular Expressions are a powerful way to search for many things at once.  For more information on regular expressions check [WikiPedia](https://en.wikipedia.org/wiki/Regular_expression).

To search for a regular expression, surround your query with `/`.  Here are some examples:

* `/.*zip$/` will search for files that end in "zip"
* `/.*[Mm]u[Ww]ire.*/` will search for files that contain any of the strings "MuWire", "Muwire", "muWire" or "muwire".

Be cautious when using wildcards as you may overwhelm your MuWire node with results!

## Search Phrases
Since version 0.5.8 MuWire supports phrases in search terms.  If you surround several words in quotation marks, you will only see results that match all those words in that order, either in the file name or in the comment.

You can also mix phrases with regular keywords, as demonstrated in the example below

### Examples

Let's say you have three shared files:

1. "My Siamese cat videos.avi"
2. "Videos of my Siamese cat.avi"
3. "Cat videos of my Siamese.avi"

Then the following searches will return the following results:

* `cat videos` - 1,2,3
* `"cat videos"` - 1,3  
* `"siamese cat videos"` - 1
* `siamese "cat videos"` - 1,3

