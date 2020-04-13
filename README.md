# **Bind9 RPZ blacklist**
Ova lista se bazira uglavnom na hrvatskim portalim i stranicama na koje sam naišao a da su ili maliciozne ili da služe za reklame. U svojoj mreži koristim Raspberry Pi 3 kao DNS server. Za sada je samo jedan, ali planiram uvesti još jednoga pošto je preporučeno imati dva DNS servera. Ne koristim ih samo kao cache, već mi služe i za lokalnu mrežu. 

### **Requirements**
- BIND9
- http server lighttpd/apache/nginx (ako koristite sinkhole)

### **README**
- https://www.ionos.com/digitalguide/server/configuration/how-to-make-your-raspberry-pi-into-a-dns-server/
- https://www.zytrax.com/books/dns/ch9/rpz.html
- https://kb.isc.org/docs/aa-01310
