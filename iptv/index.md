
# MÉRÉSI JEGYZŐKÖNYV   
# Méréstechnikai Feladat: Hálózat tervezés      

**A mérést végző neve:** Pongó Tamás  
**A mérés tárgya:**    
**A mérés száma:** 01. mérés    
**A mérés dátuma:** 2025. 02. 03.    
**A mérést vezette:** Sándor Péter    

**Évfolyam:** 13. E  
**Csoport:** GYAK 1  
**Helyszín:** V3 Labor  

## Feladat Célja    
Komplex távközlési hálózat tervezése, telepítése és mérése  

## Felhasznált Eszközök :  
- Antenna: Beltéri vagy kültéri antenna (a vizsgázó választása alapján)
- Fejállomás: LEMCO SCL-824CT 8 × DVB-S/S2/T/T2/C to 4 × DVB-T/C & IP (FTA)
- Set-top box: MAG IPTV
- Hálózati eszköz: IGMP protokollt támogató és DHCP képes router internet kapcsolattal
- Mérőműszer: METEK HDD digitális TV jelmérő
- Koaxiális kábelek és csatlakozók (már előkészítve egy másik vizsgafeladat során)
- Jelosztó: jelosztó a fejállomás bemeneteire érkező jelek kialakításához
- UTP kábelek az IPTV jel továbbításához
- Szerelési eszközök: csavarhúzó, villáskulcs, kábelvágó, iránytű, dőlésszögmérő

## Feladat célja:
Alaphelyzetbe állítottam az eszközt, hogy ne befolyásolják semmilyen zavaró tényezők. Ezt követően megtekintettem az fmdx.hu oldalon az Avas-torony csatornakiosztását.

Ezután rátaláltam a Miskolc Városi TV adására, amely a 634 MHz-es csatornán található. Ezt a csatornát választottuk, mivel ez sugároz a leggyengébben (0,126 kW), és ha ezen a frekvencián megfelelő a vétel, akkor a többi csatornán is jó lesz.

![x](https://github.com/user-attachments/assets/49ca5a2d-ff1b-48bb-bf37-3358bd1138e3)

Távolság az iskolánk és az adó torony között

![adotorony](https://github.com/user-attachments/assets/a5d4c0cb-a689-4289-991f-7855c21af0ea)

### Metek HDD adatok:  

![409261290-bb14acd7-33ab-42c0-a2e5-1fec20f5b9b4](https://github.com/user-attachments/assets/71fcbf7c-8233-4026-a6c6-0ddc11813f15)

- Jelszint: 50.3dB
- Noise Margin: 19.8
- MER érték: 26.3dB
- Moduláció: DVBT/QPSK/8K/1/32

### Router konfigurálása:  

SSID: furti  
Password: furti12345  
Admin belépés:  
  - Név: admin  
  - Jrlszó: admin12345

IGMP snooping bekapcsolása.   
Bemenetet, kimenetet és a laptop interface-t is IPTV-re állítjuk.  
Bridgeltünk LAN1-ről LAN3-ra közvetlenül IPTV-ről.    
Állítunk rá DHCP szervert, ami 192.168.1.2 tól 192.168.1.249-ig oszt IP-t, alapértelmezett átjáró 192.168.1.1.

## Tesztelések és mérési eredmények:  

A táblázat összegzi a televíziós és rádiós csatornák adatait, a csatornák neveit, azonosítóit, logikai csatorna számát, IP-címét, portját és az adatátviteli protokollt. Ezek az adatok a csatornák jellemzőit és hozzáférhetőségét foglalja össze.  

## MHz sávszélességgel sugároz mindegyik csatorna.
Az alábbi képeken a digitális televíziós vevő (DVB-T) beállítófelülete látható, amely az antennáról leválasztott különböző adók adatait jeleníti meg. A képeken megfigyelhetjük a bemeneteket, frekvenciákat, sávszélességeket, csatornákat, valamint a megjegyzésekben a multiplexált csatornák neveit is.

![409255245-7a88021a-732e-4971-bdd9-9658415c0aa0](https://github.com/user-attachments/assets/8b0256dd-5c45-4caf-b13a-ee488f71f606)
![409257121-e8fbf4ff-7d67-4cd5-9a08-86bfbd1e7a73](https://github.com/user-attachments/assets/0ab563ae-2bbb-400c-b4da-152e8beb6f87)
![409256948-4bae06d4-62bc-4f04-9bca-8dfc6dd3ff38](https://github.com/user-attachments/assets/9ba88e07-4fe0-4558-a745-7a966bdcf54c)
![409257370-a11b38c4-2c78-4c71-8d81-e2cb7f00286d](https://github.com/user-attachments/assets/9d92cdde-c973-467a-bf73-fe9b7493d5bf)




## Hálózati tesztelés és hibakeresés   

Ha a teszt nem indulna el, a Windows hálózati felderítést be kell kapcsolni  







