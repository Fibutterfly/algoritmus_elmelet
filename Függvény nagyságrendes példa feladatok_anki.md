---
TARGET DECK: 02::algoelm::függvények_nagyságrendje
---
START
Algoelm_Basic
Front:
Mit jelent függvények nagyságrendjében a O?
Back:
Mindig azt keressük, hogy ha az $n$ növekszik melyik az a $c$, amire igaz, hogy $f(n) \le c*g(n)$ (melyik az a $c$)
Mindig azt keressük, hogy ha az $n$ növekszik melyik az a $c$, amire igaz, hogy $f(n) \ge c*g(n)$ (melyik az a $c$)
Ha $O$ és $\Omega$ is létezik akkor ez is (főleg ha találunk közös $c$-t)
ha $f=c*g$ akkor $f = \Theta(g)$
<!--ID: 1678660032965-->
END

START
Algoelm_Basic
Front:
Mit jelent függvények nagyságrendjében a $\Omega$?
Back:
Mindig azt keressük, hogy ha az $n$ növekszik melyik az a $c$, amire igaz, hogy $f(n) \le c*g(n)$ (melyik az a $c$)
Mindig azt keressük, hogy ha az $n$ növekszik melyik az a $c$, amire igaz, hogy $f(n) \ge c*g(n)$ (melyik az a $c$)
Ha $O$ és $\Omega$ is létezik akkor ez is (főleg ha találunk közös $c$-t)
ha $f=c*g$ akkor $f = \Theta(g)$
<!--ID: 1678660032974-->
END

START
Algoelm_Basic
Front:
Mit jelent függvények nagyságrendjében a $\Theta$?
Back:
Mindig azt keressük, hogy ha az $n$ növekszik melyik az a $c$, amire igaz, hogy $f(n) \le c*g(n)$ (melyik az a $c$)
Mindig azt keressük, hogy ha az $n$ növekszik melyik az a $c$, amire igaz, hogy $f(n) \ge c*g(n)$ (melyik az a $c$)
Ha $O$ és $\Omega$ is létezik akkor ez is (főleg ha találunk közös $c$-t)
ha $f=c*g$ akkor $f = \Theta(g)$
<!--ID: 1678660032981-->
END

START
Algoelm_Basic
Front:
Legyen f (n) = 3n + 1000 és g(n) = n . O $\Omega$ $\Theta$ ?
Back:
- TFH $n_0 = 1000$
- ekkor $f (n) = 3n + 1000 ≤ 4n = cn$
- TFH $n \ge 1$ 
- akkor látjuk, hogy $c \ge 3$
- $3n + 1000 ≥ 3n = cn$ 
- $f = Θ(g)$ igaz, mert $f = O(g)$ és $f = Ω(g)$
<!--ID: 1678660032989-->
END

START
Algoelm_Basic
Front:
Legyen f (n) = 3n + 1000 és g(n) = $n^2$ . O $\Omega$ $\Theta$ ?
Back:
- legyen $n_0$ =1000
- Itt nem nagyon tudunk következtetést levonni közvetlenül, így úgy csináljuk, hogy
- $f (n) = 3n + 1000 \le c*n$
- $c \ge 4$
- és ebből jön az, hogy $4*n \le c*n^2$
- $\dfrac{4}{n} \le c$ -től kezdve ez teljesül
- legyen $n_0$ =1000
- Itt nem nagyon tudunk következtetést levonni közvetlenül, így úgy csináljuk, hogy
- $f (n) = 3n + 1000 \ge c*n$
- $c \le 4$
- és ebből jön az, hogy $4*n \ge c*n^2$
- $\dfrac{4}{n} \ge c$ -ig teljesül, tehát nem igaz
- $f = O(g)$, de $f \ne \Omega(g)$ így $f \ne \Theta(g)$
<!--ID: 1678660032997-->
END

