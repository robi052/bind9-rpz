# **Bind9 RPZ blacklist**
Ova lista se bazira uglavnom na hrvatskim portalim i stranicama na koje sam naišao a da su ili maliciozne ili da služe za reklame. U svojoj mreži koristim Raspberry Pi 3 kao DNS server. Za sada je samo jedan, ali planiram uvesti još jednoga pošto je preporučeno imati dva DNS servera. Ne koristim ih samo kao cache, već mi služe i za lokalnu mrežu. Blokirane su reklame koje webmasteri uposno forsiraju na stranicama ili koje su napadne. Reklame koje se normalno prikazuju nisu blokirane. Ukoliko imate kakvih upita, prijedloga, savjeta i dr to možete učiniti na [Issues](https://github.com/robi052/bind9-rpz/issues), a za sve ostalo je tu [kontakt forma](https://www.robertobilic.com/kontakt "Roberto Bilic Photography").

### **Requirements**
- BIND9
- http server lighttpd/apache/nginx (ako koristite sinkhole)

### **O listama**
- db.rpz.blacklist: Lista blokiranih stranica. Blokirane su reklame, maliciozne stranice i dr. Lista se učestalo osvježava, ali nije vam 100% zaštita. Nisu blokirane statistike poput Google Analytics i sl.
- db.rpz.safenet: Zaštita za djecu. Forsira sigurno pretraživanje Google i Bing tražilice. Za uključiti Google.com i google.hr ukloniti ispred tih linija znak ;. Za dodavanje googlea na drugim jezicima jednostavno dodati dvije adrese (bez i sa www). Može se i Youtube forsirati.
- db.rpz.whitelist: Lista url-ova za koje želimo da zaobiđu RPZ pravila (npr Netflix i sl.)
- db.sinkhole: Postavke za preusmjeravanje 

### **README**
- https://www.ionos.com/digitalguide/server/configuration/how-to-make-your-raspberry-pi-into-a-dns-server/
- https://www.zytrax.com/books/dns/ch9/rpz.html
- https://kb.isc.org/docs/aa-01310
- https://navytitanium.github.io/DNSMasterChef/
