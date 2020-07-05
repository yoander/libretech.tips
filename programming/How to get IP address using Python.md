---
title: "How to get IP address using Python?"
date: 2020-07-05 12:17:29
categories: [programming]
tags: [pyhton]
authors: sedlav
---

Use gethostbyname and gethostname from socket packet

## Using stat function

```python
#!/usr/bin/env python3
import socket
print(socket.gethostbyname(socket.gethostname()))
```
