
# Miskolci Szakképzési Centrum  
**Kandó Kálmán Informatikai Technikum**  
**Miskolc Palóczy u. 3.**

# MÉRÉSI JEGYZŐKÖNYV

**A mérést végző neve:** Pongó Tamás  
**A mérés tárgya:** Frekvencia vs. moduláció mérés


**A mérés száma:** 4. mérés  
**A mérés dátuma:** 2024. 11. 20  
**A mérést vezette:** Sándor Péter  

**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:** V3 Labor 

---

# Mérési Jegyzőkönyv

## 1. Mérés Célja
A mérés célja a **Johansson 8202 DVB-T modulátor** működésének megismerése, konfigurációjának tesztelése, valamint a METEK HD spektrum- és jelszintanalizátor használatával a modulátor által generált jel paramétereinek mérése. A mért paraméterek: **jelszint**, **bitsebesség**, **MER (Modulation Error Rate)**.

---

## 2. Használt Eszközök

| Eszköz                     | Típus                       | Funkció                                           |
|----------------------------|-----------------------------|---------------------------------------------------|
| Johansson 8202             | DVB-T modulátor            | Bitsebesség és jelminőség vizsgálata              |
| RF kábel                   | Koaxiális kábel            | Modulátorok és spektrumanalizátor összekötése     |
| Metek HDD                  | Spektrum/jelszint analizátor| Frekvencia, moduláció, sávszélesség, jelszint, MER és bitsebesség mérése |

---

## 3. Beállítások
- **Frekvencia**: 490 MHz  
- **Sávszélesség**: 8 MHz  
- **Modulációs típusok tesztelése**:  
  - QPSK  
  - 16QAM  
  - 64QAM  

---

## 4. Mérési Eredmények
Az alábbi táblázatban összefoglaljuk a mérések eredményeit különböző modulációs beállítások mellett.

| **Moduláció** | **Jelszint [dBm]** | **Bitsebesség [Mbps]** | **MER [dB]** |
|---------------|---------------------|------------------------|--------------|
| QPSK          | -30.3 dBm          | 3.5 - 4.2 Mbps        | 39.9 dB      |
| 16QAM         | -30.1 dBm          | 8.0 - 10.2 Mbps       | 35.8 dB      |
| 64QAM         | -30.5 dBm          | 13.0 - 15.8 Mbps      | 40.0 dB      |

---

## 5. Lépések
1. **Modulátor konfigurációja**:
   - A Johansson 8202 DVB-T modulátoron beállítottuk a kívánt frekvenciát (490 MHz) és a sávszélességet (8 MHz).  
   - A modulációs típusokat egyesével módosítottuk: QPSK, 16QAM, 64QAM.

2. **Jel vizsgálata METEK HD analizátorral**:
   - Az RF kábellel csatlakoztattuk a METEK HD spektrum/jelszint analizátort a modulátor kimenetéhez.  
   - Minden egyes modulációs típus esetén elvégeztük a jelszint, bitsebesség és MER mérést.  

---

## 6. Következtetések
- A mérés során megfigyelhető volt, hogy a moduláció típusának növelésével (QPSK → 64QAM) a bitsebesség jelentősen nőtt, miközben a **MER érték** változásai nem mutattak egyértelmű tendenciát.  
- A mérések a DVB-T elméleti követelményeinek megfelelő eredményeket adtak.

---

## 7. Megjegyzések
- A méréseket stabil környezeti feltételek mellett végeztük, zavarforrásoktól mentes helyiségben.  
- Az adatok alapján a különböző modulációs technikák közötti különbségek jól megfigyelhetőek voltak.

---

## 8. További Mérési Javaslatok

<details>   

<summary>Kattins a részletekért</summary>   

