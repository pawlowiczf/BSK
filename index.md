---
title: BSK
layout: default
---

**Adres**: [https://pawlowiczf.github.io/bsk](https://pawlowiczf.github.io/bsk)  

## Laboratoria  

- [Lab 1 - Firewall/zapory ogniowe](firewalls/firewall.md)
- [Lab 2 - Prywatne VLANy + HSRP](notes/vlans.md)
- [Lab 2 - Gateway Load Balancing Protocol](notes/glbp.md)
  
## Przydatne konfiguracje 

- [Zdalny dostęp do routera/switcha przez SSH, TELNET](important/remote-access.md)


```python
from dimacs import *

G = loadGraph( "graph/e5" )
V = len(G)
for v in range(V):
  s = "%d :" % v
  for u in G[v]:
    s += " %d" % u
  print s
```