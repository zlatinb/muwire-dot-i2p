---
layout: wikipage
permalink: /
---

<div class="logoAndForkMe">
    <span class="forkme">
        <a href="http://git.idk.i2p/zlatinb/muwire"><img width="149" height="149" src="/forkme.png" class="attachment-full size-full" alt="Fork me on GitLab" data-recalc-dims="1"></a>
    </span>
    <span class="logo">
    <img src="MuWire.png"/><br/>
        <center><p><b><font size="+2">Easy anonymous file sharing  using I2P technology</font></b></p></center>
    </span>
</div>

<style>
div.logoAndForkMe {
    position: relative;
}
span.forkme {
    float:left;
    position:absolute;
}
div.mucats {
    display: inline-block;
    text-align: center;
    padding: 0.3em;
}

div#all-downloads-container {
  display: inline-block;
}
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

a.get-beta {
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
  background-image : radial-gradient(orange 30%, darkorange);
  border-radius: .3em;
  text-shadow: 1px 1px 1px rgba(0,0,0,.2);
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3), 1em 3em 2em 0.5em rgba(255, 255, 255, 0.3) inset, inset -.2em -.5em 1em -0em rgba(0,0,0,.3);
  border : 3px solid black;
}
a.get-beta:hover {
  color: #333333
}

a.plugin {
   display: inline-block;
  top: 50%;
  padding: .4em;
  margin: .2em;
  line-height: 1em;
  font-size: 1.4em;
  color: white;
  font-family: Arial, Helvetica, sans-serif;
  font-weight: bold;
*sha*  text-transform: uppercase;
  text-decoration: none;
  text-align: center;
  //background: green;
  background-image : radial-gradient(blue 30%, darkblue);
  border-radius: .3em;
  text-shadow: 1px 1px 1px rgba(0,0,0,.2);
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3), 1em 3em 2em 0.5em rgba(255, 255, 255, 0.3) inset, inset -.2em -.5em 1em -0em rgba(0,0,0,.3);
  border : 3px solid black;
}
a.plugin:hover {
  color: #333333
}

</style>

MuWire is an anonymous file-sharing program.  It uses I2P for all communication keeping your IP address and activities private.  You can share, search and download files of any type.

MuWire is open-source.  You can find the source code on the GitLab link at the top of this page.

<!--
<div class="mucats"><a href="http://mucats.i2p"><img src="/mucats.png" width="80" height="80"/></a><b>NEW</b> Try out the <a href="http://mucats.i2p">MuCats</a> site where you can find and publish files shared with MuWire.</div>
-->

<br/>
# Download MuWire 0.8.12

<center>
<div id="all-downloads-container">
<div class="download-container">
<h2>Easy Install Bundle</h2>
Comes with everything you need to run MuWire.<br/>
( Download size up to 53MB )<br/>
<a class="get-muwire" href="/downloads/MuWire-0.8.12.exe">Windows</a>
<a class="get-muwire" href="/downloads/MuWire-0.8.12.dmg">Mac</a>
<br/>
<a class="get-muwire" href="/downloads/MuWire-0.8.12.AppImage">Linux x86-64</a>
<a class="get-muwire" href="/downloads/MuWire-aarch64-0.8.12.AppImage">Linux AARCH64</a>
</div>
<div class="download-container">
<h2>Small Download Bundle</h2>
You need to have Java 11 or newer.<br/>
( Download size 27MB )<br/>
<a class="get-muwire" href="/downloads/MuWire-0.8.12.zip">ZIP File</a>
</div>
<div class="download-container">
Interested in trying the latest features?<br/>
<a class="get-beta" href="/beta.html">BETA</a>
</div>
<div class="mucats">
[ I2Pd users please see the <a href="/i2pd.html">I2Pd instructions</a>. ]
</div>
</div>
</center>


# Running MuWire

The first time you run MuWire it will ask you to choose a nickname.  That nickname is combined with a cryptographically strong I2P address and forms your unique identity on MuWire.  My MuWire identity is `zlatinb@3k2gijdfdcuczkfypfddj4qsnnf744mj`

# Features
* **Search for files**: You can [search for files](search-phrases) shared by other MuWire users.

* **Share files**: 
You can [share your own files](sharing) with other MuWire users, with several options:
    * You can organize the files into [automatic feeds](file-feeds) like for a blog.
    * You can add comments about your shared files.
    * You can [issue a certificate](file-certificates) for a file you share to prove to others that you have the file.

* **Messages And Chat**: 
You can communicate with other MuWire users via messages and real-time chat.  

* **Trust**:
You can choose to [trust or distrust](trust) other MuWire users.


