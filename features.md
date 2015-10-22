---
layout: default
title: Features
permalink: /features/
---

There are 3 modes provided: Basic, Enhanced, GUI Enhanced

Basic mode provides normal screen presentation. No extras are provided. This describes most of the emulators that I have used or downloaded and tried. Also; the tn5250 for linux falls in this category as well (Please; this is no slight on this emulator just an example for me to use without naming names. I used it until I started this project).

Enhanced mode provides other functions like cursor progression, windows, continued edit fields, edit masked fields, etc... This is where Client Access falls in (and more).

The GUI part comes in by manipulating the 5250 stream and painting the fields like gui constructs in windowing systems, gui looking popup windows in place of windows, painting the PF keys on the screen as buttons (hot spots) so when clicked it will send the appropriate aid key, as well as the enhanced functions described above. (See screen shots) This is basic gui enhancements that you can receive and interpret from the 5250 stream. At this time that is all tn5250j does. Maybe in the future it will become more advanced if and when I have the time (or I have help I do have a job).

There is a great article on systems that provide more enhanced/advanced green screen make over functions on the news400 site.

Other features provided are:

* __Non displayable characters__  
  A lot of the emulators that I used would stop responding if there was data that could not be displayed on the screen. An example would be a query on a file that had variable length fields (we have a lot here). The data that gets displayed will have all sorts of information embedded in it that looks like 5250 stream commands. When Client Access, Extra or tn5250j receives these invalid characters it notifys the AS400 and the AS400 corrects it and sends the information back in a displayable format (pretty cool on the AS400 controllers part). As a developer of AS400 applications you really need to be able to look at these files and I have spent a lot of time and code in making tn5250j make these checks. It is very annoying to use an emulator that will not do this (not to mention time consuming to switch to another emulator just to look at this type of information).

* __Character counter__  
  A character counter is provided. As a developer I was always counting characters on the screen one by one. I guess that is why my vision is so bad. So I added a character counter. When you select a bounded area for copy it will display the rows and columns of the bounded area (you have to press the right mouse button to get the information).

* __Hot spots__  
  Hot spots for the function keys like other emulators that I have seen. In the future I hope to expand on this. More to come I hope.

* __Message Wait Notification__  
  A lot of developers use the message wait notification to be notified when a job terminates. Instead of using the *BREAK for message notification which interrupts the screen there is a MW at the bottom of the screen that lets them know without interrupting their sleeping woops i mean thinking process. I know this sounds basic but I have seen emulators without this basic function.

* __Key Shortcuts__  
  A lot of the functions provided have short cut key sequencing to do the same. There are a lot of programmers out there that do not like to touch the mouse (I guess we are getting fewer but maybe that is where the linux users come in).

* __Attribute settings for screen/session__ 
  This is given on all emulators that I have tried. Just thought I would list it here. Although at this time tn5250j does not allow you to change the default key bindings. Nobody has requested it so for me it has not been given high priority. Where I work the developers all use pretty much the same key bindings. The users using the emulator seem to not care as long as it works and they can: do their job and change the colors for different sessions to different systems. This allows them to work on the different systems (we have 4 different systems with 4 different languages: English, French (Luxembourg;France), Portuguese, Spanish, German is also spoken but we have no systems that need to display the German character sets) and the colors allow them to visually distinguish the systems. I hope to see more languages from you. Let me know and I will put them in.

* __File transfer from host__  
  You can export files from the host in different formats. See file transfer section for more information

* __Scripting__  
  With release 0.5.5 you can now write scripts using the python language. This uses the wonderful project code at http://www.jython.org. See scripting section here

* __Spool file export__  
  With release 0.5.5 you can now export spool files from the host into PDF or Text format.
