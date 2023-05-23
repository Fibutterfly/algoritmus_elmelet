---
tags: OE/ALKMAT/Algoelm 
aliases: ["Turing", "Turing gép"]
TARGET DECK: 02::algoelm::Turing
---
# Turing-gép
- Központi rész
	- gép munkája során véges sok lehetséges állapot valamelyikében van
- szalagok
	- cellákra osztva
- minden szalaghoz van író olvasó fej
	- mind2 irányba léphetnek

- működési folyamat
	1. input(ok)ból olvas
	2. központi egység állapota szerint csinál valamit
		- lehet, hogy semmit, lehet, hogy ír
	3. lépteti a fejeket balra, jobba, vagy helyben hagyja
	4. új állapotot vesz fel az egység

# Turing-gép jelölései
- $ad$ a gép belső állapotainak halmaza
- $c*log(n)$ egy állapot
- $ed$ véges halamz, szalagjelek halmaza
- $k$ egy jel a szalagmezőn
- $B$ üresjel
- $A$ inputjelek halmaza

# kérdések
## 1.
START
Algoelm_Basic
Front:
Legyen $f$ és $g$ a teljes $I^∗$-on értelmezett függvénnyel. T.f. $f$ -et kiszámítja $M$ , $g$-t pedig $M^\prime$. készítsünk egy olyan $TG$-t ezen $M$ és $M^\prime$ felhasználásával, ami az $f \circ g$ összetett függvény számítja ki!
Back:
![[Pasted image 20230515163417.png]]
<!--ID: 1684165704883-->
END
## 2.
START
Algoelm_Basic
Front:
rekurzív-e a prímszámokból (pl. bin. ́ábrázolás) álló nyelv?
Back:
Igen, prím teszt
<!--ID: 1684165704891-->
END
## 3.
START
Algoelm_Basic
Front:
Ha $A, B$ két halmaz, akkor a szimmetrikus differenciájuk alatt az $A ⊕ B = (A \backslash B) ∪ (B \backslash A)$ halmazt értjük.
Rekurzív-e $L1 ⊕ L2$, ha $L1$ és $L2$ rekurzív? 
Back:
Igen. Ha $L1, L2$ rekurzív, akkor komplementerük, metszetük, uniójuk is rekurzív, ́így $L1 \backslash L2 = L1 ∩ L2$ is és $L1 ⊕ L2$ is. 
<!--ID: 1684165704896-->
END
## 4.
START
Algoelm_Basic
Front:
Ha $A, B$ két halmaz, akkor a szimmetrikus differenciájuk alatt az $A ⊕ B = (A \backslash B) ∪ (B \backslash A)$ halmazt értjük.
Ha $L1$ és $L2$ két rekurzíve felsorolható nyelv, akkor igaz lesz-e ez $L1 ⊕ L2$-re is?
Back:
Nem. Legyen $L1 = I^∗$és $L2$ egy rekurzíve felsorolható, de nem [[Turing-gép által felismert rekurzív nyelv|rekurzív nyelv]]. Ekkor $L1 ⊕ L2 = L2$, ami nem rekurzíve felsorolható.
<!--ID: 1684165704900-->
END

## 5.
START
Algoelm_Basic
Front:
Legyenek $L1$ és $L2$ rekurzíve felsorolható nyelvek. Igaz-e, hogy $L1 \backslash L2$ (vagyis azon szavak összessége, melyek $L1$-ben vannak, de nincsenek $L2$-ben) rekurzíve felsorolható?
Back:
Nem. Legyen $L1 = I^∗$ és $L2$ egy rekurzíve felsorolható, de nem [[Turing-gép által felismert rekurzív nyelv|rekurzív nyelv]] (pl. $L_h$). Ekkor $L1 \backslash L2 = L2$ nem rekurzíve felsorolható
<!--ID: 1684165704905-->
END

