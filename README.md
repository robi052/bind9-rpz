# Bind9 RPZ - Croatia & Balkans Blocklist

Ovaj repozitorij sadrži konfiguraciju za BIND9 DNS server koristeći RPZ (Response Policy Zone). 

### Datoteke:
* **db.rpz.blacklist**: Glavna lista za blokiranje (Oglasi, Malware, Scam).
* **db.rpz.safenet**: Forsiranje SafeSearch-a za djecu (Google, Bing, YouTube).
* **db.rpz.whitelist**: Iznimke koje DNS ne smije blokirati.
* **db.sinkhole**: Preusmjeravanje na lokalni web server.

### Kako ažurirati:
1. Kopirajte datoteke u `/etc/bind/zones/`
2. Povećajte **serial number** u SOA zapisu.
3. Restartajte bind: `rndc reload` ili `systemctl restart bind9`.