<h1>Mérési Javaslatok</h1>

    <h2>1. Szélsőséges Jelszint Tesztelése</h2>
    <ul>
        <li><strong>Cél:</strong> Vizsgálni, hogyan viselkedik a rendszer különböző jelszint értékek mellett.</li>
        <li><strong>Lépések:</strong>
            <ol>
                <li>Állítsuk be a jelszintet az RF kimeneten szélsőségesen alacsony és magas értékekre (pl. -60 dBm, -20 dBm).</li>
                <li>Mérjük meg a bitsebességet és a MER-t a kiválasztott modulációs típusok mellett.</li>
            </ol>
        </li>
        <li><strong>Elvárt eredmények:</strong> Magasabb jelszintnél stabilabb adatátvitel, alacsonyabb jelszintnél romló MER és csökkenő bitsebesség.</li>
    </ul>

    <hr>

    <h2>2. Szűkebb és Szélesebb Sávszélesség Hatásai</h2>
    <ul>
        <li><strong>Cél:</strong> Megvizsgálni a sávszélesség változtatásának hatását a jel minőségére és teljesítményére.</li>
        <li><strong>Lépések:</strong>
            <ol>
                <li>Állítsuk be a sávszélességet különböző értékekre (pl. 6 MHz, 7 MHz, 8 MHz).</li>
                <li>Rögzítsük a jelszintet, MER-t és a bitsebességet.</li>
            </ol>
        </li>
        <li><strong>Elvárt eredmények:</strong> Szélesebb sávszélességnél nagyobb bitsebesség, de csökkenhet a MER.</li>
    </ul>

    <hr>

    <h2>3. Zavarforrások Hatása</h2>
    <ul>
        <li><strong>Cél:</strong> Meghatározni, hogy a közeli rádiófrekvenciás zavarok hogyan befolyásolják a jelek minőségét.</li>
        <li><strong>Lépések:</strong>
            <ol>
                <li>Helyezzünk egy zavarforrást (pl. másik RF jeladó) a vizsgált frekvencia közelébe.</li>
                <li>Mérjük meg a jelszintet, MER-t és a bitsebességet különböző távolságokból.</li>
            </ol>
        </li>
        <li><strong>Elvárt eredmények:</strong> Zavarforrás jelenléte csökkentheti a MER-t és növelheti a hibaarányt.</li>
    </ul>

    <hr>

    <h2>4. Moduláció Stabilitásának Vizsgálata Időfüggvényében</h2>
    <ul>
        <li><strong>Cél:</strong> Tesztelni, hogy hosszabb időtartam alatt mennyire stabil a jel különböző modulációs típusok esetén.</li>
        <li><strong>Lépések:</strong>
            <ol>
                <li>Állítsuk be az eszközt egy modulációs típusra (pl. 64QAM).</li>
                <li>Mérjünk jelszintet, MER-t és bitsebességet óránként legalább 12 órán keresztül.</li>
            </ol>
        </li>
        <li><strong>Elvárt eredmények:</strong> Stabil rendszer esetén a paramétereknek változatlannak kell maradniuk.</li>
    </ul>

    <hr>

    <h2>5. Szomszédos Csatornák Vizsgálata</h2>
    <ul>
        <li><strong>Cél:</strong> Megérteni, hogyan befolyásolja a szomszédos csatornák jelenléte a méréseket.</li>
        <li><strong>Lépések:</strong>
            <ol>
                <li>Aktiváljunk egy szomszédos csatornán (pl. 482 MHz vagy 498 MHz) másik DVB-T jelet.</li>
                <li>Mérjük meg a főcsatorna (490 MHz) paramétereit.</li>
            </ol>
        </li>
        <li><strong>Elvárt eredmények:</strong> Növekvő interferencia esetén csökkenhet a MER és romolhat a jel minősége.</li>
    </ul>

    <hr>

    <h2>6. Jelkésleltetés Vizsgálata</h2>
    <ul>
        <li><strong>Cél:</strong> Ellenőrizni a rendszer válaszidejét különböző beállítások mellett.</li>
        <li><strong>Lépések:</strong>
            <ol>
                <li>Állítsunk be eltérő modulációkat és sávszélességeket.</li>
                <li>Mérjük meg a jelkésleltetést (pl. speciális analizátorral vagy műszerekkel).</li>
            </ol>
        </li>
        <li><strong>Elvárt eredmények:</strong> A sávszélesség és moduláció változtatása hatással lehet a késleltetésre.</li>
    </ul>

    <hr>

    <h2>7. Hőmérséklet Hatásának Vizsgálata</h2>
    <ul>
        <li><strong>Cél:</strong> Megérteni, hogyan befolyásolja a környezeti hőmérséklet a rendszer teljesítményét.</li>
        <li><strong>Lépések:</strong>
            <ol>
                <li>Végezze el a méréseket különböző hőmérsékleteken (pl. 0°C, 25°C, 30°C).</li>
                <li>Rögzítse a jelszint, MER és bitsebesség értékeket.</li>
            </ol>
        </li>
        <li><strong>Elvárt eredmények:</strong> Szélsőséges hőmérsékleteken csökkenhet a rendszer stabilitása.</li>
    </ul>  

</details>

<br>

---

## 9. Diagramm
- Mérési jegyzőkönyv grafikon: 
![diagram](https://github.com/user-attachments/assets/4998637f-514c-4694-a393-6de12c99c446)


---

## 10. Záró Összegzés


---

## 11. Mért Képek

<details>
<summary>Kattins a részletekért</summary>

<br>

<img src="https://erosbence27.github.io/jegyzokonyv/image/munkakep1.jpg"/>

<br>

<img src="https://erosbence27.github.io/jegyzokonyv/image/frekik.bmp"/>

<br>

<img src="https://erosbence27.github.io/jegyzokonyv/image/qpsk_meter.bmp"/>

<br>

<img src="https://erosbence27.github.io/jegyzokonyv/image/qpsk_bit.bmp"/>

<br>

<img src="https://erosbence27.github.io/jegyzokonyv/image/16qam_meter.bmp"/>

<br>

<img src="https://erosbence27.github.io/jegyzokonyv/image/16qam_bit.bmp"/>

<br>

<img src="https://erosbence27.github.io/jegyzokonyv/image/64qam_meter.bmp"/>

<br>

<img src="https://erosbence27.github.io/jegyzokonyv/image/64qam_bit.bmp"/>

<br>

</details>

**Aláírás:** Pongó Tamás

**Dátum:** 2024. 11. 20.

