<!--
author:   Marco Hamann

email:    marco.hamann@htw-dresden.de

version:  0.0.1

language: de

comment:  Dieser Kurs richtet sich an Studierende der Hochschule für Technik und Wirtschaft Dresden im Studiengang Fahrzeugtechnik im 3. Semester.

script:   https://cdn.rawgit.com/davidedc/Algebrite/master/dist/algebrite.bundle-for-browser.js
@Algebrite.eval: <script> Algebrite.run(`@input`)</script>
-->


# Mathematik 3 (I959)

Dieser Kurs richtet sich an Studierende der Hochschule für Technik und Wirtschaft Dresden im Studiengang Fahrzeugtechnik im 3. Semester.

Sie können diesen Kurs auf [LiaScript](https://liascript.github.io/course/?https://github.com/marco-hamann/Mathe3/blob/main/README.md) oder [Opal](https://bildungsportal.sachsen.de/opal/auth/RepositoryEntry/16648798212) aufrufen. Das Repository zu diesem Kurs finden Sie unter

https://github.com/marco-hamann/Mathe3


## Funktionsreihen

Thema dieses Kapitels sind die Funktionsreihen für reelle Funktionen einer reellen Variablen. Speziell werden Potenzreihen und Fourierreihen eingeführt und untersucht.

~~Zentrale Fragen~~ sind dabei die folgenden:

1. Vertiefung von Zahlenfolgen und **Zahlenreihen**. Dies umfasst u. a. die Konvergenz und Divergenz von Zahlenfolgen, den Grenzwert einer konvergenten Zahlenfolge, Partialsummen für Zahlenfolgen und Partialsummenfolgen (Zahlenreihen), den Summenwert einer konvergenten Zahlenreihe sowie Konvergenzkriterien für Zahlenreihen und Eigenschaften konvergenter Zahlenreihen

2. Übertragung auf Funktionenfolgen und **Funktionenreihen**. Dies umfasst u. a. unendliche Folgen von reellen Funktionen einer reellen Veränderlichen über demselben Definitionsbereich (Funktionenfolge), den Konvergenzbereich einer Funktionenfolge und Grenzfunktion einer Funktionenfolge, gleichmäßige bzw. punktweise Konvergenz, Partialsummen für Funktionenfolgen und Partialsummenfolgen einer Funktionenfolge (Funktionenreihen) sowie die Summenfunktion der konvergenten Funktionenreihe
3. Untersuchung von **Potenzreihen** als speziellen Funktionenreihen, deren Eigenschaften, die Taylor-Entwicklung von reellen Funktionen von einer bzw. zwei reellen Veränderlichen zur Entwicklung einer Potenzreihe
4. Untersuchung von **Fourier-Reihen** zu periodischen Funktionen, Satz von Dirichlet, Entwicklung einer Fourier-Reihe zu einer gegebenen Funktion


### Zahlenfolgen und Reihen

Zahlenfolgen
============


In diesem Abschnitt werden grundlegende Begriffe wie Zahlenfolge, Zahlenreihe und Konvergenz wiederholt.

> Eine reelle **Zahlenfolge** ist eine Funktion der Form $f:\mathbb{N}\to\mathbb{R}$ mit
>$$
  f:k\mapsto y=f(k)=a_k
$$ worin $a_k$ $k-$tes Glied der Zahlenfolge genannt wird. Besitzt $f$ endlich viele (natürliche) Argumente, so heißt $f$ *endliche* Zahlenfolge, für unendlich viele Argumente *unendliche* Zahlenfolge.

**Bemerkung.** Reelle Zahlenfolgen lassen sich oftmals darstellen

1. in Form einer *Wertetabelle*. Die eindeutige Zuordnung der reellen Glieder $a_k$  zu den natürlichen Argumenten $k$ ist in den Spalten der nachfolgenden Tabelle formal dargestellt.  
| $k$ | $0$ | $1$ | $2$ | $...$ |
| :----- | :----- | :----- | :----- | :----- |
| $a_k$ | $a_0$ | $a_1$ | $a_2$ | $...$ |
2. als nach den natürlich geordneten Argumenten zugeordnete *Liste* der Zahlenfolgenglieder, beispielsweise
$$
  \left(a_k\right)_{k=0}^\infty=a_0,a_1,a_2,...
$$

> Eine unendliche reelle Zahlenfolge $(a_k)_{k=0}^\infty$ heißt *konvergent* gegen den Grenzwert $g\in\mathbb{R}$, $\lim_{k\to\infty}{a_k}=g$, falls ein $\epsilon>0$ existiert, dass ab einem hinreichend großem $n\in\mathbb{N}$ gilt
>$$
  |a_k-g|<\epsilon \quad\forall\; k>n
$$ Andernfalls heißt $(a_k)_{k=0}^\infty$ *divergent*.


Zahlenreihen
============


>Werden nun die Teilsummen von Gliedern der Zahlenfolge $(a_k)_{k=0}^\infty$ gebildet gemäß
>$$
  s_0=a_0\,,\quad s_1=s_0+a_1=a_0+a_1\,,\quad s_2=s_1+a_2=a_0+a_1+a_2\,, ...
$$ beziehungsweise allgemein für die $n$-te Teilsumme
>$$
  s_n=\sum_{k=0}^n{a_k}\,,\quad n\in\mathbb{N}
$$ so bildet die Zuordnung $n\mapsto s_n$, $n\in\mathbb{N}$, wieder eine unendliche Folge, die Partial-, Teilsummenfolge beziehungsweise **unendliche Zahlenreihe** $(s_n)_{n=0}^\infty$ von $(a_k)_{k=0}^\infty$ genannt wird.

Eine alternative Schreibweise für die Zahlenreihe $(s_n)_{n=0}^\infty$ zur Zahlenfolge $(a_k)_{k=0}^\infty$ ist
$$
  \sum_{k=0}^\infty{a_k}
$$ worin die Bezugnahme zur Zahlenfolge aufgezeigt ist.

Die Zahlenreihe $(s_n)_{n=0}^\infty$ zur Zahlenfolge $(a_k)_{k=0}^\infty$ heißt *konvergent* gegen den Grenzwert $w\in\mathbb{R}$, $\lim_{n\to\infty}{s_n}=w$, falls ein $\epsilon>0$ existiert, dass ab einem hinreichend großem $m\in\mathbb{N}$ gilt
$$
  |s_n-w|<\epsilon \quad\forall\; n>m
$$ Andernfalls heißt $(s_n)_{n=0}^\infty$ *divergent*.

**Beispiel 1.** Betrachtet wird die geometrische Zahlenfolge $$
  (a_k)_{k=0}^\infty=\left(\frac{1}{2^k}\right)_{k=0}^\infty=1,\frac{1}{2},\frac{1}{4},\frac{1}{8},...
$$ Für die Glieder dieser Zahlenfolge gilt $$
  \frac{a_{k+1}}{a_k}=\frac{1}{2}
$$ für alle Argumente $k$. Die Zahlenfolge ist konvergent mit Grenzwert $$
  \lim_{k\to\infty}{a_k}=0
$$

Für die Partialsummenfolge von $(a_k)_{k=0}^\infty$ gilt $$
  s_0=a_0=1\,,\quad
  s_1=a_0+a_1=1+\frac{1}{2}=\frac{3}{2}\,,\quad s_2=a_0+a_1+a_2=1+\frac{1}{2}+\frac{1}{4}=\frac{7}{4}\,,\quad ...
$$ beziehungsweise für das allgemeine Glied $$
  s_n=\sum_{k=0}^n{a_k}=a_0+a_1+a_2+...+a_n=1+\frac{1}{2}+\frac{1}{4}+...+\frac{1}{2^n}
$$ Die Konvergenz der Partialsummenfolge $$
  (s_n)_{n=0}^\infty=1,\frac{3}{2},\frac{7}{4},...
$$ folgt unter Benutzung der Summenformel für geometrische Reihen $$
  s_n-\frac{1}{2}\cdot s_n=\left(1+\frac{1}{2}+\frac{1}{4}+...+\frac{1}{2^n}\right)-\frac{1}{2}\cdot\left(1+\frac{1}{2}+\frac{1}{4}+...+\frac{1}{2^n}\right)=1-\frac{1}{2^{n+1}}\quad\leftrightarrow\quad s_n=2-\frac{1}{2^n}
$$ und schließlich $$
  \lim_{n\to\infty}{s_n}=2
$$ Graphisch geometrisch lässt sich der Grenzwert auch aus nachstehender Abbildung ermitteln. Hierfür sind die Längen der Strecken (blau) in Richtung der $x$-Achse beziehungsweise der $y$-Achse zu addieren.

![Geometrische Reihe](img/mat-bild-01.png "_Fig._ Achsenparalleles Zick-zack Polygon 'zwischen' zwei Geraden mit den Gleichungen $y=x$ und $y=1+\frac{1}{2}\cdot x$. Die Streckenlängen in $x$- bzw. in $y$-Richtung bilden die Summe $1+\frac{1}{2}+\frac{1}{4}+\frac{1}{8}+...$.")

**Beispiel 2.** Ganz ähnlich lässt sich der Grenzwert der alternierenden geometrischen Zahlenreihe $$
  \sum_{k=0}^\infty{\left((-1)^k\cdot\frac{1}{2^k}\right)}=1-\frac{1}{2}+\frac{1}{4}-\frac{1}{8}\pm ...
$$ bestimmen. Mit der Summenformel für geometrische Reihen folgt analog zu Beispiel 1 $$
  \lim_{n\to\infty}{\sum_{k=0}^n{\left((-1)^k\cdot\frac{1}{2^k}\right)}}=
  \lim_{n\to\infty}{\left(\frac{1-\left(-\frac{1}{2}\right)^{n+1}}{1-\left(-\frac{1}{2}\right)}\right)}=\frac{2}{3}
$$ Graphisch geometrisch lässt sich der Grenzwert auch aus nachstehender Abbildung ermitteln. Hierfür sind die Längen der Strecken (blau) in Richtung der $x$-Achse beziehungsweise der $y$-Achse des 'zwischen' beiden Geraden mit den Gleichungen $y=x$ und $y=1-\frac{1}{2}\cdot x$ erzeugten, achsenparallelen, spiralförmigen Polygons zu addieren / subtrahieren.

![Geometrische Reihe2](img/mat-bild-02.png "_Fig._ Achsenparalleles spiralförmiges  Polygon 'zwischen' zwei Geraden mit den Gleichungen $y=x$ und $y=1-\frac{1}{2}\cdot x$. Die orientierten Streckenlängen in $x$- bzw. in $y$-Richtung bilden die alternierende Summe $1-\frac{1}{2}+\frac{1}{4}-\frac{1}{8}\pm...$.")

**Bemerkung 1.** Eine geometrische Zahlenreihe $$
  \sum_{k=0}^\infty{\left(a\cdot r^k\right)}\,,\quad a\in\mathbb{R}\setminus\{0\}
$$ konvergiert dann, wenn $\left|r\right|\in(0,1)$. Vergleiche Beispiel 1 und 2.

**Bemerkung 2.** Der Begriff einer Summe einer unendlichen Reihe ist wesentlich verschieden von der Summe endlich vieler Summanden. Zum Beispiel können zur divergenten Reihe $$
  1-1+1-1+1-1\pm ...
$$ durch Klammerung neue (!) Zahlenreihen gebildet werden $$
  (1-1)+(1-1)+(1-1)+...=0+0+0+...=0
$$ wohingegen eine davon abweichende Klammerung $$
  1-(1-1)-(1-1)-(1-1)-...=1-0-0-0-...=1
$$ erzeugt.

Es gilt folgender Satz (ohne Beweis):

>**Satz 1.** Wird zu einer ~~konvergenten~~ Reihe $$
  \sum_{k=0}^\infty{a_k}=a_0+a_1+a_2+...
$$ durch Klammerung die Reihe $$
  (a_0+...+a_{n_1})+(a_{n_1+1}+...+a_{n_2})++(a_{n_2+1}+...+a_{n_3})+...
$$ gebildet, so konvergiert diese stets und besitzt dieselbe Summe wie die Reihe $\sum_{k=0}^\infty{a_k}$ (*Assoziativgesetz*).

**Beispiel 3.** Analog zu Beispiel 1 lässt sich zeigen, dass die Reihe $$
  \sum_{m=0}^\infty{\left(\frac{3}{2^{2\cdot m+1}}\right)}=\frac{3}{2}+\frac{3}{8}+\frac{3}{32}+...=\left(1+\frac{1}{2}\right)+\left(\frac{1}{4}+\frac{1}{8}\right)+\left(\frac{1}{16}+\frac{1}{32}\right)+...
$$ gegen den Grenzwert $2$ konvergiert. Wegen $$
  \frac{1}{2^{2\cdot m}}+\frac{1}{2^{2\cdot m+1}}=\frac{2+1}{2^{2\cdot m+1}}=\frac{3}{2^{2\cdot m+1}}
$$ entsteht durch Klammerung aus der konvergenten Reihe $$
  1+\frac{1}{2}+\frac{1}{4}+\frac{1}{8}+...=2
$$


Konvergenzkriterien für Zahlenreihen
====================================


>**Satz 2.** Gegeben ist eine unendliche Zahlenreihe $\sum_{k=0}^\infty{a_k}$. Für die Konvergenz der Reihe ist
>
>1. *notwendig* $$
  \lim_{k\to\infty}{a_k}=0
$$ d.h. die zugehörige Zahlenfolge $(a_k)_{k=0}^\infty$ ist eine Nullfolge.
>2. *hinreichend*, falls $a_k\not=0$ für alle $k$ $$
  \lim_{k\to\infty}{\left|\frac{a_{k+1}}{a_k}\right|}=q<1
$$ Für $q>1$ divergiert die Reihe, für $q=1$ ist über die Konvergenz der Reihe mit diesem Kriterium nicht entscheidbar. Dieses Kriterium wird *Quotientenkriterium* genannt.

**Beweis.** Für Interessierte hier eine Beweisskizze für die zweite Aussage unter Benutzung des Majorantenkriteriums, siehe Satz 3.

Es werde $a_k>0$ für alle $k\in\mathbb{N}$ vorausgesetzt (alternativ $a_k<0$). Es gelte dann $$
  \lim_{k\to\infty}{\left|\frac{a_{k+1}}{a_k}\right|}=
  \lim_{k\to\infty}{\frac{a_{k+1}}{a_k}}<1
$$ Dann gibt es ein $k_0\in\mathbb{N}$, so dass $$
  \left|\frac{a_{k+1}}{a_k}\right|=\frac{a_{k+1}}{a_k}\leq r<1\quad\forall\;k\geq k_0
$$ für ein bestimmtes $r$. Hieraus folgt $$
  a_{k_0+j}\leq r\cdot a_{k_0+j-1}\leq r^2\cdot a_{k_0+j-2}\leq ...\leq r^j\cdot a_{k_0}\quad\forall\; j\geq0
$$ Damit ist die geometrische Reihe $$
  \sum_{j=0}^\infty{b_j}:=a_{k_0}\cdot\sum_{j=0}^\infty{r^j}
$$ eine konvergente Majorante der Reihe $\sum_{j=0}^\infty{a_{k_0+j}}$. Durch Addition endlich vieler Glieder $a_k$ mit $k<k_0$ ändert sich die Konvergenz nicht.

In den nachstehenden Videos werden notwendiges Kriterium / Quotientenkriterium / Wurzelkriterium für die Konvergenz einer Zahlenreihe an je einem Beispiel erläutert.

!?[Notwendiges Kriterium](https://www.youtube.com/watch?v=uafZtktPqN0&list=PLLTAHuUj-zHjs82YCjiSUeWnNGZkEePIE)

!?[Quotientenkriterium](https://www.youtube.com/watch?v=QVHW1YyNHgI&list=PLLTAHuUj-zHjs82YCjiSUeWnNGZkEePIE)

In den nachstehenden Videos wird das Wurzelkriterium für die Konvergenz einer Zahlenreihe an je einem Beispiel erläutert.

!?[Wurzelkriterium1](https://www.youtube.com/watch?v=-cnZrIZ66xs&list=PLLTAHuUj-zHjs82YCjiSUeWnNGZkEePIE)

!?[Wurzelkriterium2](https://www.youtube.com/watch?v=J0ZDceKddcI&list=PLLTAHuUj-zHjs82YCjiSUeWnNGZkEePIE)

Nachstehend werden weitere hinreichende Kriterien zum Nachweis der Konvergenz / Divergenz von Zahlenreihen aufgezeigt (ohne Beweis).

In Satz 3 werden alternierende Reihen untersucht.

>**Satz 3.** *Leibnizsches Konvergenzkriterium*
>
>Eine alternierende Reihe $$
  \sum_{k=1}^\infty{(-1)^{k+1}\cdot a_k}=a_1-a_2+a_3-a_4+-\ldots
$$ ist konvergent, wenn für die Reihenglieder gilt:
>
>1. $\left(a_k\right)_{k=1}^\infty$ bildet eine monoton fallende Zahlenfolge, d.h. $$
  a_1>a_2>a_3>\ldots>a_k>a_{k+1}>\ldots
$$ mit $a_k>0$ für alle $k\in\mathbb{N}\setminus\{0\}$.
>2. Für den Grenzwert gilt: $\lim_{k\rightarrow\infty}{a_k}=0$

In Satz 4 wird aus der zu untersuchenden Reihe durch Verdichten eine Vergleichsreihe gebildet, deren Konvergenzverhalten stellvertretend untersucht werden kann.

>**Satz 4.** *Cauchysches Verdichtungskriterium*
>
>Sei $(a_k)_{k\in\mathbb{N}}$ eine monoton fallende Zahlenfolge. Dann hat die unendliche Reihe $$
  S=\sum_{k=1}^\infty{a_k}=a_1+a_2+a_3+\ldots
$$ das gleiche Konvergenzverhalten wie die verdichtete Reihe $$
  T=\sum_{n=0}^\infty{2^na_{\left(2^n\right)}}=a_1+2\cdot a_2+4\cdot a_4+8\cdot a_8+\ldots
$$ das heißt, dass die eine Reihe genau dann konvergiert, wenn die andere konvergiert.

Durch Abschätzung der Reihenglieder werden Vergleichsreihen gebildet, deren Konvergenzverhalten Rückschluss auf das der zu untersuchenden Reihe lässt (Satz 5).

>**Satz 5.** Sei $\sum_{n=1}^\infty{a_n}$ eine unendliche Reihe mit positiven Gliedern $a_n$.
>
>*Majorantenkriterium.* Die Reihe *konvergiert*, wenn eine Vergleichsreihe $$
  \sum_{n=1}^\infty{b_n}
$$ existiert mit:
>
>* Die Vergleichsreihe $\sum_{n=1}^\infty{b_n}$ konvergiert.
>* Zwischen den Gliedern beider Reihen besteht die Relation $a_n\leq b_n$ für alle $n$.
>
>*Minorantenkriterium*. Die Reihe *divergiert*, wenn eine Vergleichsreihe $$
  \sum_{n=1}^\infty{b_n}
$$ existiert mit:
>
>* Die Vergleichsreihe $\sum_{n=1}^\infty{b_n}$ ist divergent.
>* Zwischen den Gliedern beider Reihen besteht die Relation $a_n\geq b_n$ für alle $n$.

**Beispiel 4.** Die zur unendlichen Zahlenfolge $$
  n\mapsto a_n=\frac{1}{n} \quad (n\in\mathbb{N}\setminus\emptyset)
$$ gebildete unendliche Folge $\left( s_n\right)_{n=1}^\infty$ der Partialsummen mit $$
  s_n=\sum_{k=1}^n{\frac{1}{k}}= 1+\frac{1}{2}+\frac{1}{3}+\ldots+\frac{1}{n-1}+\frac{1}{n}
$$ heißt *harmonische Reihe*.

Zur Untersuchung des Konvergenzverhaltens der Reihe werden die Teilsummen $s_n$ zum Index $n=2^m$ gebildet $$
  s_{2^m}=\sum_{k=1}^{2^m}{\frac{1}{k}}=1+\frac{1}{2}+\frac{1}{3}+\cdots+\frac{1}{2^m}
$$ und anschließend durch Vergleichssummen von Potenzen $\frac{1}{2^p}$ mit $p\in\{0,1,\ldots,m\}$ nach unten abgeschätzt. Für $m\geq1$ gelten beispielsweise: $$
  s_{2^1} = 1+\frac{1}{2}
$$ beziehungsweise $$
  s_{2^2} = 1+\frac{1}{2}+\left(\frac{1}{3}+\frac{1}{4}\right) > 1+\frac{1}{2}+\frac{1}{4}+\frac{1}{4} = \underline{1+\frac{1}{2}+\frac{1}{2}}
$$ beziehungsweise $$
  s_{2^3} = 1+\frac{1}{2}+\left(\frac{1}{3}+\frac{1}{4}\right)+\left(\frac{1}{5}+\frac{1}{6}+\frac{1}{7}+\frac{1}{8}\right) > 1+\frac{1}{2}+\frac{1}{4}+\frac{1}{4}+\frac{1}{8}+\frac{1}{8}+\frac{1}{8}+\frac{1}{8} = \underline{1+\frac{1}{2}+\frac{1}{2}+\frac{1}{2}}
$$ sowie für ein allgemeines $m$ $$
  s_{2^m} = 1+\frac{1}{2}+\left(\frac{1}{3}+\frac{1}{4}\right)+\ldots+\left(\frac{1}{2^{m-1}+1}+\frac{1}{2^{m-1}+2}+\ldots+\frac{1}{2^{m-1}+2^{m-1}}\right) > 1+\frac{1}{2}+\frac{1}{4}+\frac{1}{4}+\ldots+\frac{1}{2^m}\cdot l
$$ mit $l=2^m-\left(2^{m-1}+1\right)+1=2^{m-1}$.

Hieraus folgt $$
  s_{2^m}>m\cdot\frac{1}{2}+1
$$ Somit ist die Teilfolge $\left(s_{2^m}\right)_{m=1}^\infty$ nicht beschränkt, also auch nicht konvergent. Und schließlich folgt, dass die Reihe $\left(s_n\right)_{n=1}^\infty$ nach Satz 4 keinen Grenzwert besitzt.

**Beispiel 5.** Zu untersuchen ist die unendliche Reihe $\left( t_n\right)_{n=1}^\infty$ mit $$
  t_n=\sum_{k=1}^n{\frac{1}{\sqrt{k}}}= 1+\frac{1}{\sqrt{2}}+\frac{1}{\sqrt{3}}+\ldots+\frac{1}{\sqrt{n-1}}+\frac{1}{\sqrt{n}}
$$ auf Konvergenz durch Vergleich mit der harmonischen Reihe.

Mit dem Minorantenkriterium folgt wegen $$
  \frac{1}{\sqrt{k}}\geq\frac{1}{k} \quad\forall k
$$ und der Eigenschaft, dass die Folge $\left(\frac{1}{\sqrt{k}}\right)_{k=1}^\infty$ streng monoton fallend ist, dass die harmonische Reihe (Beispiel 4) eine divergente Minorante der Reihe $\left( t_n\right)_{n=1}^\infty$ ist, letztere also ebs. divergent ist. Vergleiche Satz 5.

>**Satz 6.**   Seien $\left(\sum_{k=0}^na_k\right)_{n=0}^\infty$ und $\left(\sum_{k=0}^nb_k\right)_{n=0}^\infty$ konvergente Reihen mit Summenwerten $$
  \sum_{k=0}^\infty a_k=a\,,\quad\sum_{k=0}^\infty b_k=b
$$ Dann gelten:
>
>1. Gliedweise Multiplikation mit $\lambda\in\mathbb{R}$ $$
  \lambda\cdot\sum_{k=0}^na_k=\sum_{k=0}^n\left(\lambda a_k\right)\longrightarrow \lambda\cdot\sum_{k=0}^\infty a_k=\lambda\cdot a
$$
>2. Gliedweise Addition und Subtraktion: $$
\sum_{k=0}^na_k\pm \sum_{k=0}^nb_k=\sum_{k=0}^n\left(a_k\pm b_k\right)\longrightarrow \sum_{k=0}^\infty a_k\pm \sum_{k=0}^\infty b_k=a\pm b
$$


Sicher gewußt
=============


Testen Sie Ihr Wissen zu den Themen dieses Abschnitts.

---

**Frage 1.** Für welche der folgenden Zahlenreihen ist die notwendige Bedingung für die Konvergenz erfüllt?

[[X]] $$\sum_{k=1}^\infty{\frac{1}{k\cdot(k+1)}}$$
[[X]] $$\sum_{k=0}^\infty{\left(k\cdot\exp{(-k)}\right)}$$
[[ ]] $$\sum_{k=0}^\infty{\exp{k}}$$
[[?]] Notwendig für die Konvergenz einer Reihe $\sum_{k\in\mathbb{N}}{a_k}$ ist $$
  \lim_{k\to\infty}{a_k}=0
$$ d. h. dass die Folge der Glieder $a_k$ mit $n\in\mathbb{N}$ eine Nullfolge ist. Vergleiche Satz 2.
****************************************

Mit Hilfe der Grenzwertsätze und $\lim_{k\to\infty}{(1/k^m)}=0$ für beliebiges $m\in\mathbb{N}\setminus{0}$ ergibt sich $$
  \lim_{k\to\infty}{\frac{1}{k\cdot(k+1)}}=
  \lim_{k\to\infty}{\frac{\frac{1}{k^2}}{1+\frac{1}{k}}}=0
$$ unter Benutzung der L´Hospital-Regel für die reellen Funktionen $k\mapsto k$ und $k\mapsto \exp{k}$ mit $k\in\mathbb{R}$ $$
  \lim_{k\to\infty}{\left(k\cdot\exp{(-k)}\right)}=
  \lim_{k\to\infty}{\left(-1\cdot\exp{(-k)}\right)}=0
$$ jedoch $$
  \lim_{k\to\infty}{\exp{k}}=\infty
$$

****************************************

---

**Frage 2.** Für welche reellen $x$ gilt die folgende Gleichung? $$
  \sum_{k=0}^\infty{x^k}=
  \sum_{k=0}^\infty{\left(\left(\frac{1}{2}\right)^{k+1}\cdot(x+1)^k\right)}
$$

[( )] $x\in\mathbb{R}$
[( )] $x\in\mathbb{R}\setminus\{1\}$
[(X)] $x\in(-1,1)$
[[?]] Linke und reche Seite der Gleichung sind unter Benutzung der Summenformel für geometrische Reihen umzuformen. Der Konvergenzbereich der jeweiligen Reihe ist zu beachten.
****************************************

Die linke Seite der Gleichung berechnet sich unter Benutzung der Summenformel zu $$
  \sum_{k=0}^\infty{x^k}=\frac{1}{1-x}\,,\quad x\in(-1,1)
$$ die rechte Seite entsprechend $$
  \sum_{k=0}^\infty{\left(\left(\frac{1}{2}\right)^{k+1}\cdot(x+1)^k\right)}=
  \sum_{k=0}^\infty{\left(\frac{1}{2}\cdot\left(\frac{x+1}{2}\right)^k\right)}=
  \frac{1}{2}\cdot\frac{1}{1-\frac{x+1}{2}}=\frac{1}{1-x}
$$ worin $$
  \frac{x+1}{2}\in(-1,1)\quad\leftrightarrow\quad x\in(-3,1)
$$ den Konvergenzbereich angibt. Die Gleichheit von linker und rechter Seite ergibt sich also für alle $x$ in $$
  (-1,1)=(-1,1)\cap(-1,3)
$$

****************************************


### Definition einer Funktionenreihe

Funktionenfolge
===============


Es bezeichne $\left(f_k\right)_{k=1}^\infty$ mit $$
  f_k:x\mapsto y=f_k(x)
$$ eine unendliche Folge reeller Funktionen mit gemeinsamen Definitionsbereich $D\subseteq\mathbb{R}$. Für ein Argument $x_0\in D$ bildet $$
  (y_k)_{k=1}^\infty=\left(f_k(x_0)\right)_{k=1}^\infty
$$ eine zu $x_0$ gehörende Zahlenfolge von Funktionswerten $y_k=f_k(x_0)$.

Für die anstehende Begriffsbildung wird das folgende Beispiel betrachtet.

**Beispiel 1.** Es wird die Folge $\left( f_k\right)_{k=1}^\infty$ der Funktionen $f_k:x\mapsto x^k=f_k(x),\; x\in\mathbb{R}$ betrachtet.

1. Für $x_0=1$ bildet $$
  \left(f_k(x_0)\right)_{k=1}^\infty=\left(1^k\right)_{k=1}^\infty=1,1,1,1,...
$$ eine unendliche, konstante Zahlenfolge der zu $x_0$ gehörenden Funktionswerte $f_k(x_0)$.
2. Für $x_0=-1$ bildet $$
  \left(f_k(x_0)\right)_{k=1}^\infty=\left((-1)^k\right)_{k=1}^\infty=-1,1,-1,1,...
$$ eine unendliche, alternierende Zahlenfolge der zu $x_0$ gehörenden Funktionswerte $f_k(x_0)$. Diese ist divergent mit den beiden Häufungswerten $1$ und $-1$.
3. Für $x_0=\frac{1}{2}$ bildet $$
  \left(f_k(x_0)\right)_{k=1}^\infty=\left(\left(\frac{1}{2}\right)^k\right)_{k=1}^\infty=\frac{1}{2},\frac{1}{4},\frac{1}{8},\frac{1}{16},...
$$ eine unendliche, monoton fallende Zahlenfolge der zu $x_0$ gehörenden Funktionswerte $f_k(x_0)$. Diese ist konvergent mit dem Grenzwert $0$. (Nachweis beispielsweise mit Quotientenkriterium, siehe Abschnitt [Zahlenreihen](#Zahlenfolgen-und-Reihen))
4. Für ein allgemeines Argument $x_0\in D$ bildet $$
  \left(f_k(x_0)\right)_{k=1}^\infty=\left(x_0^k\right)_{k=1}^\infty=x_0,x_0^2,x_0^3,x_0^4,...
$$ eine unendliche, geometrische Zahlenfolge. Dabei gilt $$
  \lim_{k\rightarrow\infty}{f_k(x_0)}=\left\{\begin{array}{ll}
    0 & \text{ für } |x_0|<1 \\ 1 & \text{ für } x_0=1
  \end{array}\right.
$$ Für $|x_0|>1$ beziehungsweise für $x_0=-1$ ist die Folge $\left(f_k(x_0)\right)_{k=1}^\infty$ divergent.

Das Intervall $D_0=(-1,1]$ heißt *Konvergenzbereich* der Funktionenfolge $\left( f_k\right)_{k=1}^\infty$. Es ist $D_0\subset D$.

![Funktionenfolge](img/mat-bild-03.png "_Fig._ Glieder der Funktionenfolge $\left( f_k\right)_{k=1}^\infty$ der Funktionen $f_k:x\mapsto x^k=f_k(x),\; x\in\mathbb{R}$ mit $n=1$ (rot), $n=2$ (blau), $n=3$ (lila), $n=4$ (cyan), $n=5$ (grün) und $n=100$ (schwarz). Die Funktionen sind auf dem Intervall $(-1,1]$ definiert.")

>**Definition 1.** Sei $\left( f_k\right)_{k=1}^\infty$ eine unendliche Folge reeller Funktionen mit gemeinsamen Definitionsbereich $D\subseteq\mathbb{R}$. Sei $D_0\subseteq D$ die Menge aller Argumente $x\in D$, für welche die Folge der Funktionswerte $\left( f_k(x)\right)_{k=1}^\infty$ konvergiert. $D_0$ heißt **Konvergenzbereich** der Funktionenfolge $\left( f_k\right)_{k=1}^\infty$ und $$
  f:x\mapsto f(x)=\lim_{k\to\infty}{f_k(x)}\,,\quad x\in D_0
$$ heißt **Grenzfunktion** dieser Folge.

**Bemerkung 1.** Konvergenzbereich und Grenzfunktion übertragen den Begriff des Grenzwertes einer Zahlenfolge auf Folgen reeller Funktionen.

**Beispiel 2.** (Fortführung von Beispiel 1.) Die Grenzfunktion der Funktionenfolge $\left( f_k\right)_{k=1}^\infty$ der Funktionen $$
  f_k:x\mapsto y=f_k(x)=x^k,\; x\in\mathbb{R}
$$ ist die Funktion $$
  f:x\mapsto y=f(x)=\left\{
    \begin{array}{ccc}
      0 & \text{ für } & x\in(-1,1) \\ 1 & \text{ für } & x=1
    \end{array}
  \right.
$$ der Konvergenzbereich der Funktionenfolge bildet den Definitionsbereich der Grenzfunktion. Zu bemerken ist, das alle Funktionen $f_k$ mit $k\geq1$ differenzierbar sind, hingegen ist die Grenzfunktion $f$ nicht stetig in $x=1$. Siehe auch die vorstehende Abbildung.


Funktionenreihe
===============


In gewisser Analogie zur Bildung einer Partialsummenfolge zu einer Zahlenfolge wird nun zu gegebener Folge $\left( f_k\right)_{k=1}^\infty$ reeller Funktionen mit gemeinsamen Definitionsbereich $D_0$ (Konvergenzbereich der Funktionenfolge) die Folge von Teilsummen von $\left( f_k(x)\right)_{k=1}^\infty$ für $x\in D_0$ gebildet, für $n=1$ $$
  s_1(x)=f_1(x)
$$ beziehungsweise für $n=2$ $$
  s_2(x)=f_1(x)+f_2(x)
$$ beziehungsweise für ein allgemeines $n\in\mathbb{N}$ $$
  s_n(x)=\sum_{k=1}^n{f_k(x)}
$$ das *$n$-tes Glied der Funktionenreihe* genannt wird. Anders als bei Zahlenreihen ist das Glied $s_n(x)$ abhängig von der Stelle $x$.

---

Die zu $\left( f_k\right)_{k=1}^\infty$ gebildete Partialsummenfolge $$
  \left(s_n(x)\right)_{n=0}^\infty=\sum_{k=1}^\infty{f_k(x)}\,,\quad x\in D_0
$$ wird **Funktionenreihe** der Funktionenfolge genannt.

---

**Beispiel 3.**  (Fortführung der Beispiele 1 und 2.) Für die Funktionenfolge $\left( f_k\right)_{k=1}^\infty$ der Funktionen $f_k:x\mapsto x^k=f_k(x),\; x\in D_0$ ergibt sich das allgemeine Glied der Funktionenreihe $$
  s_n(x)=x+x^2+...+x^n=\sum_{k=1}^n{x^k}\,,\quad x\in D_0
$$ Unter Benutzung von $$
  x\cdot s_n(x)=x^2+...+x^n+x^{n+1}=\sum_{k=2}^{n+1}{x^k}
$$ folgt hieraus für das allgemeine Glied der Funktionenreihe $$
  s_n(x)=\left\{\begin{array}{lcl}
    x\cdot\frac{1-x^n}{1-x} & \text{für} & x\not=1 \\
    n & \text{für} & x=1 \\
  \end{array}\right.
$$ Damit ergibt sich unter dem Grenzübergang $n\to\infty$ $$
  \lim_{n\to\infty}{s_n(x)}=\left\{\begin{array}{lcl}
    \frac{1}{1-x}-1 & \text{für} & x\in(-1,1) \\
    \infty & \text{für} & x=1 \\
  \end{array}\right.
$$ und schließlich für die Summenfunktion der Funktionenreihe $(s_n(x))_{n=1}^\infty=\sum_{k=1}^\infty{f_k(x)}$ $$
  s:x\mapsto y=s(x)=\frac{1}{1-x}-1\,,\quad x\in(-1,1)
$$ Siehe nachstehende Abbildung.

![Funktionenfolge2](img/mat-bild-04.png "_Fig._ Summenfunktion $s$ (strichliert) sowie Glieder der Funktionenfolge $\left( f_k\right)_{k=1}^\infty$ der Funktionen $f_k:x\mapsto x^k=f_k(x),\; x\in\mathbb{R}$ mit $n=1$ (rot), $n=2$ (blau), $n=3$ (lila), $n=4$ (cyan), $n=5$ (grün) und $n=100$ (schwarz).Die Funktion $s$ ist im Intervall $(-1,1)$ definiert.")

>**Definition 2.** Die Menge aller Argumente $x_0\in D_0$, für welche die Reihe $\sum_{k=0}^\infty{(f_k(x_0))}$ konvergiert, heißt **Konvergenzbereich** $D_1$ der Funktionenreihe, und $$
  x\mapsto s(x)=\sum_{k=0}^\infty{(f_k(x))}\,,\quad x\in D_1
$$ heißt **Summenfunktion** der Funktionenreihe.

**Bemerkung 2.** Der in Definition 1 genutzte Begriff der Konvergenz ist auf eine Stelle $x_0$ des Konvergenzbereiches bezogen. Unter Zuhilfenahme von Quantoren lässt sich diese darstellen: $$
  \forall \epsilon>0\;\; \forall x\in D\;\; \exists n_0\in\mathbb{N}\;\; \forall n\geq n_0\;\; \left(|f_n(x)-f(x)|<\epsilon\right)
$$ worin $x$ eine Stelle des Konvergenzbereiches $D$ und $f$ die Grenzfunktion bezeichnen. Die so definierte Konvergenz wird ~~punktweise Konvergenz~~ genannt.

Demgegenüber legt $$
  \forall \epsilon>0\;\; \exists n_0\in\mathbb{N}\;\; \forall x\in D\;\; \forall n\geq n_0\;\; \left(|f_n(x)-f(x)|<\epsilon\right)
$$ ~~gleichmäßige Konvergenz~~ fest. Hier wird die absolute Differenz zwischen $f_n(x)$ und $f(x)$ für alle $x\in D$ betrachtet.

**Beispiel 4.**   (Fortführung der Beispiele 1, 2 und 3.)

1. Betrachtet sei $(f_k)_{k=0}^\infty$ mit $f_k(x)=x^k$ wie im vorigen Beispiel, jedoch mit eingeschränktem Definitionsbereich $D=[0,q)$ und $q\in(0,1)$ als reellem Parameter. Die Funktionen $f_k$ konvergieren gleichmäßig gegen $f:x\mapsto 0$ (Nullfunktion).
2. Für D=[0,1) konvergieren $f_k$ punktweise gegen die Nullfunktion, nicht aber gleichmäßig, da $$
  \lim_{x\to 1-0}{f_k(x)}=1\;\;\forall k
$$ aber $$
  \lim_{x\to 1-0}{f(x)}=0
$$


### Potenzreihen

Definition und Eigenschaften
============================


In diesem Abschnitt wird eine spezielle Klasse von Funktionenreihen untersucht.

>**Definition 1.** Eine Funktionenreihe der Form $$
  \sum_{k=0}^\infty{\left(a_k\cdot(x-x_0)^k\right)}
$$ mit Koeffizienten $a_k\in\mathbb{R}$ heißt **Potenzreihe**. Die feste Stelle $x_0\in\mathbb{R}$ wird **Entwicklungsstelle** bzw. Mittelpunkt der Potenzreihe genannt.

Das allgemeine Glied der Potenzreihe in Definition 1 ist $$
  s_n(x)=\sum_{k=0}^n{\left(a_k\cdot(x-x_0)^k\right)}
$$ Bezeichnet $D_1$ den Konvergenzbereich der Potenzreihe, so stellt $$
  x\in s(x)=\sum_{k=0}^\infty{\left(a_k\cdot(x-x_0)^k\right)}=\lim_{n\to\infty}{s_n(x)}
$$ die *Summenfunktion* der Potenzreihe dar.

**Beispiel 1.** Die nachstehenden Beispiele von Funktionenreihen stellen Potenzreihen dar.

1. Die bereits in ähnlicher Form im vorangegangenen Abschnitt betrachtete Funktionenreihe kann dargestellt werden $$
  \sum_{k=0}^\infty{x^k}=1+x+x^2+...+x^n+x^{n+1}+...=\sum_{k=0}^\infty{\left(1\cdot(x-0)^k\right)}
$$ woraus sich die Koeffizienten $a_k=1$ für beliebige Werte $k\in\mathbb{N}$ und die Entwicklungsstelle $x_0=0$ ablesen lassen. Damit lassen sich das allgemeine Glied der Potenzreihe $$
  s_n(x)=\sum_{k=0}^\infty{x^k}
$$ sowie die Summenfunktion der Potenzreihe $$
  x\mapsto s(x)=\frac{1}{1-x}\,,\quad x\in(-1,1)
$$ angeben.
2. Die Funktionenreihe der Form $$
  \sum_{k=0}^\infty{\left((x+2)^k\right)}=1+(x+2)+(x+2)^2+(x+2)^3+...
$$ ist eine Potenzreihe mit reellen Koeffizienten $a_k=1$ für beliebige Werte $k\in\mathbb{N}$ und der Entwicklungsstelle $x_0=-2$, da sich die Summanden der Reihe in der Form $$
  (x+2)^k=(x-(-2))^k
$$ (vergleiche Definition 1) darstellen lassen. Diese Funktionenreihe liefert für jedes $x\not=-2$ eine geometrische Reihe, wonach unter Nutzung der Summenformel für geometrische Reihen $$
  x\mapsto s(x)=\frac{1}{1-(x+2)}=-\frac{1}{1+x}\,,\quad x\in(-3,-1)
$$ für die Summenformel der Funktionenreihe ergibt.
3. Die Funktionenreihe der Form $$
  \sum_{k=0}^\infty{\frac{x^k}{k!}}=1+\frac{x}{1}+\frac{x^2}{2}+\frac{x^3}{3!}+...+\frac{x^n}{n!}+\frac{x^{n+1}}{(n+1)!}+...
$$ lässt sich in der Form von Definition 1 darstellen $$
  \sum_{k=0}^\infty{\frac{x^k}{k!}}=\sum_{k=0}^\infty{\left(\frac{1}{k!}\cdot (x-0)^k\right)}
$$ woraus sich die Koeffizienten $a_k=\frac{1}{k!}$ für beliebige Werte $k\in\mathbb{N}$ und die Entwicklungsstelle $x_0=0$ ablesen lassen. Damit lässt sich das allgemeine Glied der Potenzreihe $$
  s_n(x)=\sum_{k=0}^n{\left(\frac{1}{k!}\cdot (x-0)^k\right)}
$$ angeben. Um die Summenfunktion dieser Potenzreihe zu ermitteln, ist zunächst der Konvergenzbereich $D_1$ der Reihe zu bestimmen. Hierfür wird ein $x\in\mathbb{R}$ beliebig, aber fest gewählt. Mit $$
  b_n=\frac{x^n}{n!}\quad\text{und}\quad b_{n+1}=\frac{x^{n+1}}{{n+1}!}=\frac{x^n}{n!}\cdot\frac{x}{n+1}=b_n\cdot\frac{x}{n+1}
$$ lässt sich unter Benutzung des Quotientenkriteriums für die Zahlenreihen (siehe Abschnitt [Zahlenfolgen und Reihen](#Zahlenfolgen-und-Reihen) zeigen $$
  \left|\frac{b_{n+1}}{b_n}\right|=\frac{|x|}{n+1}
$$ sowie $$
  \lim_{n\to\infty}\left|\frac{b_{n+1}}{b_n}\right|=0\quad \forall x\in\mathbb{R}
$$ Dies bedeutet, dass für jedes $x\in\mathbb{R}$ die entsprechende Zahlenreihe $\sum_{n=0}^\infty{b_n}$ konvergiert und damit $D_1=\mathbb{R}$. Die Summenfunktion ergibt sich damit $$
  x\mapsto s(x)=\sum_{k=0}^\infty{\frac{x^k}{k!}}\,,\quad x\in\mathbb{R}
$$

Im nachstehenden Video werden Definition und allgemeine Darstellungeiner Potenzreihen sowie Begriffe wie Koeffizienten und Entwicklungsstelle erläutert.

!?[Potenzreihe](https://www.youtube.com/watch?v=CeEfXWalXeU&list=PLLTAHuUj-zHjs82YCjiSUeWnNGZkEePIE)


Konvergenzbereich
=================


Der ~~Konvergenzbereich~~ $D_1$ einer Potenzreihe ergibt sich zu $$
  D_1=(x_0-r,x_0+r)\quad\text{mit}\quad r\geq 0
$$ d. h. als zur Entwicklungsstelle $x_0$ symmetrisches Intervall, worin $r$ den **Konvergenzradius** bezeichnet, beziehungsweise ist $D_1=\mathbb{R}$. (In diesem Fall ist $r$ als 'unbegrenzt' groß zu interpretieren.)

Der Konvergenzradius lässt sich mithilfe der Formel $$
    r=\frac{1}{\limsup_{n\to\infty}{\sqrt[n]{|a_{n+1}|}}}
$$ d. h. unter Benutzung des Limes superior und der expliziten Darstellung der Koeffizienten $n\mapsto a_n$ der Potenzreihe berechnen. Siehe auch [Konvergenzradius](https://de.wikipedia.org/wiki/Konvergenzradius).

Gilt ab einem $n\in\mathbb{N}$ für alle folgenden Argumente $N>n$ für die Koeffizienten der Potenzreihe $a_N\not=0$, so lässt sich der Konvergenzradius einfacher berechnen mittels $$
  r=\lim_{n\to\infty}{\left|\frac{a_n}{a_{n+1}}\right|}
$$ sobald dieser existiert ($r\in\mathbb{R}$) bzw. 'unendlich' ergibt.

**Nachweis.** Es bezeichne $$
  \sum_{k=0}^\infty{\left(a_k\cdot(x-x_0)^k\right)}
$$ eine Potenzreihe mit reellen Koeffizienten $a_k$, Entwicklungsstelle $x_0\in D_1$ des Konvergenzbereiches $D_1$. Es sei eine weitere Stelle $x_1\not=x_0$ des Konvergenzbereiches $D_1$ der Potenzreihe vorausgesetzt. Damit gelte $$
  a_k\cdot(x_1-x_0)^k<c \quad\forall\; k\in\mathbb{N}
$$ für ein $c\in\mathbb{R}$. Hieraus lässt sich unter Benutzung von $$
  \left|a_k\cdot(x-x_0)^k\right|=\left|a_k\cdot(x_1-x_0)^k\right|\cdot\frac{|x-x_0|^k}{|x_1-x_0|^k}<
  c\cdot\frac{|x-x_0|^k}{|x_1-x_0|^k}
$$ eine Majorante konstruieren $$
  c\cdot\sum_{k=0}^\infty\cdot\left|\frac{x-x_0}{x_1-x_0}\right|^k
$$ die für jede Wahl $x$ eine geometrische Reihe bestimmt. Diese konvergiert, falls $$
  \left|\frac{x-x_0}{x_1-x_0}\right|<1
$$ Vergleiche Beispiel 1 im Abschnitt [Zahlenfolgen und Reihen](#Zahlenfolgen-und-Reihen). Letztere Bedingung liefert eine Ungleichung für den Konvergenzradius $r$ $$
  |x-x_0|<|x_1-x_0|=:r_1<r
$$ (als Supremum über alle $x_1\in D_1$). Außerdem folgt mit Hilfe des Quotientenkriteriums $$
  \lim_{k\to\infty}\left|\frac{a_{k+1}\cdot(x-x_0)^{k+1}}{a_{k}\cdot(x-x_0)^{k}}\right|=
  \lim_{k\to\infty}{\left|\frac{a_{k+1}}{a_{k}}\right|}\cdot|x-x_0|<1
$$ woraus die Formel zur Berechnung des Konvergenzradius folgt $$
  |x-x_0|<\lim_{k\to\infty}{\left|\frac{a_{k}}{a_{k+1}}\right|}=r
$$ $\square$

>**Satz 1.** (Gleichmäßige Konvergenz von Potenzreihen)
>
>Jede Potenzreihe $$
  \sum_{k=0}^\infty{\left(a_k\cdot(x-x_0)^k\right)}
$$ konvergiert gleichmäßig auf jedem abgeschlossenen und beschränkten Teilbereich $$
  [x_0-r_1,x_0+r_1]\subset D_1
$$ des Konvergenzbereiches $D_1$, worin $0<r_1<r$ für den Konvergenzradius $r$ gilt.

>**Folgerung 2.** Gegeben seien die auf dem gemeinsamen Bereich $D=[x_0-d,x_0+d]$ konvergenten Potenzreihen $$
 s_a(x)=\sum_{k=0}^\infty{a_k\left(x-x_0\right)^k}\,, \quad s_b(x)=\sum_{k=0}^\infty{b_k\left(x-x_0\right)^k} \quad (x\in D)
$$ mit $d>0$.[^1]
>
>1. $s_a$ darf beliebig oft gliedweise differenziert und integriert werden. Die neuen Potenzreihen konvergieren im gleichen Bereich $D$.
>2. $s_a$ und $s_b$ dürfen gliedweise addiert, subtrahiert, multipliziert werden. Die neuen Potenzreihen konvergieren mindestens im Bereich $D$.


Konstruktion einer Potenzreihe zu gegebener Funktion
====================================================


Nun soll die Konstruktion einer Potenzreihe zu einer hinreichend of stetig differenzierbaren Funktion $f$ betrachtet werden.

>**Satz 3.** (Taylor-Polynom)
>
>Ist eine Funktion $f:D\to\mathbb{R}$ mit $D\subseteq\mathbb{R}$ in der Umgebung $U(x_0)$ einer Entwicklungsstelle $x_0\in D$ $(n+1)$-mal stetig differenzierbar, dann existiert eine Stelle $\xi\in U(x_0)$, so dass für alle $x\in U(x_0)$ gilt $$
  f(x)=P_n(x)+R_n(x)
$$ mit **Taylorpolynom** $n$-ten Grades $$
  P_n(x)=f(x_0)+\sum_{k=1}^n{\frac{f^{(k)}(x_0)}{k!}\cdot(x-x_0)^k}
$$ und dem **Restglied** $$
  R_n(x)=\frac{f^{(n+1)}(\xi)}{(n+1)!}\cdot(x-x_0)^{n+1}
$$ das ein Polynom  $(n+1)$-ten Grades ist.

**Beispiel 2.** Gegeben sei die Funktion $$
  f:x\mapsto y=\sin{x}\,,\quad x\in\mathbb{R}
$$ sowie die Stelle $x_0=\frac{\pi}{2}$.

Das Taylorpolynom zweiten Grades von $f$ an der Stelle $x_0$ berechnet sich mittels $f(x_0)=\sin{x_0}=1$ und der beiden Ableitungen $$
  f^\prime(x_0)=\cos{x_0}=0\quad\text{und}\quad
  f^{\prime\prime}(x_0)=-\sin{x_0}=-1
$$ zu $$
  P_2(x)=1+\frac{0}{1!}\cdot(x-x_0)-\frac{1}{2!}\cdot(x-x_0)^2=1-\frac{1}{2}\cdot\left(x-\frac{\pi}{2}\right)^2
$$ Wird $x\mapsto P_2(x)$ als quadratische Funktion betrachtet, so beschreibt das Taylorpolynom $P_2(x)$ eine nach 'unten' geöffnete Parabel mit Scheitelpunkt $S\left(\frac{\pi}{2},1\right)$, die gegenüber der Normalparabel mit dem Faktor $-\frac{1}{2}$ gestaucht ist.

![Taylorpolynom](img/mat-bild-05.png "_Fig._ Graphen der Funktionen $f$ (schwarz) und des Taylorpolynoms $P_2$ zu $f$ an der Stelle $x_0=\frac{\pi}{2}$.")

Die Berechnung des Taylorpolynoms $P_n(x)$ $n$-ten Grades einer mindestens $n$-mal stetig differenzierbaren reellen Funktion $f:x\mapsto y=f(x)$ ist nachfolgend unter Benutzung der Javascript Bibliothek Algebrite ausgeführt. Die beiden letzten Argumente in der Funktion *taylor(.)* bezeichnen dessen Grad $n$ und die Entwicklungsstelle $x_0$.

```javascript
f=sin(x)
p=taylor(f,x,2,pi/2)
p
coeff(p,x,2)
```
@Algebrite.eval

**Bemerkung 1.** Für $$
  \lim_{n\to\infty}{R_n(x)}=0
$$ ist nach dem vorstehenden Satz 3 $$
  f(x)=\lim_{n\to\infty}{P_n(x)}=f(x_0)+\sum_{k=1}^\infty{\frac{f^{(k)}(x_0)}{k!}\cdot(x-x_0)^k}
$$ d. h. das Taylorpolynom $P_n(x)$ konvergiert in diesem Fall gegen $f(x)$ auf $U(x_0)$.

Wird das Restglied $R_n(x)$ in der Darstellung aus Satz 3 weggelassen, so ist $P_n(x)$ in der Umgebung $U(x_0)$ nur eine Näherung von $f(x)$.

>**Definition 2.** (Taylorreihe)
>
>Sei $f$ wie oben definiert. $f$ werde in $U(x_0)$ beliebig of stetig differenzierbar vorausgesetzt, wobei $f^{(k)}(x_0)$ die $k$-te Ableitung der Funktion $f$ in $x_0$ bezeichnet. Dann heißt $$
  f(x_0)+\sum_{k=1}^\infty{\frac{f^{(k)}(x_0)}{k!}\cdot(x-x_0)^k}=
  f(x_0)+\frac{f^{\prime}(x_0)}{1!}\cdot(x-x_0)^1+
  \frac{f^{\prime\prime}(x_0)}{2!}\cdot(x-x_0)^2+...
$$ die **Taylorreihe** von $f$ in $x_0$.
>
>Falls die Entwicklungsstelle $x_0=0$, so wird die Taylorreihe auch **McLaurin-Reihe** genannt.

**Bemerkung 2.** Die zum Taylorpolynom gebildete Funktion $x\mapsto P_n(x)$ besitzt in $x_0\in U(x_0)\subseteq D_f$ mit $f$

1. denselben Funktionswert $P_n(x_0)=f(x_0)$, da $$
  P_n(x_0)=f(x_0)+\sum_{k=1}^n{\frac{f^{(k)}(x_0)}{k!}\cdot(x_0-x_0)^k}=f(x_0)
$$
2. übereinstimmende Ableitungen $$
  P_n^{(k)}(x_0)=\left.\frac{\mathrm{d}}{\mathrm{d}x}{P_n(x)}\right|_{x=x_0}=f^{(k)}(x_0)
$$ für $k\in{1,2,...,n}$, da unter Benutzung der $k$-ten Ableitung $P_n^{(k)}$ $$
    P_n^{(k)}(x)=f^{(k)}(x_0)+\sum_{i=k+1}^n{\left(\frac{f^{(i)}(x_0)}{i!}\cdot(x-x_0)^{i-k}\cdot\frac{i!}{(i-k)!}\right)}
$$ und somit $P_n^{(k)}(x_0)=f^{(k)}(x_0)$.

---

Ein Vergleich der $k$-ten Ableitungen des Taylorpolynoms $P_n(x)$ $n$-ten Grades  $(k\leq n)$ einer mindestens $n$-mal stetig differenzierbaren reellen Funktion $f:x\mapsto y=f(x)$ an der Entwicklungsstelle $x_0\in D_f$ kann interaktiv unter Benutzung der Javascript Bibliothek Algebrite durchgeführt werden. Neben den Ableitungen $P_n^{(k)}(x)$ und $f^{(k)}(x)$ wird an letzter Stelle die Differenz $P_n^{(k)}(x_0)-f^{(k)}(x_0)$ ausgegeben.

```javascript
f=sin(x)
n=3
x0=1
p=taylor(f,x,n,x0)
k=1
pk=d(p,x,k)
fk=d(f,x,k)
pk
fk
subst(x0,x,pk)-subst(x0,x,fk)
```
@Algebrite.eval


In den beiden nachstehenden Videos wird die Differentiation / Integration von Potenzreihen am Beispiel der Taylorentwicklung der Exponentialfunktion zu exp(x) erklärt.

!?[Ableitung der Taylorreihe](https://www.youtube.com/watch?v=DHTXqFjwJIA&list=PLLTAHuUj-zHjs82YCjiSUeWnNGZkEePIE&index=40)

!?[Integration der Taylorreihe](https://www.youtube.com/watch?v=UDAqeXyBmf0&list=PLLTAHuUj-zHjs82YCjiSUeWnNGZkEePIE&index=41)

**Beispiel 3.** Die Funktion $f:\mathbb{R}\to\mathbb{R}$ mit $$
  f:x\mapsto y=f(x)=\sin{x}
$$ soll an der Stelle $x_0=1$ in Ihre Potenzreihe entwickelt werden.

Die $k$-ten Ableitungen $f^{(k)}(x)$ berechnen sich einsichtig zu $$
  f^{(k)}(x)=\left\{
    \begin{array}{rcl}
       \sin{x} & \text{für} & k=4\cdot m \\
       \cos{x} & \text{für} & k=4\cdot m+1 \\
      -\sin{x} & \text{für} & k=4\cdot m+2 \\
      -\cos{x} & \text{für} & k=4\cdot m+3
    \end{array}
  \right.
$$ worin $m\in\mathbb{N}$. Für $m=0$ wird $f^{(0)}(x)=f(x)$ vereinbart. Hiermit ergeben sich die Koeffizienten der Potenzreihe $$
  a_k=\frac{f^{(k)}(x_0)}{k!}=\left\{
    \begin{array}{rcl}
       \frac{\sin{1}}{k!} & \text{für} & k=4\cdot m \\
       \frac{\cos{1}}{k!} & \text{für} & k=4\cdot m+1 \\
      -\frac{\sin{1}}{k!} & \text{für} & k=4\cdot m+2 \\
      -\frac{\cos{1}}{k!} & \text{für} & k=4\cdot m+3
    \end{array}
  \right.
$$ Für den Konvergenzradius folgt $$
  \left|\frac{a_k}{a_{k+1}}\right|=\left\{
    \begin{array}{rcl}
      \tan{1}\cdot\frac{(k+1)!}{k!} & \text{für} & k=2\cdot n \\
      \cot{1}\cdot\frac{(k+1)!}{k!} & \text{für} & k=2\cdot n+1
    \end{array}
  \right.
$$ mit $n\in\mathbb{N}$. Für den Grenzübergang $n\to\mathbb{R}$ ergibt sich der Konvergenzradius $r=\infty$ und somit der Konvergenzbereich $D_1=\mathbb{R}$. Die Taylorreihe zur Funktion $f$ lässt sich damit angeben $$
  \sin{1}+\frac{\cos{1}}{1!}\cdot(x-1)-\frac{\sin{1}}{2!}\cdot(x-1)^2-
  \frac{\cos{1}}{3!}\cdot(x-1)^3+\frac{\sin{1}}{1!}\cdot(x-1)^4+...
$$ beziehungsweise - unter Verwendung des Summenzeichens - $$
  \sum_{m=0}^\infty{\frac{\sin{1}}{(4\cdot m)!}\cdot(x-1)^{4\cdot m}}+
  \sum_{m=0}^\infty{\frac{\cos{1}}{(4\cdot m+1)!}\cdot(x-1)^{4\cdot m+1}}-
  \sum_{m=0}^\infty{\frac{\sin{1}}{(4\cdot m+2)!}\cdot(x-1)^{4\cdot m+2}}-
  \sum_{m=0}^\infty{\frac{\cos{1}}{(4\cdot m+3)!}\cdot(x-1)^{4\cdot m+3}}
$$ mit $x\in\mathbb{R}$. (Die hier vorgenommene Umordnung der Summanden in der Darstellung ist zulässig, da für jede Wahl von $x$ die zugehörige Zahlenreihe absolut konvergent ist.)

Wird die Reihenentwicklung nach dem $k$-ten Glied abgebrochen entsteht das Taylorpolynom $k$-ter Ordnung. Die nachstehende Abbildung zeigt die Taylorpolynome der Ordnungen $k=1$ (rot), $k=3$ (lila) und $k=5$ (blau).

![Taylorpolynom1](img/mat-bild-06.png "_Fig._ Graphen der Funktionen $f$ (schwarz) und der Taylorpolynome $P_1$ (rot), $P_3$ (lila) und $P_5$ (blau) zu $f$ an der Stelle $x_0=1$.")

---

**Beispiel 4.** Die Funktion $f:\mathbb{R}\to\mathbb{R}$ mit $$
  f:x\mapsto y=f(x)=\exp{x}\cdot\arctan{x}
$$ kann nicht elementar integriert werden.

```javascript
f=exp(x)*arctan(x)
integral(f)
```
@Algebrite.eval

*Ansatz*: Zur Ermittlung des unbestimmten Integrals von $f$

1. wird $f$ als Produkt der Funktionen $$
  f_1:x\mapsto y=f_1(x)=\exp{x}\quad\text{und}\quad
  f_2:x\mapsto y=f_2(x)=\arctan{x}
$$ mit $x\in\mathbb{R}$ aufgefasst.
2. Unter Benutzung der Reihenentwicklung der Funktionen $f_1$ und $f_2$ werden diese nach Folgerung 2 auf einem gemeinsamen Konvergenzbereich (gliedweise) multipliziert.
3. Das Produkt beider Potenzreihen konvergiert (mindestens) auf dem gemeinsamen Konvergenzbereich und wird dort gliedweise integriert.

Die Taylorreihe der Funktion $f_1$ an der Entwicklungstelle $x_0=0$ ist $$
  f_1(x)=\exp{x}=\sum_{n=0}^\infty{\frac{x^n}{n!}}=1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+...
$$ mit Konvergenzbereich $D_1=\mathbb{R}$. (Bitte nachrechnen.)

Zur Berechnung der Taylorreihe der Funktion $f_2$ kann man (alternativ) zunächst $f_2^\prime$ in eine Potenzreihe entwickeln und diese anschließend gliedweise integrieren. Es ist $$
  f_2^\prime(x)=\frac{1}{1+x^2}=\frac{1}{1-(-x^2)}=\sum_{n=0}^\infty{\left(-x^2\right)^n}=\sum_{n=0}^\infty{\left((-1)^n\cdot x^{2\cdot n}\right)}
$$ als Summenfunktion einer geometrischen Reihe. Der Konvergenzbereich ist $|x|<1$. Nach Folgerung 2 ergibt sich $$
  f_2(x)=\sum_{n=0}^\infty{\left(\frac{(-1)^n}{2\cdot n+1}\cdot x^{2\cdot n+1}\right)}
$$ mit $|x|<1$.

Die Potenzreihe der Funktion $f$ ergibt sich durch gliedweise Multiplikation der Reihen für $f_1$ und $f_2$ $$
  f_1(x)\cdot f_2(x)=\left(\sum_{n=0}^\infty{\frac{x^n}{n!}}\right)\cdot
  \left(\sum_{k=0}^\infty{\left(\frac{(-1)^k}{2\cdot k+1}\cdot x^{2\cdot k+1}\right)}\right)=
  \sum_{i=1}^\infty{\left(x^i\cdot\left(\sum_{k\leq \frac{i-1}{2}}{\frac{(-1)^k}{2\cdot k+1}\cdot\frac{1}{(i-(2\cdot k+1))!}}\right)\right)}
$$ mit $x\in(-1,1)$ beziehungsweise $$
  f_1(x)\cdot f_2(x)=\sum_{i=1}^\infty{b_i\cdot x^i}
$$ mit

<!-- data-type="none" -->
| $i$ | $k$ | $b_i$ |
| :--- | :--- | :--- |
| $1$ | $0$ | $1$ |
| $2$ | $0$ | $1$ |
| $3$ | $\leq 1$ | $1\cdot\frac{1}{2!}-\frac{1}{3}\cdot\frac{1}{0!}=\frac{1}{6}$ |
| $4$ | $\leq 1$ | $1\cdot\frac{1}{3!}-\frac{1}{3}\cdot\frac{1}{1!}=-\frac{1}{6}$ |
| $5$ | $\leq 2$ | $1\cdot\frac{1}{4!}-\frac{1}{3}\cdot\frac{1}{2!}+\frac{1}{5}\cdot\frac{1}{0!}=\frac{3}{40}$ |
| $\vdots$ | $\vdots$ | $\vdots$ |

Die entstandene Reihe zu $f(x)=f_1(x)\cdot f_2(x)$ konvergiert mindestens im Intervall $(-1,1)$ und darf gliedweise integriert werden $$
  \int{f(x)}{\mathrm{d}x}=\sum_{i=1}^\infty{\frac{b_i}{i+1}\cdot x^{i+1}}+c=\frac{1}{2}\cdot x^2+\frac{1}{3}\cdot x^3+\frac{1}{24}\cdot x^4-\frac{1}{30}\cdot x^5+\frac{1}{80}\cdot x^6 +...
$$ mit $c\in\mathbb{R}$. Wird die Reihe abgebrochen, so entsteht eine 'Näherung' für das unbestimmte Integral.

Wird die Berechnung einer Näherung des unbestimmten Integrals unter Benutzung der Javascript Bibliothek Algebrite durchgeführt, ist darauf zu achten, dass die aus den Taylorpolynomen berechneten Koeffizienten $a_i$ in der Näherung für $\int{f}{\mathrm{d}x}$ nur für hinreichend kleine $i$ mit den Koeffizienten $b_i/(i+1)$ übereinstimmen.

```javascript
f1=taylor(exp(x),x,4,0)
f2=taylor(arctan(x),x,4,0)
f=f1*f2
f
integral(f,x)
```
@Algebrite.eval

**Bemerkung 3.** Ein Taylorpolynom lässt sich für reelle Funktionen zweier reeller Veränderlicher konstruieren. Sei hierfür $$
  f:(x,y)\mapsto z=f(x,y)\quad\text{mit}\quad (x,y)\in D\subset\mathbb{R}^2
$$ in Umgebung von $(x_0,y_0)\in D$ $(k+1)$-mal stetig partiell differenzierbar. Dann heißt $$
  P_n(x,y)=f(x_0,y_0)+
  \sum_{k=1}^n{\frac{1}{k!}\left((x-x_0)\frac{\partial}{\partial x}+(y-y_0)\frac{\partial}{\partial y}\right)^k\cdot f(x_0,y_0)}
$$ das **Taylor-Polynom** $n$-ter Ordnung zu $f$ und $$
  R_n(x,y)=\frac{1}{(k+1)!}\left((x-x_0)\frac{\partial}{\partial x}+(y-y_0)\frac{\partial}{\partial y}\right)^{k+1} f(\xi_0,\chi_0),\quad (\xi_0,\chi_0)\in D
$$ das Restglied $(n+1)$-ter Ordnung.

Hierin kann das Argument der Summe in $P_n(x,y)$ mithilfe des Binomischen Lehrsatzes ausgewertet werden. Für $n=1$ ergibt sich beispielsweise $$
  \frac{1}{1!}\left(f_x(x_0,y_0)\cdot(x-x_0)^1+f_y(x_0,y_0)\cdot(y-y_0)^1\right)
$$ für $n=2$ $$
  \frac{1}{2!}\left(f_{xx}(x_0,y_0)\cdot(x-x_0)^2+2f_{xy}(x_0,y_0)\cdot(x-x_0)(y-y_0)+f_{yy}(x_0,y_0)\cdot(y-y_0)^2\right)
$$

**Beispiel 5.** Es ist das Taylorpolynom $3$-ter Ordnung für die Funktion $$
  f:(x,y)\mapsto z=f(x,y)=\exp{x}\cdot\sin{y}\,,\quad (x,y)\in\mathbb{R}^2
$$ an der Stelle $(x_0,y_0)=(0,0)$ zu berechnen.

1. Der Funktionswert an der Stelle $(0,0)$ ist $f(0,0)=\exp{0}\cdot\sin{0}=0$.
2. Die partiellen ersten Ableitungen von $f$ berechnen sich zu $$
  f_x(x,y)=f(x,y)\,,\quad f_y(x,y)=\exp{x}\cdot\cos{y}
$$ und damit $f_x(0,0)=0$ und $f_y(0,0)=1$.
3. Die partiellen zweiten Ableitungen von $f$ berechnen sich zu $$
  f_{xx}(x,y)=f(x,y)\,,\quad
  f_{xy}(x,y)=f_{yx}(x,y)=\exp{x}\cdot\cos{y}\quad\text{und}\quad
  f_{yy}(x,y)=-\exp{x}\cdot\sin{y}
$$ und somit $$
  f_{xx}(0,0)=f_{yy}(0,0)=0\quad\text{und}\quad
  f_{xy}(0,0)=f_{yx}(0,0)=1
$$
4. Entsprechend berechnen sich die partiellen dritten Ableitungen von $f$ $$
  f_{xxx}(x,y)=f(x,y)\quad\text{mit}\quad f_{xxx}(0,0)=0
$$ und $$
    f_{xxy}(x,y)=f_{xyx}(x,y)=f_{yxx}(x,y)=\exp{x}\cdot\cos{y}\quad\text{mit}\quad f_{xxy}(0,0)=1
$$ und $$
    f_{xyy}(x,y)=f_{yxy}(x,y)=f_{yyx}(x,y)=-\exp{x}\cdot\sin{y}\quad\text{mit}\quad f_{xyy}(0,0)=0
$$ sowie $$
    f_{yyy}(x,y)=-\exp{x}\cdot\cos{y}\quad\text{mit}\quad f_{yyy}(0,0)=-1
$$
5. Aus dem berechneten Funktionswert und den partiellen Ableitungen lässt sich nun das Taylorpolynom dritter Ordnung an der Entwicklungsstelle $(0,0)$ berechnen. $$
  P_3(x,y)=0+y+x\cdot y+\frac{1}{6}\cdot\left(3\cdot x^2\cdot y-y^3\right)=
  x+x\cdot y+\frac{1}{2}\cdot x^2\cdot y-\frac{1}{6}\cdot y^3
$$


Sicher gewußt
=============


Testen Sie Ihr Wissen zu den Themen dieses Abschnitts.

---

**Frage 1.** Berechnen Sie den Konvergenzbereich der Potenzreihe $$
  \sum_{k=1}^\infty{\frac{(x+2)^k}{k^3\cdot 2^k}}
$$

[( )] $$x\in[0,4]$$
[( )] $$x\in\left[-\frac{5}{2},\frac{5}{2}\right]$$
[(X)] $$x\in[-4,0]$$
[[?]] Der Konvergenzradius $r$ und die Entwicklungsstelle $x_0$ der Reihe sind zu berechnen. Der Konvergenzbereich ist das Intervall $(x_0-r,x_0+r)$. Die Konvergenz der Potenzreihe an den Intervallgrenzen $x=x_0\pm r$ ist separat zu untersuchen.
****************************************

Die Entwicklungsstelle $x_0=-2$ ist abzulesen aus $x+2=x-(-2)$ in der allgemeinen Darstellung der Potenzreihe.

Die Koeffizienten der Potenzreihe sind $$
  a_k=\frac{1}{k^3\cdot 2^k}
$$ Hieraus berechnet sich der Konvergenzradius $r$ $$
  r=\lim_{k\to\infty}\left|\frac{(k+1)^3\cdot 2^{k+1}}{k^3\cdot 2^k}\right|=
  2\cdot\lim_{k\to\infty}\left|\frac{(k+1)^3}{k^3}\right|=2
$$ Hieraus ergibt sich der Konvergenzbereich $K=(-4,0)$. An der Grenze $x=-4$ ergibt sich die konvergente Reihe $$
  \sum_{k=1}^\infty{\frac{(-2)^k}{k^3\cdot 2^k}}=
  \sum_{k=1}^\infty{\frac{(-1)^k}{k^3}}=-1+\frac{1}{8}-\frac{1}{27}+\frac{1}{64}\mp...
$$ (Konvergenz nach Leibnitzkriterium), für $x=4$ die ebenfalls konvergente Reihe $$
  \sum_{k=1}^\infty{\frac{2^k}{k^3\cdot 2^k}}=
  \sum_{k=1}^\infty{\frac{1}{k^3}}=1+\frac{1}{8}+\frac{1}{27}+\frac{1}{64}+...
$$

****************************************

---

**Frage 2.** Berechnen Sie zur Funktion $$
  f:x\mapsto y=f(x)=\ln{(2\cdot x+1)}\,,\quad x>-\frac{1}{2}
$$ das Taylorpolynom $3$-ten Grades an der Stelle $x_0=0$.

[( )] $$ 2\cdot x-2\cdot x^2+\frac{8}{3}\cdot x^3\pm... $$
[(X)] $$ 2\cdot x-2\cdot x^2+\frac{8}{3}\cdot x^3 $$
[( )] $$ 2\cdot x-4\cdot x^2+16\cdot x^3 $$
[[?]] Das Taylorpolynom $P_n(x)$ $n$-ter Ordnung einer mindestens $n$-mal stetig differenzierbaren Funktion berechnet sich an der Entwicklungsstelle $x_0$ nach der Formel $$
  P_n(x)=f(x_0)+\sum_{k=1}^n{\frac{f^{(k)}(x_0)}{k!}\cdot(x-x_0)^k}
$$
****************************************

Die ersten drei Ableitungen berechnen sich $$
  f^\prime(x)=\frac{2}{2\cdot x+1}\,,\quad
  f^{\prime\prime}(x)=-\frac{4}{\left(2\cdot x+1\right)^2}\quad\text{und}\quad
  f^{\prime\prime\prime}(x)=\frac{16}{\left(2\cdot x+1\right)^3}
$$ und also an der Entwicklungsstelle $x_0=0$ $$
  f^\prime(0)=2\,,\quad
  f^{\prime\prime}(0)=-4\quad\text{und}\quad
  f^{\prime\prime\prime}(0)=16
$$ Das Taylorpolynom dritten Grades an der Stelle $x_0=0$ berechnet sich hiermit $$
  P_3(x)=f(0)+\frac{1}{1!}\cdot f^\prime(0)\cdot x
  +\frac{1}{2!}\cdot f^{\prime\prime}(0)\cdot x^2
  +\frac{1}{3!}\cdot f^{\prime\prime\prime}(0)\cdot x^3=
  2\cdot x-2\cdot x^2+\frac{8}{3}\cdot x^3
$$ Es ist durch die Koeffizienten $a_0=0$, $a_1=\frac{2}{1!}=2$, $a_2=-\frac{4}{2!}=-2$ und $a_3=\frac{16}{3!}$ eindeutig festgelegt.

****************************************


[^1]: Die Summe $s_a(x)$ darf auf dem Konvergenzbereich $D_1$ als Funktion $s_a:x\mapsto s(x)$ aufgefasst werden, ebs. $s_b(x)$.


### Fourierreihen


Ziel ist es, eine periodische Funktion in eine unendliche Reihe periodischer Funktionen zu entwickeln.

---

Spezialfall
===========

Gegeben sei zunächst eine reelle Funktion $f$ mit $$
  f:x\mapsto y=f(x)\,,\quad x\in D\subseteq\mathbb{R}
$$ welche <span style="color: orange" > periodisch mit Periode $2\pi$ </span> ist, d. h. $$
  f(x)=f(x+2\cdot\pi)\quad\forall x\in D
$$ $f$ darf in $D$ endlich viele Definitionslücken beziehungsweise Sprünge endlicher Höhe besitzen.


Ansatzgleichung
---------------


Mit der Gleichung $$
  f(x)=\sum_{k=0}^\infty{\left(A_k\cdot\sin{(k\cdot x+\varphi_k)}\right)}
$$ und zu bestimmenden Parametern $A_k\geq0$ und $\varphi_k$ für $k\in\mathbb{N}$ wird eine unendliche Reihe von Sinusfunktionen angesetzt, deren Perioden $p_k=2\pi/k$ sind. Unter Benutzung des Additionstheorems für den Sinus folgt hieraus $$
  f(x)=A_0\cdot\sin{\varphi_0}+\sum_{k=1}^\infty{\left(
    A_k\cdot\cos{\varphi_k}\cdot\sin{(k\cdot x)}+
    A_k\cdot\sin{\varphi_k}\cdot\cos{(k\cdot x)}
  \right)}
$$ was zur allgemeinen Darstellung einer **Fourierreihe** $$
f(x)=\frac{a_0}{2}+\sum_{k=1}^\infty{\left(
    a_k\cdot\cos{(k\cdot x)}+
    b_k\cdot\sin{(k\cdot x)}
\right)}
$$ mit zu bestimmenden **Fourierkoeffizienten** $a_k$ und $b_k$ führt.


Fourierkoeffizienten
--------------------


Für die Berechnung der Fourierkoeffizienten wird $D\supseteq(-\pi,\pi)$ vorausgesetzt.

1. Zur Berechnung des Fourierkoeffizienten $a_0$ werden beide Seiten der Ansatzgleichung über dem Intervall $(-\pi,\pi)$ integriert. Es ergibt sich (ohne Nachweis) $$
  \int_{-\pi}^\pi{f(x)}\,\mathrm{d}x=\int_{-\pi}^\pi{a_0}\,\mathrm{d}x+
  \sum_{i=1}^\infty{a_k\cdot\int_{-\pi}^\pi{\cos{(k\cdot x)}}\,\mathrm{d}x}+
  \sum_{i=1}^\infty{b_k\cdot\int_{-\pi}^\pi{\sin{(k\cdot x)}}\,\mathrm{d}x}=0
$$ woraus sich unter Beachtung von $$
  \int_{-\pi}^\pi{\cos{(k\cdot x)}}\,\mathrm{d}x=0\quad\text{und}\quad
  \int_{-\pi}^\pi{\sin{(k\cdot x)}}\,\mathrm{d}x=0
$$ für beliebige $k\in\mathbb{Z}$ der Fourierkoeffizient $a_0$ berechnet
>$$
  a_0=\frac{1}{\pi}\cdot\int_{-\pi}^\pi{f(x)}\,\mathrm{d}x
$$
2. Die Fourierkoeffizienten $a_k$, $k\geq1$, berechnen sich aus dem Ansatz $$
  \int_{-\pi}^\pi{f(x)\cdot\textcolor{orange}{\cos(n\cdot x)}}\,\mathrm{d}x=
  a_0\cdot\int_{-\pi}^\pi{\textcolor{orange}{\cos(n\cdot x)}}\,\mathrm{d}x+
  \sum_{i=1}^\infty{a_k\cdot\int_{-\pi}^\pi{\left(\textcolor{orange}{\cos(n\cdot x)}\cdot\cos{(k\cdot x)}\right)}\,\mathrm{d}x}+
  \sum_{i=1}^\infty{b_k\cdot\int_{-\pi}^\pi{\left(\textcolor{orange}{\cos(n\cdot x)}\cdot\sin{(k\cdot x)}\right)}\,\mathrm{d}x}
$$ für ein $n\in\mathbb{N}\setminus\{0\}$. Darin berechnen sich $$
  \int_{-\pi}^\pi{\cos(n\cdot x)}\,\mathrm{d}x=\left.\frac{1}{n}\cdot\sin{(n\cdot x)}\right|_{-\pi}^\pi=0
$$ ebenso - unter partieller Integration $$
  \int_{-\pi}^\pi{\left(\cos(n\cdot x)\cdot\cos{(k\cdot x)}\right)}\,\mathrm{d}x=
  \left.\frac{1}{n}\cdot\sin{(n\cdot x)}\cdot\cos{(k\cdot x)}\right|_{-\pi}^\pi+
  \frac{k}{n}\cdot\int_{-\pi}^\pi{\sin{(n\cdot x)}\cdot\sin{(k\cdot x)}}\,\mathrm{d}x
$$ was für $n\not=k$ unter nochmaliger Integration auf $$
  \int_{-\pi}^\pi{\left(\cos(n\cdot x)\cdot\cos{(k\cdot x)}\right)}\,\mathrm{d}x=
  \left.{\frac{n}{n^2-k^2}\cdot\sin{(n\cdot x)}\cdot\cos{(k\cdot x)}-\frac{k}{n^2-k^2}\cdot\cos{(n\cdot x)}\cdot\sin{(k\cdot x)}}\right|_{-\pi}^\pi=0
$$ führt, wohingegen für $n=k$ unter Nutzung des Additionstheorems für den Sinus folgt $$
  \int_{-\pi}^\pi{\left(\cos^2(k\cdot x)\right)}\,\mathrm{d}x=\left.{\frac{1}{4\cdot k}\cdot\sin{(2\cdot k\cdot x)}+\frac{x}{2}}\right|_{-\pi}^\pi=\pi
$$ Ebenso berechnet sich $$
  \int_{-\pi}^\pi{\left(\cos(n\cdot x)\cdot\sin{(k\cdot x)}\right)}\,\mathrm{d}x=0
$$ für alle $n$. Aus diesen bestimmten Integralen ergibt sich die Berechnung der Fourierkoeffizienten $a_k$
>$$
  a_k=\frac{1}{\pi}\cdot\int_{-\pi}^\pi{f(x)\cdot\cos{(k\cdot x)}}\,\mathrm{d}x\,,\quad  k\geq1
$$
3. Die Fourierkoeffizienten $k_k$, $k\geq1$, berechnen sich aus dem Ansatz $$
  \int_{-\pi}^\pi{f(x)\cdot\textcolor{orange}{\sin(n\cdot x)}}\,\mathrm{d}x=
  a_0\cdot\int_{-\pi}^\pi{\textcolor{orange}{\sin(n\cdot x)}}\,\mathrm{d}x+
  \sum_{i=1}^\infty{a_k\cdot\int_{-\pi}^\pi{\left(\textcolor{orange}{\sin(n\cdot x)}\cdot\cos{(k\cdot x)}\right)}\,\mathrm{d}x}+
  \sum_{i=1}^\infty{b_k\cdot\int_{-\pi}^\pi{\left(\textcolor{orange}{\sin(n\cdot x)}\cdot\sin{(k\cdot x)}\right)}\,\mathrm{d}x}
$$ für ein $n\in\mathbb{N}\setminus\{0\}$. Darin berechnen sich $$
  \int_{-\pi}^\pi{\sin(n\cdot x)}\,\mathrm{d}x=\left.-\frac{1}{n}\cdot\cos{(n\cdot x)}\right|_{-\pi}^\pi=0
$$ Ebenso berechnet sich - vergleiche Punkt 2 - $$
  \int_{-\pi}^\pi{\left(\sin(n\cdot x)\cdot\cos{(k\cdot x)}\right)}\,\mathrm{d}x=0
$$ für alle $n$. Unter Benutzung partieller Integration berechnet sich $$
  \int_{-\pi}^\pi{\left(\sin(n\cdot x)\cdot\sin{(k\cdot x)}\right)}\,\mathrm{d}x=
  \left.-\frac{1}{n}\cdot\cos{(n\cdot x)}\cdot\sin{(k\cdot x)}\right|_{-\pi}^\pi+
  \frac{k}{n}\cdot\int_{-\pi}^\pi{\cos{(n\cdot x)}\cdot\cos{(k\cdot x)}}\,\mathrm{d}x
$$ was für $n\not=k$ unter nochmaliger Integration auf $$
  \int_{-\pi}^\pi{\left(\sin(n\cdot x)\cdot\sin{(k\cdot x)}\right)}\,\mathrm{d}x=
  \left.{-\frac{n}{n^2-k^2}\cdot\cos{(n\cdot x)}\cdot\sin{(k\cdot x)}+\frac{k}{n^2-k^2}\cdot\sin{(n\cdot x)}\cdot\cos{(k\cdot x)}}\right|_{-\pi}^\pi=0
$$ führt, wohingegen für $n=k$ unter Nutzung des Additionstheorems für den Sinus folgt $$
  \int_{-\pi}^\pi{\left(\sin^2(k\cdot x)\right)}\,\mathrm{d}x=\left.{-\frac{1}{4\cdot k}\cdot\sin{(2\cdot k\cdot x)}+\frac{x}{2}}\right|_{-\pi}^\pi=\pi
$$ Aus diesen bestimmten Integralen ergibt sich die Berechnung der Fourierkoeffizienten $a_k$
>$$
  b_k=\frac{1}{\pi}\cdot\int_{-\pi}^\pi{f(x)\cdot\sin{(k\cdot x)}}\,\mathrm{d}x\,,\quad  k\geq1
$$

Der nachstehende Satz fasst Fourierreihenentwicklung einer periodischen Funktion mit $p=2\cdot\pi$ zusammen.

>**Satz 1.** Eine periodische Funktion $f:x\mapsto y=f(x)$, $x\in D$ mit der Periode $p=2\cdot\pi$ lässt sich darstellen als Fourierreihe $$
  S_f(x)=\frac{a_0}{2}+\sum_{k=1}^\infty{\left(a_k\cdot\cos{(k\cdot x)}+b_k\cdot\sin{(k\cdot x)}\right)}
$$ mit den Koeffizienten $$
  a_0=\frac{1}{\pi}\cdot\int_{-\pi}^\pi{f(x)}\,\mathrm{d}x\,,\quad
  a_k=\frac{1}{\pi}\cdot\int_{-\pi}^\pi{f(x)\cdot\cos{(k\cdot x)}}\,\mathrm{d}x\quad\text{und}\quad
  b_k=\frac{1}{\pi}\cdot\int_{-\pi}^\pi{f(x)\cdot\sin{(k\cdot x)}}\,\mathrm{d}x
$$ mit $k\geq1$.

**Bemerkung 1.** Durch Abbruch der Fourier-Reihe nach endlich vielen Gliedern erhält man $$
  S_f(x)\approx\frac{a_0}{2}+\sum_{k=1}^n{\left(a_k\cos{(k\cdot\omega\cdot x)}+b_k\sin{(k\cdot\omega\cdot x)}\right)}
$$ diese wird *Näherung der Ordnung $n$* $(n\geq1)$ genannt. In der Umgebung einer Sprungstelle der Grundfunktion tritt dabei für abgebrochene Fourierreihen ein Überschwingen auf, dass unabhängig von der Ordnung $n$ cirka neun Prozent der Sprunghöhe beträgt. (*[Gibbsches Phänomen](https://en.wikipedia.org/wiki/Gibbs_phenomenon)*)

---

 Allgemeiner Fall
=================


Gegeben sei nun eine reelle Funktion $f$ mit $$
  f:x\mapsto y=f(x)\,,\quad x\in D\subseteq\mathbb{R}
$$ welche <span style="color: orange" > periodisch mit Periode $p>0$ </span> ist, d. h. $$
  f(x)=f(x+p)\quad\forall x\in D
$$ $f$ darf in $D$ endlich viele Definitionslücken beziehungsweise Sprünge endlicher Höhe besitzen.

Durch die Substitution $$
  \left(z\mapsto x=\frac{p}{2\cdot\pi}\cdot z\right)\quad\leftrightarrow\quad
  \left(x\mapsto z=\frac{2\cdot\pi}{p}\cdot x\right)
$$ ergeben sich $$
  f(x)=f\left(\frac{p}{2\cdot\pi}\cdot z\right)=g(z)
$$ und die zugehörige  Fourierreihe $$
  \frac{a_0}{2}+\sum_{k=1}^\infty{
    \left(a_k\cdot\cos{(k\cdot z)}+b_k\cdot\sin{(k\cdot z)}\right)
  }=\frac{a_0}{2}+\sum_{k=1}^\infty{
    \left(a_k\cdot\cos{\left(k\cdot\frac{2\cdot\pi}{p}\cdot x\right)}+b_k\cdot\sin{\left(k\cdot\frac{2\cdot\pi}{p}\cdot x\right)}\right)
  }
$$ Die Fourierkoeffizienten berechnen unter der Substitution zu
>$$
  a_0=\frac{1}{\pi}\cdot\int_{-\pi}^\pi{g(z)}\,\mathrm{d}z=\frac{2}{p}\cdot\int_{-\frac{p}{2}}^\frac{p}{2}{f(x)}\,\mathrm{d}x
$$

beziehungsweise
>$$
  a_k=\frac{1}{\pi}\cdot\int_{-\pi}^\pi{f(z)\cdot\cos{(k\cdot z)}}\,\mathrm{d}z=\frac{2}{p}\cdot\int_{-\frac{p}{2}}^\frac{p}{2}{\left(\cos{\left(k\cdot\frac{2\cdot\pi}{p}\cdot x\right)}\cdot f(x)\right)}\,\mathrm{d}x\,,\quad k\geq1
$$

sowie
>$$
  b_k=\frac{1}{\pi}\cdot\int_{-\pi}^\pi{f(z)\cdot\sin{(k\cdot z)}}\,\mathrm{d}z=\frac{2}{p}\cdot\int_{-\frac{p}{2}}^\frac{p}{2}{\left(\sin{\left(k\cdot\frac{2\cdot\pi}{p}\cdot x\right)}\cdot f(x)\right)}\,\mathrm{d}x\,,\quad k\geq1
$$

Der Ausdruck $$
  \omega=\frac{2\cdot\pi}{p}
$$ wird *Kreisfrequenz* der Grundschwingung genannt.

---

**Beispiel 1.** Gegeben ist eine stückweise definierte Funktion $f$ mit $$
  f(x)=\left\{
      \begin{array}{rcl}
        1 & \text{für} & |x|\leq1 \\ 0 & \text{für} & (-2<x<-1)\vee(1<x\leq 2)
      \end{array}
    \right.
$$ Diese Funktion soll auf mittels $$
  f(x)=f(x+4)\quad\forall\; x\in\mathbb{R}
$$ periodisch fortgesetzt werden.

Die Periode der auf $\mathbb{R}$ periodisch fortgesetzten Funktion $f$ ist $p=4$, woraus sich deren Kreisfrequenz $\omega=\frac{\pi}{2}$ berechnet.

Die im Fourierreihenansatz auftretenden Fourierkoeffizienten berechnen sich $$
  a_0=\frac{1}{2}\cdot\int_{-2}^2{f(x)}\,\mathrm{d}x=
  \frac{1}{2}\cdot\left(
    \int_{-2}^{-1}{f(x)}\,\mathrm{d}x+
    \int_{-1}^{1}{f(x)}\,\mathrm{d}x+
    \int_{1}^{2}{f(x)}\,\mathrm{d}x
  \right)=
  \frac{1}{2}\cdot(0+2+0)=1
$$ unter Zerlegung des Integrationsgebietes gemäß der stückweisen Definition von $f(x)$, sowie entsprechend für $k\geq1$ $$
  a_k=\frac{1}{2}\cdot\int_{-2}^{2}{\left(f(x)\cdot\cos{\left(k\cdot\frac{\pi}{2}\cdot x\right)}\right)}\,\mathrm{d}x=
  \frac{1}{2}\cdot\int_{-1}^{1}{\cos{\left(k\cdot\frac{\pi}{2}\cdot x\right)}}\,\mathrm{d}x=
  \frac{1}{2}\cdot\left[\frac{2}{k\cdot\pi}\cdot\sin{\left(k\cdot\frac{\pi}{2}\cdot x\right)}\right]_{-1}^1=
  \frac{1}{k\cdot\pi}\cdot\left(2\cdot\sin{\left(k\cdot\frac{\pi}{2}\right)}\right)
$$ und somit $$
  a_k=\left\{
      \begin{array}{rcl}
        0 & \text{für} & k=2\cdot m \\
        \frac{2}{k\cdot\pi} & \text{für} & k=4\cdot m-3  \\
        -\frac{2}{k\cdot\pi} & \text{für} & k=4\cdot m-1 \\
      \end{array}
    \right.
$$ worin $m\in\mathbb{N}$ mit $m\geq1$ gewählt werden können. Die Fourierkoeffizienten $b_k$ der Sinusfunktionen im Reihenansatz berechnen sich hingegen $$
  b_k=\frac{1}{2}\cdot\int_{-2}^{2}{\left(f(x)\cdot\sin{\left(k\cdot\frac{\pi}{2}\cdot x\right)}\right)}\,\mathrm{d}x=

  \frac{1}{2}\cdot\left[-\frac{2}{k\cdot\pi}\cdot\cos{\left(k\cdot\frac{\pi}{2}\cdot x\right)}\right]_{-1}^1=
  \frac{1}{k\cdot\pi}\cdot\left(\cos{\left(k\cdot\frac{\pi}{2}\right)}-\cos{\left(-k\cdot\frac{\pi}{2}\right)}\right)=0
$$ für alle $k\in\mathbb{N}$ mit $k\geq1$. Hiernach treten die Sinusfunktionen $x\mapsto\sin{(k\cdot\omega\cdot x)}$ in der Fourierreihe nicht auf, was nicht überrascht, da die Grundfunktion $f$ und deren periodische Fortsetzung auf $\mathbb{R}$ gerade Funktionen sind, wohingegen die Sinusfunktionen für jede Wahl von $k$ ungerade Summanden liefern.

Die Berechnung der Fourierkoeffizienten kann interaktiv unter Benutzung der Javascript Bibliothek [Algebrite](http://algebrite.org/) nachstehend ausgeführt werden.

```javascript
f=1
ak=1/2*defint(f*cos(k*pi/2*x),x,-1,1)
bk=1/2*defint(f*sin(k*pi/2*x),x,-1,1)
bk
subst(1,k,ak)
```
@Algebrite.eval

Schließlich stellt sich die Fourierreihe der periodischen Grundfunktion dar $$
  x\mapsto S_f(x)=
  \frac{1}{2}+\sum_{m=1}^\infty{\left[\frac{2}{(4\cdot m-3)\cdot\pi}\cdot\cos{\left(\frac{4\cdot m-3}{2}\cdot\pi\cdot x\right)}-\frac{2}{(4\cdot m-1)\cdot\pi}\cdot\cos{\left(\frac{4\cdot m-1}{2}\cdot\pi\cdot x\right)}\right]}
$$ beziehungsweise - unter Weglassen des Summenzeichens - $$
  x\mapsto S_f(x)=
  \frac{1}{2}
  +\frac{2}{\pi}\cdot\cos{\left(\frac{1}{2}\cdot\pi\cdot x\right)}
  -\frac{2}{3\cdot\pi}\cdot\cos{\left(\frac{3}{2}\cdot\pi\cdot x\right)}
  +\frac{2}{5\cdot\pi}\cdot\cos{\left(\frac{5}{2}\cdot\pi\cdot x\right)}
  -\frac{2}{7\cdot\pi}\cdot\cos{\left(\frac{7}{2}\cdot\pi\cdot x\right)}
  \pm ...
$$

An den beiden Sprungstellen des Grundintervalls $(-2,2)$ gilt einsichtig $S_f(\pm1)=\frac{1}{2}$.

In der nachfolgenden Abbildung sind die Graphen der Grundfunktion $f$ sowie der bei $n=3$ beziehungsweise $n=7$ abgebrochenen Fourierreihenentwicklungen dargestellt.

![Fourierreihe](img/mat-bild-07.png "_Fig._ Graphen der Funktionen $f$ (dunkellila) und $x\mapsto S_3(x)$ (helllila) sowie $x\mapsto S_7(x)$ (blau), dargestellt in einem gemeinsamen Koordinatensystem. An den Sprungellen ist ein Überschwingen gegenüber der Grundfunktion zu beobachten.")

Der [Satz von Dirichlet](https://de.wikipedia.org/wiki/Dirichlet-Bedingung) trifft eine Aussage, unter welchen Voraussetzungen eine Fourierreihe zu einer gegebenen periodischen Funktion $f$ mit $p>0$ konvergiert. (hier ohne Beweis)

>**Satz 2.** (*Satz von Dirichlet*) Sind für eine gegebene periodische, reelle Funktion $f$ mit Definitionsbereich $D\subseteq\mathbb{R}$ und Periode $p>0$ folgende Bedingungen erfüllt,
>
>1. Das Intervall $(0,p)\subseteq D$ lässt sich in endlich viele Teilintervalle zerlegen, in denen $f(x)$ jeweils stetig und monoton ist.
>2. Ist $x_0\in(0,p)$ eine Unstetigkeitsstelle von $f(x)$, so existieren die einseitigen Grenzwerte $$
  \lim_{x\to x_0-0}{f(x)}\quad\text{und}\quad
  \lim_{x\to x_0+0}{f(x)}
$$
>
> so konvergiert die Funktionenreihe $S_f$ von $f$ gegen $$
  \lim_{n\to\infty}{S_f(x_0)}=\left\{
    \begin{array}{rl}
      f(x_0) & \text{falls $f(x)$ in $x_0$ stetig} \\
      \frac{1}{2}\cdot\left(\lim_{x\to x_0-0}{f(x)}+\lim_{x\to x_0+0}{f(x)}\right) & \text{sonst}
    \end{array}
  \right.
$$ Der Grenzwert in der letzten Formelzeile bildet das arithmetische Mittel des links- und rechtseitigen Grenzwertes an dieser Stelle.

**Bemerkung 2.** Zu einer periodischen, reellen Funktion $f$ mit Periode $p>0$ soll eine Fourierreihe $$
  S_f(x)=\frac{a_0}{2}+\sum_{k=1}^\infty{\left(a_k\cdot\cos{(k\cdot\omega\cdot x)}+b_k\cdot\sin{(k\cdot\omega\cdot x)}\right)}
$$ ermittelt werden. Der Aufwand zur Berechnung der Fourierkoeffizienten $a_0$ sowie $a_k$ und $b_k$ mit $k\geq1$ lässt sich ggf. durch folgende Überlegungen reduzieren.

1. Das Integrationsintervall $[0,p]$ kann durch $[x_0,x_0+p]\subset D$ mit beliebiger Stelle $x_0\in D$ ersetzt werden.
2. Ist $y=f(x)$ eine *gerade* Funktion, so gilt $b_k=0$ für alle $k\geq1$ und $$
  S_f(x)=\frac{a_0}{2}+\sum_{k=1}^\infty{a_k\cos{(k\cdot\omega\cdot x)}}
$$ Gilt hingegen $y=f(x)$ *ungerade*, so gelten $a_0=0$ und $a_k=0$ für alle $k\geq1$ und $$
  S_f(x)=\sum_{k=1}^\infty{b_k\sin{(k\cdot\omega\cdot x)}}
$$

Die zweite Aussage soll für den Fall einer geraden Funktion $f:x\mapsto y=f(x)$ mit $$
  f(x)=f(-x)\quad\forall\, x\in(-a,a)\,,\;a>0\quad(\text{bzw.}\; \forall\,x\in\mathbb{R})
$$ nachgerechnet werden. Die Fourierkoeffizienten $b_k$ berechnen sich in diesem Fall unter Benutzung der Substitution $x=-t$ mit $\mathrm{d}x=-\mathrm{d}t$ sowie $$
  \int_{-\frac{p}{2}}^\frac{p}{2}{\left(\sin{\left(k\cdot\omega\cdot x\right)}\cdot f(x)\right)}\,\mathrm{d}x=
  \int_{\frac{p}{2}}^{-\frac{p}{2}}{\left(\sin{\left(k\cdot\omega\cdot (-1)\cdot t\right)}\cdot f(-t)\right)}\cdot(-1)\,\mathrm{d}t=
  \int_{-\frac{p}{2}}^{\frac{p}{2}}{\left(\sin{\left(k\cdot\omega\cdot (-1)\cdot t\right)}\cdot f(-t)\right)}\,\mathrm{d}t
$$ Mit dem Wissen der Eigenschaft von $f$, eine gerade Funktion zu sein, sowie $\sin{x}=-\sin{(-x)}$ für alle $x$ folgt hieraus direkt $$
  b_k=\frac{2}{p}\cdot\int_{-\frac{p}{2}}^\frac{p}{2}{\left(\sin{\left(k\cdot\omega\cdot x\right)}\cdot f(x)\right)}\,\mathrm{d}x=
  -\frac{2}{p}\cdot\int_{-\frac{p}{2}}^\frac{p}{2}{\left(\sin{\left(k\cdot\omega\cdot x\right)}\cdot f(x)\right)}\,\mathrm{d}x=0
$$ für alle $k\geq1$.

Im nachstehenden Video ist noch einmal die Frage thematisiert, zu erkennen, ob die - stückweise stetige Grundfunktion $f$ gerade beziehungsweise ungerade ist. Der Aufwand zur Berechnung der Fourierkoeffizienten einer Fourierreihe lässt sich ggf. reduzieren.

!?[Gerade-ungerade Funktion](https://www.youtube.com/watch?v=7Uig_X9Lg3s&list=PLLTAHuUj-zHgvbOordkJ5jLmqcls2ZNrg&index=22)


Spektrale Darstellung einer Fourierreihe
========================================

...


Sicher gewußt
=============


Testen Sie Ihr Wissen zu den Themen dieses Abschnitts.

---

**Frage 1.** Setzen Sie die Funktion $f:[0,1]\to\mathbb{R}$ mit $f(x)=a\cdot(1-x)$ und $a\in\mathbb{R}\setminus{0}$ zu einer geraden Funktion $g$ auf dem Intervall $[-1,1]$ fort.

[( )] $$ g(x)=\left\{ \begin{array}{rcl} f(x) & \text{für} & x\in[0,1] \\ -a\cdot(1+x) & \text{für} & x\in[-1,0) \end{array} \right. $$
[( )] $$ g(x)=f(x)\quad\text{für alle}\quad x\in[-1,1] $$
[(X)] $$ g(x)=\left\{ \begin{array}{rcl} f(x) & \text{für} & x\in[0,1] \\ a\cdot(1+x) & \text{für} & x\in[-1,0) \end{array} \right. $$
[[?]] Stellen Sie den Graph der Funktion $f$ im kartesischen Koordinatensystem graphisch dar. Ergänzen Sie zu einem Graph einer Funktion $g$ über dem Intervall $[-1,1]$, welcher symmetrisch zur zweiten Achse des Koordinatensystems ist. Bestimmen Sie den Funktionsterm von $g$ über dem Teilintervall $[-1,0)$.
****************************************

Für eine gerade Funktion $g$ gilt $$
  g(x)=g(-x)\quad\forall\;x\in D
$$ worin $D\in\mathbb{R}$ beziehungsweise $D=(-d,d)$ mit $d>0$ ist. Wird $x>0$ vorausgesetzt, so gelten $-x<0$ sowie $$
  g(x)=a\cdot(1-x)=a\cdot(1+(-x))=g(-x)
$$ Die Funkion $g$ der ersten Antwortoption ist ungerade, da für $x>0$ analog gilt $$
  g(x)=a\cdot(1-x)=a\cdot(1+(-x))=-g(-x)
$$ Die Funktion $g$ der zweiten Antwortoption ist weder gerade noch ungerade.

****************************************

---

**Frage 2.** Entscheiden Sie, welche Periode $p>0$ die Funktion $$
  f:x\mapsto y=f(x)=\left|\cos{\left(2\cdot x+\frac{\pi}{8}\right)}\right|\,,\quad x\in\mathbb{R}
$$ besitzt.

[( )] $p=\pi$
[(X)] $p=\frac{\pi}{2}$
[( )] $p=2\cdot\pi$
[[?]] Eine reelle Funktion $f$ einer reellen Variablen $x\in\mathbb{R}$ heißt periodisch, falls es ein $p>0$ gibt, so dass für alle $x$ gilt $f(x+p)=f(x)$.
****************************************

Die Kosinusfunktion ist periodisch mit der Fundamentalperiode $p=2\cdot\pi$. Für die Hilfsfunktion $h:x\mapsto h(x)$, $x\in\mathbb{R}$, mit $$
  h(x)=\cos{\left(2\cdot x+\frac{\pi}{8}\right)}
$$ gilt für beliebige $k\in\mathbb{Z}$ $$
  h(x)=\cos{\left(2\cdot x+\frac{\pi}{8}\right)}=
  \cos{\left(2\cdot x+\frac{\pi}{8}+\textcolor{red}{2\cdot k\cdot\pi}\right)}=
  \cos{\left(2\cdot (x+k\cdot\pi)+\frac{\pi}{8}\right)}=h(x+k\cdot\pi)
$$ d. h. $h$ ist periodisch mit Fundamentalperiode $p=\pi$. Der Summand $\pi/8$ im Argument des Kosinus hat keinen Einfluss auf die Periode.

Des Weiteren berechnet sich unter Verwendung des Additionstheorems für den Kosinus $$
  h\left(x+\textcolor{red}{\frac{\pi}{2}}\right)=
  \cos{\left(2\cdot\left(x +\textcolor{red}{\frac{\pi}{2}}\right)+\frac{\pi}{8}\right)}=
  \cos{(2\cdot x+\pi)}\cdot\cos{\left(\frac{\pi}{8}\right)}-
  \sin{(2\cdot x+\pi)}\cdot\sin{\left(\frac{\pi}{8}\right)}=
  -\left(
    \cos{(2\cdot x)}\cdot\cos{\left(\frac{\pi}{8}\right)}-
    \sin{(2\cdot x)}\cdot\sin{\left(\frac{\pi}{8}\right)}
  \right)=
  -h(x)
$$ für alle $x\in\mathbb{R}$, woraus unmittelbar folgt $$
  f(x)=f\left(x+\frac{\pi}{2}\right)\quad\forall x\in\mathbb{R}
$$ Die Funktion $f$ besitzt die Fundamentalperiode $p=\frac{Pi}{2}$.

****************************************

---

**Frage 3.** Berechnen Sie zur periodischen Funktion $$
  f:x\mapsto y=f(x)=\left|\cos{\left(2\cdot x+\frac{\pi}{8}\right)}\right|\,,\quad x\in\mathbb{R}
$$ den Fourierkoeffizienten $a_0$.

[( )] $$ \frac{2}{\pi} $$
[( )] $$ 0 $$
[(X)] $$ \frac{4}{\pi} $$
[[?]] Der Fourierkoeffizient $a_0$ berechnet sich mit Hilfe des bestimmten Integrals $$
  a_0=\frac{2}{p}\cdot\int_{-\frac{p}{2}}^\frac{p}{2}{\left|\cos{\left(2\cdot x+\frac{\pi}{8}\right)}\right|}\,\mathrm{d}x
$$ worin - unter Nutzung der Lösung zu Frage 2 - für die Periode $p=\frac{\pi}{2}$ einzusetzen ist. Beachten Sie, dass vor Bildung einer Stammfunktion die Beträge im Integranden zu eliminieren sind.
****************************************

Zur Berechnung des bestimmten Integrals kann das Integrationsintervall $\left[0,\frac{\pi}{2}\right]$ durch das Intervall gleicher Länge $$
  \left[-\frac{\pi}{16},\frac{\pi}{2}-\frac{\pi}{16}\right]=
  \left[-\frac{1}{16}\cdot\pi,\frac{7}{16}\cdot\pi\right]
$$ ersetzt werden. (Verschiebung um den Wert $-\frac{\pi}{16}$.) Für die Grenzen / Mitte dieses Intervalls berechnen sich die Argumente des trigonometrischen Terms $$
  2\cdot x+\frac{\pi}{8}=\left\{
    \begin{array}{rcl}
      0 & \text{für} & x=-\frac{1}{16}\cdot\pi \\
      \frac{\pi}{2} & \text{für} & x=\frac{3}{16}\cdot\pi \\
      \pi & \text{für} & x=\frac{7}{16}\cdot\pi
    \end{array}
  \right.
$$ Somit ergibt sich $$
  \left\{
    \begin{array}{rcl}
      \cos{\left(2\cdot x+\frac{\pi}{8}\right)}\geq0 & \text{für} & x\in\left[-\frac{\pi}{16},\frac{3}{16}\cdot\pi\right] \\
      \cos{\left(2\cdot x+\frac{\pi}{8}\right)}<0 & \text{für} & x\in\left(\frac{3}{16}\cdot\pi,\frac{7}{16}\cdot\pi\right]
    \end{array}
  \right.
$$ Der Fourierkoeffizient berechnet sich damit $$
  a_0=\frac{4}{\pi}\cdot\left(
    \int_{-\frac{1}{16}\cdot\pi}^{\frac{3}{16}\cdot\pi}{\cos{\left(2\cdot x+\frac{\pi}{8}\right)}}\,\mathrm{d}x+
    \int_{ \frac{3}{16}\cdot\pi}^{\frac{7}{16}\cdot\pi}{\left[-\cos{\left(2\cdot x+\frac{\pi}{8}\right)}\right]}\,\mathrm{d}x
  \right)=
  \frac{2}{\pi}\cdot\left(
    \left[
      \sin{\left(2\cdot x+\frac{\pi}{8}\right)}
    \right]_{-\frac{1}{16}\cdot\pi}^{\frac{3}{16}\cdot\pi}+
    \left[
      -\sin{\left(2\cdot x+\frac{\pi}{8}\right)}
    \right]_{ \frac{3}{16}\cdot\pi}^{\frac{7}{16}\cdot\pi}
  \right)=\frac{4}{\pi}
$$

****************************************
