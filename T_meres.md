
# MÉRÉSI JEGYZŐKÖNYV

**A mérést végző neve:** Szabó Tamás
**A mérés tárgya:** T ellenállás hálózat
**A mérés száma:**  01
**A mérés dátuma:**  2024.11.27 
**A mérést vezette:** Sándor Péter  

**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:**   V3 labor

---

## 1. Mérés célja
A T ellenállás-hálózat jellemzőinek meghatározása 6dB-es csillapításnál.

---

## 2. Eszközök 
- **NI myDAQ** 
- **Ellenállások:**
  - **számolás alapján:**
    - Rg = 1100 Ω
    - R1 = 367 Ω
    - R2 = 1.473 kΩ
  - **méréskor használt:**
    - Rg = 2,2 kΩ X 2,2 Ω
    - R1 = 220 Ω + 120 Ω
    - R2 = 1.5 kΩ
---

## 3. Elmélet
A T pad egy speciális csillapító áramkör az elektronikában, ahol az áramkör topológiája a "T" betű alakjában van kialakítva.

Az elektronikában a csillapítókat a jel szintjének csökkentésére használják. Párnáknak is nevezik őket, mivel az akusztikával analóg módon lepárolják a jelet. A csillapítók lapos frekvenciamenettel rendelkeznek , amely minden frekvenciát egyformán csillapít abban a sávban, amelyen működni kívánnak. A csillapítónak az erősítővel ellentétes feladata van . A csillapító áramkör topológiája általában az egyszerű szűrőszakaszok egyikét követi . A szükséges frekvenciaválasz egyszerűsége miatt azonban nincs szükség bonyolultabb áramkörre, mint a szűrők esetében.

<h3>Az ellenálls értékek számítása:</h3>
<p>Generátor impedancia: 1100 Ω</p>
<p>Csillapítá mértéke: 6 dB</p>

<h3>Az ellenállások értékének képlete:</h3>

![kép](https://github.com/user-attachments/assets/6f1eb4c4-6b68-451b-8bc6-b52f0b87d846)

<h3>Behelyettesítve:</h3>

![kép](https://github.com/user-attachments/assets/08469239-b31b-4f84-a100-24f94ad70c49)

---

## 4. Szimuláció
A T-tagú csillapítás szimulációja megmutatja, hogy a T-tag milyen hatékonyan csökkenti a rezgés amplitúdóját.

<a target="blank" href="https://tinyurl.com/27rgeq6c">

![Névtelen](https://github.com/user-attachments/assets/da1cbba4-0042-4df3-a802-c5ea1a689f10)

</a>

## 5. Gyakorlatban/Számítások

<h3>Mérési eredmények:</h3>

| Paraméter           | Érték |
|---------------------|-------|
| Generátor jel       | 2.002 Vp2p |
| Kimeneti Jel        | 1.062 Vp2p |
| Generátor Frekvencia| 1000 Hz |
| Csillapítás         | -5.507 dB |
| Átviteli Arány      | 5.507 dB |
| Bemeneti impedancia | 2.17 kΩ |
| Kimeneti impedancia | 687 Ω |   

- ***Breadboardon összerakva:***
  A jelgenerátoron 1000Hz-s 2Vpp váltakozó feszültséget állítottunk be.
  CH0 a bemeneti feszülstég CH1 pedig a kimeneti fesz. Szépen látszódik hogy a CH1 feszültsége nagyyábol a fele a CH0-nak.

![Képernyőkép 2024-11-27 131730](https://github.com/user-attachments/assets/019d4817-a12e-40f1-b3f7-9943edb8771d)

![IMG_3206](https://github.com/user-attachments/assets/1eca01f4-fcb8-407b-a809-c1fc802ca057)

**Aláírás:** Pongó Tamás

**Dátum:** 2024.11.27