START
Algoelm_Basic
Front:
$f (n) = 3n^2 − 100n + 6$
$f (n) = O(n^3)$?
Back:
- mivel nincs $n^3$ tag az $f$-ben így indirekt módon tudjuk csak keresni
- kérdés valójában: $3n^2-100n+6 \le c*n^2 \le d*n^3$ (melyik az a $c$)
- megkeressük a baloldal lokminimumát $6*n-100 = 0 \rightarrow n \ge 16$ szigmonnő a függvény értéke 34 körül 0 (másodfokú)
- $c = 3$ $n_0 = 34$ párostól biztosan igaz
- $3*n^2 \le d*n^3$ és $n \ge 34$
- behelyettesítünk és látjuk, hogy már $d=1$-től teljesül
<!--ID: 1678660033004-->
END

START
Algoelm_Basic
Front:
$f (n) = 3n^2 − 100n + 6$
$f(n) = O(n)$?
Back:
- ránézésre nem valószínű, mert van benne nagyobb kitevőjű
- kérdés valójában: $3n^2-100n+6 \le c*n$ (melyik az a $c$)
- ezt úgy tudjuk megtalálni, hogy megmondjuk minél biztosan kisebb, ami
- kérdés valójában: $3n^2-100n+6 \le c*n^2$ (melyik az a $c$)
- $c = 3$ $n_0 = 34$ párostól biztosan igaz
- vesszük a $c$-t és elveszünk belőle egyet és felteszünk egy új kérdést
- $2n^2 > c*n$? viszont erre azt kapjuk, hogy $n > \cfrac{c}{2}$ amíg igaz ez az állítás így $f(n) \ne O(n)$ 
<!--ID: 1678660033011-->
END

START
Algoelm_Basic
Front:
$f (n) = 3n^2 − 100n + 6$
$f (n) = Θ(n^2)$?
Back:
- $f (n) = O(n^2)$?
	- kérdés valójában: $3n^2-100n+6 \le c*n^2$ (melyik az a $c$)
	- megkeressük a baloldal lokminimumát $6*n-100 = 0 \rightarrow n \ge 16$ szigmonnő a függvény értéke 34 körül 0 (másodfokú)
	- $c = 3$ $n_0 = 34$ párostól biztosan igaz
- $f (n) = \Omega(n^2)$?
	- kérdés valójában: $3n^2-100n+6 \ge c*n^2$ (melyik az a $c$)
	- megkeressük a baloldal lokminimumát $6*n-100 = 0 \rightarrow n \ge 16$ szigmonnő a függvény értéke 34 körül 0 (másodfokú)
	- előbb láttuk, hogy kell hozzá legalább $c=3$ hogy felülről közelíthető legyen, akkor vegyünk el belőle 1-et $c=2$ ekkor az $n$-nek legalább $100$-nak kell lennie, de teljesül
- $f(n)=\Theta(n^2)$ igaz
<!--ID: 1678660033018-->
END

START
Algoelm_Basic
Front:
$\log_a( n )= Θ(\log_2( n))$?
Back:
- [[logaritmus összefüggések#logaritmus alap váltás|logaritmikus alapváltást felhasználva]] $\cfrac{1}{\log_2(a)} * \log_2(n)$ 
- mivel $f = c*g$ az igaz, ezért $\log_a(n) = \Theta(log_2(n))$ is
<!--ID: 1678660033025-->
END

START
Algoelm_Basic
Front:
$2^{2n} = O(2^n)$
Back:
- a kérdés valójában $2^{2*n} \le c*2^n$
- $2^n \le c$ marad, összefüggésben van az $n$-nel így nem lesz jó
<!--ID: 1678660033032-->
END

START
Algoelm_Basic
Front:
$max(f (n), g(n)) = Θ(f (n) + g(n))$
Back:
- ez 1 szivatás, azt kell tudni, hogy számtani közép mindig $\ge$ egész
- $max(f,g) \ge c*f+c*g \rightarrow c=\dfrac{1}{2}$ ($\Omega$ oldal)
- $max(f,g) \le c*f+c*g$ ez akár $1$-el is igaz ($O$ oldal)
- $\Omega$ és $O$ is igaz, így $\Theta$ is az
<!--ID: 1678660033040-->
END
