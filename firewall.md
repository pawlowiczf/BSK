---
title: Firewall/zapory ogniowe
layout: default
---

### Wzorzec działania zapor ogniowych:
- domyślne przepuszczanie, 
- domyślne odrzucanie 

### Urządzenia IDS/IPS
- IDS - Intrusion Detection System - wykrywa i raportuje  
- IPS - Inttrustion Protection System - wykrywa i reaguje 

![Urządzenia IDS/IPS](images/devices,ids,ips.png)

### Listy ACL (Access Control Lists)
Najprostsze klasyfikatory (**standard**) klasyfikują jedynie na podstawie adresu źródłowego. Są także rozszerzone (**extended**), które klasyfikują na podstawie: 
- adresów źródłowych i docelowych 
- informacji dodatkowej: numerów portów TCP, UDP, pakietach ICMP, flag TCP itd.

Pakiety przechodzą sekwencyjnie przez listę dostępu - dlatego na początku listy są wpisy najbardziej szczegółowe. 

Tworzenie firewalla przebiega dwuetapowo:   
1. Definiowanie listy o konkretnym numerze (określającym jej rodzaj):    
```access-list NUMER permit|deny ADRES_ŹRÓDŁOWY WILDCARD```
2. Przypisanie list konkretnym interfejsom:  
```ip access-group NUMER in|out```

Aby wyświetlić utworzone listy wywołaj: `show access-lists`