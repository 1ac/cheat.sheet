---
layout: post
title: Example code for view
date: '2018-11-11 00:00:00'
tags:
- python
---

# Python:
```python
import socket

sock = socket.socket()
sock.bind(('', 9090))
sock.listen(1)
conn, add = sock.accept()

print('connecdetd:  {}'.format(add))

while True:
    data = conn.recv(1024)
    if not data:
        break
    conn.send(data.upper())
conn.close()
```
