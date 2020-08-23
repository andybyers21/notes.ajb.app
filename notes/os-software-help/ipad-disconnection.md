---
layout: note
title: iPad Disconnection Issues 
parent: OS and Software Help
nav_exclude: true
---

# iPad constantly disconnecting and reconnecting when linked to your Mac?

1. Open the Terminal app (*Applications > Utilities*)
2. Enter the terminal command: 
```shell
sudo killall -STOP -c usbd
```
3. Type in your admin password to confirm