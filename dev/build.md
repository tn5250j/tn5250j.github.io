---
layout: default
title: Building
permalink: /dev/build/
---

We currently use Apache Ant to build TN5250J. Documentation and installation files can be found at [ant.apache.org](https://ant.apache.org/)

## Building in SSL support

The build process does not include SSL support as default. To compile the files that are associated with SSL you must use the `-DSSL=true` flag when executing the build process.  
    