## 6.
START
Algoelm_Basic
Front:
Bizonyítsuk be, hogy: $L1, L2$ rekurzív (rekurzíve felsúrolható) $=⇒ L1 ∪ L2, L1 ∩ L2$  nyelv rekurzív (r.f.).
Back:
![[Pasted image 20230515172750.png]]
<!--ID: 1684165704909-->
END
## 7.
START
Algoelm_Basic
Front:
Bizonyítsuk be, hogy az $L_d$ diagonális nyelv komplementer nyelve rekurzíve felsorolható, azaz $I^∗ \backslash L_d ∈ RE$ !
Back:
![[Pasted image 20230515173607.png]]
<!--ID: 1684165704914-->
END
## 8.
START
Algoelm_Basic
Front:
Igazoljuk, hogy az $L_h$ megállási nyelvnek van végtelen sok szót tartalmazó rekurzív résznyelve!
Back:
Legyen $x ∈ I^∗$ a jegyzetben lévő $n \to n + 1$ függvényt kiszámító TG kódja. Ekkor az $L = {x\#1^n|n ∈ Z^+}$ nyelv rekurzív és $L ⊆ L_h$.
<!--ID: 1684165704919-->
END

## 9.
START
Algoelm_Basic
Front:
Rekurzív-e az azon $x ∈ I^∗$ szavakból álló nyelv, melyekre az $M_x$ Turing-gép létezik, és van olyan $y ∈ I^∗$ szó, hogy $M_x$ az $y$ input esetén 5 lépésen belül megáll?
Back:
![[Pasted image 20230515174155.png]]
<!--ID: 1684165704924-->
END

## 10.
START
Algoelm_Basic
Front:
Legyen $f: {0, 1}^∗ → {0, 1}^∗$ egy függvény, és tegyük fel, hogy a párokból álló ${x\#f(x), x ∈ {0, 1}^∗}$ nyelv rekurzíve felsorolható. Igaz-e, hogy ekkor $f$ egy rekurzív függvény?
Back:
![[Pasted image 20230515174634.png]]
<!--ID: 1684165704928-->
END

## 11.
START
Algoelm_Basic
Front:
![[Pasted image 20230515174809.png]]
Back:
![[Pasted image 20230515174819.png]]
<!--ID: 1684165704933-->
END

## 12.
START
Algoelm_Basic
Front:
Valaki egy $n$ pontú $G = (V, E)$ gráfban $\log^2(n)$ elemű független csúcshalmazt szeretne találni. Azt a meglehetősen egyszerű módszert választja, hogy sorra veszi a $V$ csúcshalmaz $\log^2(n)$ elemű $S$ részhalmazait, és minden ilyen $S$-ről megvizsgálja, hogy független-e. Igaz-e, hogy a részletek megfelelő kidolgozásával ez a módszer polinom idejű algoritmust eredményez?
Back:
Nem. Ugyanis $\left( n \atop \log^2(n) \right)$ lehetőséget vizsgál meg a módszer, tehát legalább ennyi a lépésszám. Ugyanakkor bármely $c$ állandóra $\left( n \atop \log^2(n) \right)/n^c → ∞$. Ez utóbbi állítás például a következő elemi becslés felhasználásával igazolható: $\left( n \atop \log^2(n) \right)= \dfrac{n}{\log^2(n)} \dots \dfrac{n− \log^2(n)+1}{1}  ≥ \left( \dfrac{n− \log^2(n)}{\log^2(n)}\right)^{log^2(n−1)} ≥ n^{\dfrac{1}{2}(log^2(n−1)}$, ha $n$ elegendően nagy.
<!--ID: 1684249429141-->
END

## 13.
START
Algoelm_Basic
Front:
Mutassuk meg, hogy a modulo $m$ tekintett hatványozás elvégezhető polinomidőben
Back:
Az $x^n$ $mod$ $m$ feladat mérete $c(\log(x) + \log(n) + \log(m))$. Az $x^n$ hatványozás elvégezhető polinom sok szorzés segítségével a gyors hatványozás (iterált négyzetre emelés) módszerével: Ha $n = \sum_{k i=0} a_i^{2^i}$ alakú $(k ≤ log_2(n), a_i ∈ \{0, 1\})$, akkor kiszámítva $x^1, x^2,\dots, x^{2^k}ó$ összesen $k$ négyzetre emeléssel, majd azokat az $x^{2^i}$hatványokat (max. $k$ szorzással) összeszorozva, amelyekre $a_i = 1$, megkapjuk $x^n$-et, max. $2k$ szorzás felhasználásával. Mivel a szorzásokat modulo $m$ kell elvégezni, sem a részeredmények, sem a végeredmény mérete nem haladja meg a $2*\log_2(m)$ korlátot. Egy szorzás (két $m$-nél nem nagyobb számnak az összeszorzása és a szorzat maradékos osztása $m$-mel) elvégezhető $\log(m)$-ben polinomidőben.
<!--ID: 1684249429149-->
END

## 14.
START
Algoelm_Basic
Front:
Egy $L ⊆ I^∗$ nyelv esetén az $L^∗$ nyelv definíciója a következő: $L^∗ = \{x ∈ I^∗$; és van olyan $k ≥ 0$egész és $x_1,\dots, x_k ∈ L$ hogy $x = x_1 x_2 \dots x_k\}$.
Igazoljuk, hogy ha $L ∈ N P$ , akkor $L^∗ ∈ N P$ .
Back:
![[Pasted image 20230516163310.png]]
<!--ID: 1684249429155-->
END

## 15.
START
Algoelm_Basic
Front:
Tegyük fel, hogy van egy polinom idejű $M$ eljárásunk, mely a (binárisan ́ábrázolt) $m, n$ pozitív egészekből ́álló bementre megadja $m!(mod \\\ n)$ értékét. Javasoljunk egy polinom idejű $M$-et használó módszert az $n$ prímtényezőinek kiszámítására.
Back:
![[Pasted image 20230516164806.png]]
<!--ID: 1684249429160-->
END

## 16.
START
Algoelm_Basic
Front:
![[Pasted image 20230516170329.png]]
Back:
![[Pasted image 20230516170339.png]]
<!--ID: 1684249429165-->
END

## 17.
START
Algoelm_Basic
Front:
Tegyük fel, hogy van egy $P$ eljárásunk, mely egy input gráfra $1$ költséggel megmondja a gráfban lévő maximális [[klikk]](ek) méretét. Tervezzünk egy olyan, a $P$ eljárást használó algoritmust, mely polinom időben talál egy maximális klikket az input gráfban!
Back:
Vegyük sorra a $G$ gráf $v ∈ V$ csúcsait. Ha a $v$ csúcs és a hozzá illeszkedő élek elhagyásával nyert gráfban a max. klikkméret kisebb, mint az eredeti gráfban (ezt $P$ segítségével állapíthatjuk meg), akkor $v$ a $G$ gráf minden max. méretű klikkjében benne van. Különben hagyjuk el $v$-t, és ismételjük az eljárást. Ha már nincs elhagyható csúcs, kaptunk egy max. méretű klikket. Max. $|V |$ iterációra ( és $P$ -hívásra) van szükség.
![[Turing_17.svg]]
Max $|V|$-szer futhat le
<!--ID: 1684249429170-->
END

## 18.
START
Algoelm_Basic
Front:
Igazoljuk, hogy az alábbi $L$ nyelv $N P$ -ben van: $L = \{f (x) = a_0 + a_1 x + a_2 x^2 + \dots + a_n x^n; a_i ∈ Z$  és az $f (x) = 0$ egyenletnek van egész megoldása $\}$. Megjegyzés: az $a_i$  számokat az inputban binárisan ábrázoljuk.
Back:
![[Pasted image 20230516170153.png]]
<!--ID: 1684249429175-->
END

## 19.
START
Algoelm_Basic
Front:
![[Pasted image 20230516170225.png]]
Back:
![[Pasted image 20230516170239.png]]
<!--ID: 1684249429180-->
END