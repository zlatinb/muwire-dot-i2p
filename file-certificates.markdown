---
layout: wikipage
permalink: /file-certificates.html
---
# Shared File Certificates

Since MuWire version 0.5.8 you can issue certificates for the files you share.  A certificate is a proof that you shared the file, and anyone on the network can verify that.

**WARNING** Once issued a certificate cannot be revoked.  Even if you delete the certificate from your disk, others may have already gotten it.  Do not do this unless you are absolutely sure.  The GUI will warn you about this as well.

### Why certificates are useful

Certificates help you make a more informed decision whether to download a file or not.  Imagine the following scenario:

1. Alice shares a file and issues a certificate for it.  
2. Bob downloads the file from Alice and imports the certificate Allice issued.
3.  Alice then goes offline.  
4. Charlie comes online and searches for the same file.  Bob returns a search result which says the file has certificates associated with it.  
5. Charlie fetches the certificate(s) and verifies that at some point Alice shared the given file.


### Under the hood

A certificate is a signed document that contains a timestamp, the name of the file, the hash of the file and the identity of the person signing it.  If the file has a comment, the comment is stored in the certificate as well.  Because of that, if you change the comment you need to issue the certificate again.

Certificate files are stored in `$HOME/.MuWire/filecerts` and follow the naming convention `<hash of file>_<issuer>_<timestamp>.mwcert`.  You can view the certificates you have issued or imported with the Tools->Certificates menu.  


