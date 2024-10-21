# Miskolci Szakképzési Centrum 
## Kandó Kálmán Informatikai Technikum
Miskolc, Palóczy u. 3.

# MÉRÉSI JEGYZŐKÖNYV

**A mérést végző neve**: Pongó Tamás  
**A mérés tárgya**: Föld felszíni televíziós vétel kialakítása  
**A mérés száma**: 02  
**A mérés dátuma**: 2024. 09. 25.  
**A mérést vezette**: Sándor Péter  

## Alkalmazott mérőeszközök és készülékek

| Műszer neve         | Típus         | Gyártási szám    | Képek         |
|---------------------|---------------|------------------|---------------|
| DVB-T Modulátor     | 8202          | H160865877       |               |
| Antenna Iskra       | P-20          | 3831002931507    |               |
| Antenna Ikusi FlasHD | HDTF-C48V     | 18180522         |               |
| Nytro Boksz Plis set | top box T2/C  | 220100821        |               |

## Kapcsolási vázlat rajz

(*Insert diagram here*)

## A mérés menete és célja

1. Az antenna összeszerelése  
2. Bekábelezés a tápvonal kiépítése  
3. A legerősebb jelszint beállítása a vételi ponton  
4. Nyugat 255: 53 dBuV al jön az adás (avasi kilátó)  
   665 dBuV al jön az adás (Tokaji adó)  
5. ---  
6. Felszereltük, telepítettük a P20-as antennát és beállítottuk egy szabad csatornára (38Ch, 618Mhz)  
7. Ráirányítottuk az adó antennát a vevő antennára, ami házon belül van, kb. 18-20m távolságra  
8. Az adó teljesítmény 99dBuV, és ezt vesszük a házon belül a vevő antennán (52 dBuV)  
9. Az Nytro Set top-boksz programozása  

## 38 csatorna 610Mhz

### Adattáblázatok

(*Insert data tables here*)

### Számítások

#### Adatok

- Ut = 9V  
- I = 5mA = 0.005A  
- UL1 = UL2 = 1.8V  
- R1 = ?  
- R2 = ?  

#### Számítások

- Re = R1 + R2 = ?  
- UL12 = UL1 + UL2 = 1.8V + 1.8V = 3.6V  
- URe = Ut – UL12 = 9V – 3.6V = 5.4V  
- Re = URe / I = 5.4V / 0.005A = 1080Ω  

Két értékből lehetett választani: 510Ω és 1000Ω  
Az 1080Ω érték előállítása két darab 510Ω ellenállás soros kapcsolásából hozható létre:  
Re = 510Ω + 510Ω = 1020Ω  

## Értékelés, észrevétel, megjegyzés
