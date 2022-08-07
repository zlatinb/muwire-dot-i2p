---
layout: default
permalink: /chat.html
---
# MuWire Chat

You can chat anonymously with other MuWire users through the MuWire chat system.  To do so, you need to either connect to someone else's chat server or run a chat server yourself and wait for someone to connect to you.

### Connecting To Someone Else's Server

You can see from the search results who is running a MuWire server.  If the checkbox in the "Chat" column is checked, you can press the "Chat" button and MuWire will connect to their server.  Otherwise, you can connect to their server if you know their address by pressing the "Connect To Remote server" button in the "Chat" tab.  For example, I'm running a chat server at the following address (copy-paste this):

`
AQAHemxhdGluYiN~3G-hPoBfJ04mhcC52lC6TYSwWxH-WNWno9Y35JS-WrXlnPsodZtwy96ttEaiKTg-hkRqMsaYKpWar1FwayR6qlo0pZCo5pQOLfR7GIM3~wde0JIBEp8BUpgzF1-QXLhuRG1t7tBbenW2tSgp5jQH61RI-c9flyUlOvf6nrhQMZ3aoviZ4aZW23Fx-ajYQBDk7PIxuyn8qYNwWy3kWOhGan05c54NnumS3XCzQWFDDPlADmco1WROeY9qrwwtmLM8lzDCEtJQXJlk~K5yLbyB63hmAeTK7J4iS6f9nnWv7TbB5r-Z3kC6D9TLYrQbu3h4AAxrqso45P8yHQtKUA4QJicS-6NJoBOnlCCU887wx2k9YSxxwNydlIxb1mZsX65Ke4uY0HDFokZHTzUcxvfLB6G~5JkSPDCyZz~2fREgW2-VXu7gokEdEugkuZRrsiQzyfAOOkv53ti5MzTbMOXinBskSb1vZyN2-XcZNaDJvEqUNj~qpfhe-ov2F7FuwQUABAAHAAAfqq-MneIqWBQY92-sy9Z0s~iQsq6lUFa~sYMdY-5o-94fF8a140dm-emF3rO8vuidUIPNaS-37Rl05mAKUCcB
`

Once you connect, you will be greeted with a message "Welcome to my chat server.  Type /HELP for list of available commands".  You can type `/HELP` in the input field and the server will print the commands it supports.

To start chatting, you need to join a room.  To see what rooms exist on the server, type `/LIST`.  To join a room or create one, type `/JOIN <room name>`.  For example, on my server there is a room called "#muwire".  To join that room, type `/JOIN #muwire`.  Once you're in the room, anything you say will be seen by everyone in the room.

### Running Your Own Server

To run your own server, click on the "Chat" tab and press the "Start Chat Server" button.  This will open the "Console" window where you can control your server.  You need to create a room and join it before someone can start chatting with you.

To see the address of your server, type `/INFO` in the server console.  You can then copy-paste that address and give it to others.

### Private Messages

To send someone a private message, double-click on their name in the list of room members to the left, or right-click on their name and select "Start Private Chat". **Private messages are not encrypted**, the server operator can see them.

### Blocking And Banning Users

If you are connecting to someone else's server, you can block other users from sending you messages by right-clicking on their name and selecting "Mark Distrusted".  That will not kick the user from the server, it will only prevent you from seeing anything the user says.

If you are running your own server and mark someone as DISTRUSTED, they will be disconnected from your server and will not be able to connect again.
