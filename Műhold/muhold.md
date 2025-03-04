# MÉRÉSI JEGYZŐKÖNYV   
# Méréstechnikai Feladat: Műhold

**A mérést végző neve:** Pongó Tamás  
**A mérés tárgya:**  Műholdas vételi rendszer kiépítése     
**A mérés száma:** 03. mérés    
**A mérés dátuma:** 2025. 03. 04.    
**A mérést vezette:** Sándor Péter    

**Évfolyam:** 13. E  
**Csoport:** GYAK 1   
**Helyszín:** V3 Labor, kisudvar    

## Feladat célja   
Egy szabadon fogható (FTA) csatorna véletének beállítása, műholdas vételi rendszer kiépítése és vizsgálata, majd optimális vételi jel csatlakoztatása egy set op boxba, amin keresztül képet jelenítünk meg.  

## Felhasznált eszközök   
- Parabolaantenna: D80 Mesh 
- Műholdvevő fej (LNB):Ekselans SATCR LNB
- Set-top box: Amiko HD 8265+
- METEK HDD jelmérő
- Koaxiális kábelek és csatlakozók
- 2-es műholdas jelosztó
- Szerelési eszközök: csavarhúzó, villáskulcs, iránytű, dőlésszögmérő

## Feladat menete  
Először összeszereltem az antennát, majd rákötöttem az általam választott LNB fejegységet (Ekselans SATCR). Az internetes műholdvevő adatbázisból (lyngsat.com) kiválasztottam a FTA csatornákat, és egy olyan adót választottam, amely az Eutelsat 9B műholdról sugároz. Iránytű segítségével beállítottam az antenna dőlésszögét és polarizációját, majd a METEK HDD eszközzel megpróbáltam a lehető legjobb jelet megtalálni. Végül az optimális beállítások a következőképpen alakultak: a tetőponti (azimuth) szög 198°, az emelkedési (elevation) szög 36°, és az LNB skew (elforgatási) szög 10° lett. Ezután összekötöttem az LNB vevőfejet a set-top boxszal, majd csatlakoztattam a set-top boxot egy monitorhoz. Beállítottam a megfelelő régiót, országot, és elindítottam az automatikus csatornakeresést.

## METEK HDD képek és jelszintmérés  

Az alábbi kép a spektrumanalizátoron lévő műholdas jelszint kijelzőjét mutatja.   

![image](https://github.com/user-attachments/assets/37097f97-6894-45c8-957a-eb51d4acb0b9)   

Fontosabb információk: 
 - MER (Modulation Error Ratio) érték : 11.9 dB (közepes)   
 - A vizsgált frekvencia 1358.0 MHz.
 - A műhold: Eutelsat 9A (9B-vel megegyező csatornakiosztásai vannak)
 - A beesések interferenciára is utalhatnak
 - Jelszint: 83.2 dBuV (egész erős jel)

A következő képen pedig láthatóak a csatornainformációk.    

![image](https://github.com/user-attachments/assets/01450615-d799-4418-81a3-4d7ad422f031)  

- Csatorna neve: M1 HD.
- Service ID: 101
- Network ID: 158
- ONID (Original Network ID) érték: 106
- Felbontás: 1920 × 1080 (Full HD)
- VPID (Video PID) és bitráta: 1101 / 3.989220 Mb/s (H.264 tömörítés)
- APID (Audio PID) és bitráta: 1201 / 0.415802 Mb/s (AC3 hangformátum)


## Hibakeresés  
Nem jelent meg kép, kiderült, hogy a hiba a rossz UTP kábelből adódott. Beállítottuk a spektrumanalizátort a Hot Bird 13 műholdra, az antennát pedig a megfelelő szögbe állítottuk, majd finomhangoltuk. Bár 80 dBuV jelet kaptunk, mégsem jelent meg a kép. Végül, amikor új szoftverrel és másik kábellel próbálkoztunk, sikerült elérni a megfelelő jelet.
