---
tags: OE/ALKMAT/Algoelm 
aliases: []
TARGET DECK: 02::algoelm::Bonyolultsági osztályok
---

# feladatok
## 1.
START
Algoelm_Basic
Front:
Mutassuk meg, hogy a MAXKLIKK probléma polinom időben megoldható az olyan $G$ irányítatlan gráfok
esetén, melyekben bármely két különböző pontnak legfeljebb $2*log_2(| V (G) |)$ közös szomszédja van.
Back:
Nézzük végig $G$ minden egyes élére a végpontokat tartalmazó max. klikkek méretét, mégpedig egyszerűen úgy,
hogy megvizsgáljuk a végpontok szomszédainak az összes részhalmazát, hogy klikket alkotnak-e. A feltevés
miatt ezen halmazok száma élenként legfeljebb $2^{2*log_2(|V (G)|)} = |V (G)|^2$ , így összesen $O(|E(G)||V (G)|^ 2 )$ esetet kell
megvizsgálni, és a legkedvezőbbet (a legnagyobbat, ami klikket alkot) kiválasztani.
<!--ID: 1684695939915-->
END

## 2.
START
Algoelm_Basic
Front:
a) Mutassuk meg, hogy a Hamilton-kör keresésének feladata polinom időben megoldható azon irányítatlan gráfok
esetén, amelyeknek legfeljebb $n + 10$ élük van ($n$ a csúcsok száma).
Back:
![[Pasted image 20230521200709.png]]
<!--ID: 1684695939925-->
END

## 3.
START
Algoelm_Basic
Front:
Adjunk $O(n)$ lépésszámú algoritmust (éllistával adott bemeneten) Hamilton-kör megkeresésére polinom időben legfeljebb $n+10$ élen, ahol $n$ a csúcsok száma
Back:
![[Pasted image 20230521200904.png]]
![[Pasted image 20230521200936.png]]
<!--ID: 1684695939930-->
END

## 4.
START
Algoelm_Basic
Front:
Az alábbi $f : N → N$ függvények közül melyek tartoznak $F P$ -be és melyek nem?
$f (n) = n!$
Back:
![[Pasted image 20230521205145.png]]
<!--ID: 1684695939937-->
END

## 5.
START
Algoelm_Basic
Front:
Az alábbi $f : N → N$ függvények közül melyek tartoznak $F P$ -be és melyek nem?
$f (n) =$ az $n$ legkisebb prímosztója
Back:
![[Pasted image 20230521205200.png]]
<!--ID: 1684695939943-->
END

## 6.
START
Algoelm_Basic
Front:
Az alábbi $f : N → N$ függvények közül melyek tartoznak $F P$ -be és melyek nem?
$f (n) = \lfloor log^2(n) \rfloor.$
Back:
![[Pasted image 20230521205223.png]]
<!--ID: 1684695939949-->
END

## 7.
START
Algoelm_Basic
Front:
Jelölje $RH^\prime$ a Részhalmazösszeg feladatnak azt a speciális esetét, amelyben az $s_i$ súlyok mind páros számok.
Karp-redukció megadásával igazoljuk, hogy az $RH^\prime$ feladat $NP$-teljes.
Back:
![[Pasted image 20230521205718.png]]
<!--ID: 1684695939955-->
END

## 8.
START
Algoelm_Basic
Front:
Igazoljuk, hogy polinom időben megoldható a Ládapakolás feladatnak az a speciális esete, amelyben minden súly $\dfrac{1}{2^j}$ alakú.
Back:
![[Pasted image 20230521210005.png]]
![[Pasted image 20230521210019.png]]
<!--ID: 1684695939960-->
END

## 9.
START
Algoelm_Basic
Front:
Igazoljuk, hogy az alábbi L nyelv P -ben van:

$L = \{(v_1 , v_2 , . . . , v_m , b); v_i , b ∈ \mathbb{Z}^+ , v_i ≤ m$ és van olyan $I ⊆ \{1, 2, . . . , m\}$, hogy $i∈I v_i = b\}$.
Back:
![[Pasted image 20230521210442.png]]
<!--ID: 1684695939966-->
END