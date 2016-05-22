---
layout: default
title: Menu Options
permalink: /docs/menu-options/
---

Right clicking on the screen will produce a context menu with the following options

* __Copy__  
_Copies bounded area or if no bounded area selected copies the screen to the clipboard to be pasted_

* __Paste__  
_Pastes clipboard data to the screen_

* __Paste Special__  
_This will paste the data from the clipboard stripping all non letter and non numeric characters._

* __Selected columns and Selected rows__  
_Shows the status of the selection. We use this to count the characters of a selection. Note these two entries will only show up if there is a bounded area specified._

* __Sum Area__  
_This option will only show up if there was a bounded area selected for example copy and paste._

* __Print Screen__  
_Prints the screen_

* __Keyboard__  
_Presents a list of keyboard options that can be selected from the menu._

* __System Request__  
_Issues a System Request to the AS400 system._

* __Help__  
_NOTE this is not application help but the help key that is sent to the AS400._

* __Host Print__  
_This will send a host print to the AS400 which will print the screen to the users spool._

* __Display Messages__  
_Will only display if there are messages waiting (ie. the MW light is on). When the option is selected the messages will be displayed. Alt + M will also do this but you can press this at any time._

* __Hex Map__  
_Displays a hex map of ASCII characters that can be inserted into the current field._

* __Map Keys__  
_Displays a window to allow remapping of the keys for the emulator._

* __Settings__  
_Displays a window to allow the changing of the font, colors, cursor size and column separator._

* __Macros__  
_If there are macros defined then this item will be displayed. It will have a submenu of all macros defined across the sessions. More information can be found in the macros.txt file._

* __Export__  
_From this menu item you can select to export a file or a spool file._

* __File...__  
_The user is presented with a screen to fill out the file information to be downloaded. More information can be found in the filetransfers.txt file._

* __Spool...__  
_The user is presented with a screen to select the spool file to export. More information can be found in the spoolexport.txt file._

* __Send Screen__  
_Send screen via e-mail. More information can be found in the e-mail.txt file._

* __Connect/Disconnect__  
_This is a toggle switch. When connected this entry will read Disconnect and when disconnected this item will read Connect._

* __Close this session__  
_Will popup a options panel that will allow you to close the current session or all sessions and remove the sessions from the session tab panel._
