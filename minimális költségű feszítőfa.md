---
tags: OE/ALKMAT/Algoelm 
aliases: ["maximális költségű feszítőfa"]
TARGET DECK: 02::algoelm::spanning tree
---

# minimális költségű feszítőfa
$G$-nek az a feszítőfája, amelynek az $a_i$ súlyok által értelmezett legkisebb költségű.
- $G=(V,E)$ [[összefüggő gráf]]
- feszítőfa az összefüggő
- $a_{ij} \in \mathbb{R}$ és $1 \leq i,j \leq |V|$ az élek súlyai 
- $V$ csúcsok halmaza
- $E$ élek halmaza

#Rónyai/Algoritmusok

# Kérdések
## 1.
START
Algoelm_Basic
Front:
Módosítsuk a Kruskalt úgy, hogy a maximális súlyú feszítőfát kapjuk meg.
Back:
Mindig a maximális súlyú élt vesszük ki
<!--ID: 1684155555153-->
END

## 2.
START
Algoelm_Basic
Front:
G hurok mentes összefüggő súlyozott gráf.
TFH $e_i \ne e_j \Rightarrow w(e_i) \ne w(e_j) \forall e_i,e_j$
Bizonyítsd be, hogy pontosan egy feszítőfája van
Back:
Mivel mindegyik különböző a feladat szerint, ezért Kruskal esetén mindig tudjuk, hogy az [[algoritmus]] mit fog választani
<!--ID: 1684155555158-->
END

