---
name: Hive
hide: true
---

# Spielregeln Hive: Software-Challenge 2020

## Anfangsaufstellung

Das Spielfeld ist ein Hexagon bestehend aus Hexagonen. Das Spielfeld hat
die Kantenlänge *n=6,* der Durchmesser beträgt 11. Es wird das kubische
Koordinatensystem genutzt
(<https://www.redblobgames.com/grids/hexagons/>).

Zu Anfang ist das Spielfeld leer bis auf 3 Felder, die von Brombeeren
blockiert sind.

![image](./images/1200px-MagicHexagon-Order3-a-6500c7c7-bad3-454d-bcb9-926e20bba906.svg3.png)

![image](./images/img-2019-09-16-110132-9c11473c-d9f2-4163-be28-f1dab692d018.png)

Ein Spieler spielt die roten Insekten, ein anderer die blauen. Beide
Spieler bekommen jeweils 11 Spielsteine folgender Typen:

-   1 Bienenkönigin

-   2 Spinnen

-   2 Käfer

-   3 Grashüpfer

-   3 Ameisen

## Ziel des Spieles

Das Ziel des Spieles ist, die gegnerische Bienenkönigin von allen 6
Seiten durch Spielsteine (also Insekten), blockierte Felder oder den
Rand einzuschließen. Ob die Spielsteine rot oder blau sind, spielt dabei
keine Rolle. Man könnte sich also auch selbst einschließen, was aber
natürlich nicht sinnvoll ist, weil damit dem Gegner zum Sieg verholfen
wird.

## Züge

Es wird abwechselnd gezogen, wobei Rot beginnt. In jeder Runde darf der
Spieler, der gerade am Zug ist, entweder einen Spielstein bewegen, der
sich bereits auf dem Spielfeld befindet, oder einen Spielstein aus
seinem Vorrat legen. Zu Beginn des Spiels darf jeder Spieler in seinem
Zug nur jeweils einen Spielstein legen. Erst nachdem der Spieler seine
Königin gelegt hat, darf dieser Spieler in den folgenden Zügen jeweils
frei wählen, ob er entweder einen Spielstein bewegen will, der sich
bereits auf dem Spielfeld befindet, oder einen zusätzlichen Spielstein
legen will.

### Der Schwarm

Die aneinander grenzenden Spielsteine sind der namensgebende Schwarm von
Hive. Während eines Spiels darf es immer nur einen Schwarm auf dem
Spielfeld geben. Es dürfen also keine Spielsteine vom Schwarm getrennt
werden.

### Blockierte Felder (Brombeeren)

![image](./images/black-berry-dark-65d040fc-200a-4202-90d9-a9b71b208265.png)

Auf die blockierten Felder darf kein Stein gelegt oder bewegt werden.
Für eine Königin wird ein benachbartes blockiertes Feld wie ein von
einem Stein belegtes Feld gewertet. Befindet sich also eine Königin
neben einem blockierten Feld, kann sie einfacher eingeschlossen werden.

### Der Rand des Spielfeldes

Natürlich dürfen Spielsteine nur auf das Spielfeld gelegt werden und
auch während des Ziehens dürfen die Spielsteine nicht das Spielfeld
verlassen. Für eine Königin werden Felder außerhalb des Spielfeldes wie
belegte Felder gewertet. Befindet sich also eine Königin am Rand, kann
sie einfacher eingeschlossen werden.

### Einen neuen Spielstein legen

Ein Spielstein darf nur auf ein freies Feld gelegt werden. Dieses freie
Feld muss mit mindestens einem Feld benachbart sein, auf dem ein
Spielstein der eigenen Farbe liegt. Es darf zu keinem Feld benachbart
sein, auf dem ein gegnerischer Spielstein zu oberst liegt. Einzige
Ausnahme bildet das Legen des ersten Spielsteines einer Farbe: Der erste
rote Spielstein darf auf ein beliebiges freies Feld gesetzt werden, der
erste blaue Spielstein muss direkt daran angelegt werden. Innerhalb der
ersten vier Runden müssen beide Spieler ihre Königin setzen.

### Einen Spielstein auf dem Spielfeld bewegen

#### Voraussetzungen für das Bewegen eines Spielsteins

Insekten eines Spielers dürfen erst bewegt werden, nachdem der Spieler
seine Königin gesetzt hat.

Insekten dürfen nur bewegt werden, wenn dadurch der Schwarm nicht
unterbrochen wird! Alle Steine müssen also immer (auch während eines
Zuges) miteinander verbunden sein. Während ein Stein bewegt wird, zählt
dieser nicht als Verbindung des Schwarms. Der Schwarm muss also auch
verbunden sein, wenn man den Stein in Bewegung entfernt.

Ein Spielstein kann nur auf das nächste Feld gezogen werden, wenn dafür
keine Steine beiseite geschoben werden müssen. Sind also die Felder
rechts und oben links von unserem Stein (z.B. der Biene auf (-1,1) in
dem Bild unten) belegt, so dürften wir nicht auf das Feld oben rechts
(0,1) von unserem Stein ziehen. (Ausnahmen: Grashüpfer, Käfer). Steine
dürfen trotzdem auf eingeschlossene Felder gelegt werden.

![image](./images/move.png)

In der vorstehenden Grafik sind alle für die rote Biene zulässigen
Felder gelb markiert.

Abgesehen vom Grashüpfer müssen sich die Steine immer am Rand des
Schwarms entlang bewegen. Der Käfer im unteren Bild darf sich also nicht
nach unten rechts bewegen. Zusätzlich dürfen sich Käfer über andere
Steine bewegen.

![image](./images/connected.png)

In der vorstehenden Grafik sind alle für den roten Käfer zulässigen
Felder gelb markiert.

Kann ein Spieler nicht ziehen, so muss er die Runde aussetzen!

#### Bienenkönigin

Die Königin darf - ähnlich dem König beim Schach - pro Zug nur ein Feld
weit bewegt werden.

![image](./images/bee.png)

#### Käfer

Der Käfer darf pro Zug auch nur ein Feld weit laufen. Allerdings ist der
Käfer das einzige Insekt, das auf andere Insekten draufziehen darf. Das
Insekt, auf dem der Käfer steht, ist blockiert und kann nicht verschoben
werden. Für das Legen neuer Steine zählt immer die Farbe des obersten
Steins. Käfer können also auf einen gegnerischen Stein klettern, was dem
Spieler ermöglicht, eigene Steine auf benachbarte, freie Felder zu
legen. Käfer können auch auf Käfer klettern, die auf anderen Steinen
stehen, es gibt keine Höhenbegrenzung.

![image](./images/beetle.png)

#### Grashüpfer

Der Grashüpfer springt von seinem Feld über eine gerade Reihe
miteinander verbundener Steine zum nächsten unbesetzten Feld. Er muss
immer über mindestens einen Stein springen.

![image](./images/grasshopper.png)

#### Spinne

Die Spinne bewegt sich immer genau 3 Felder weit. Während des Zuges darf
sie allerdings nicht zweimal auf dasselbe Feld ziehen und sie muss in
Verbindung mit dem Schwarm bleiben.

![image](./images/spider.png)

#### Ameise

Die Ameise darf beliebig viele Felder am Rand des Schwarms entlang
gezogen werden. Sie darf sich jedoch nicht über Lücken oder blockierte
Felder hinweg bewegen.

![image](./images/ant.png)

### Spielende

Wird die Bienenkönigin eines Spielers von allen Seiten von Insekten,
blockierten Feldern oder dem Rand eingeschlossen, so gewinnt der andere
Spieler. Allerdings darf Blau noch einen letzten Zug machen, nachdem die
blaue Bienenkönigin umstellt wurde.

Wird die 31. Runde erreicht, so gewinnt derjenige Spieler, dessen
Bienenkönigin die meisten freien angrenzende Felder hat, wobei
blockierte Felder oder Felder außerhalb des Spielfeldes nicht als freie
Felder zähen.

Sofern der Fall eintritt, dass beide Königinnen mit demselben Zug
eingeschlossen werden oder die 31. Runde erreicht wird und die Anzahl
der freien Nachbarfelder für beide Bienenköniginnen gleich ist, endet
das Spiel unentschieden.
