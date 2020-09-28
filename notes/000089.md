---
layout: note
title: iPad Disconnection Issues
parent: OS and Software Help
grand_parent: Home
---

# iPad Disconnection Issues

## iPad constantly disconnecting and reconnecting when linked to your Mac?

1. Open the Terminal app (_Applications > Utilities_)
2. Enter the terminal command:

```shell
sudo killall -STOP -c usbd
```

3. Type in your admin password to confirm

---
