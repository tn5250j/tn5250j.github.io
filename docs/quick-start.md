---
layout: default
title: Quick Start
permalink: /docs/quick-start/
---

`java -jar tn5250j.jar`

On first invocation of the emulator there where be some warning messages that will be output to the console. These are to inform you that defaults files are being setup for you for first run.

You will be presented with a Connections screen for defining sessions. Select the configure button to define sessions when the session selection window is displayed.

You can connect directly to a server using the following command:
`java -jar tn5250j.jar host -p port`

If you prefer to just run a command not use the Connections screen, the following command line options are available:

Option | Description
---|---
`-p` | Port to be used. Default is port 23 if not specified
`-f` | Configuration file. This is defined on the Session Configuration screen under Options Tab - Configuration File Name.
`-t` | Use system name instead of system id Host IP Address/DNS Host name.
`-cp` | Code Page. 37 - US default. 37PT - Portuguese. 273 - German. 280 - Italian. 284 - Spanish. 297 - French. 500-ch - Switzerland. 870-pl - Poland
`-e` | Enhanced 5250 option.  This gives graphical windows, edit masked fields, continued edit fields, etc.
`-L` | Specify the locale/language to be used for literals.  The default is the locale of the system if it is supported.
`-132` | Change to 27*132 column.
`-s` | Start up emulator using an existing configured session you can specify multiple of these as in -s xxxx -s yyyy and at startup the emulator will start up session xxxx and yyyy. This does not use the sessions file but the entries that are defined inside for PRE-EXISTIING session definitions.
`-width` | Start up emulator using the width specified
`-height` | Start up emulator using the height specified
`-d` | If no other instances are running and the -nc options is not specified then start up the bootstrap monitoring thread
`-nc` | no check for other tn5250j instances that are running. A new frame will be created within another instance of JVM
`-noembed` | Do not add a new session tab but open in new frame.  Default is embed so add a new session tab in the visible frame.
`-usp` | Use Socks Proxy
`-sph` | Socks Proxy Host
`-spp` | Socks Proxy Port
`-dn` | This option takes a device name parameter to be used by the Host.  The device name is 10 characters in length and follows rfc2877.
`-MDI` | Use the MDI interface represented by JInternalFrames instead of tabs.
      
## Example of command line options

This will change the default language of the system to use the languange translations of what is specified.  
`java -jar tn5250j.jar -L es`

This will connect to hostAS400 and use the file hostAS400.prop as the property file. Any properties that are changed will be saved to this file under the current directory. It does not have to exist as it will be created. If there are any properties saved from a previous session then those will be read and used. It uses the code page 37 which is default.  
`java -jar tn5250j.jar hostAS400 -f hostAS400.prop`

This will connect to parisAS400 use the property file as described above and use the code page 297 for french.  
`java -jar tn5250j.jar parisAS400 -f parisAS400.prop -cp 297`

This will connect to spainAS400 use the property file as described above and use the code page 284 for spanish and will notify the as400 that it can send enhanced commands.  
`java -jar tn5250j.jar spainAS400 -f spainAS400.prop -cp 284 -e`

## Sample sessions file
```
luxembourg=lux -f luxgui.prop -e -gui
lux-nogui=lux -f lux.prop -e
houilles=houilles -f houilles.prop -cp 297 -e
paris=paris -f paris.prop -cp 297 -e
spain=spain -f spain.prop -cp 284 -e
```

<p class="message-info">Session names are case sensitive.</p>

Example of command line option -s  
`java -jar tn5250j.jar -s luxembourg`
    
This will search the session file for the entry luxembourg and if found use the the entry parameters that are defined for that session.

So using the Sample sessions file described above the program would read the -s option and obtain luxembourg. It would then search the sessions file for this entry and if found execute the options that where there:

system/ip addrss = lux configuration file = luxgui.prop -e = use enhanced mode -gui = start in gui mode

If an entry is not found for the -s option then the Connection dialog is displayed for you to enter a new connection or select a pre existing one from the list.
