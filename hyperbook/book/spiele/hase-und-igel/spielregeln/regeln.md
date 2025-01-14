Ziel dieser Dokumentation ist es, die Spielregeln der Softwarechallenge
festzuhalten.

[PDF-Version dieses Dokumentes](regeln.pdf)

Wir freuen uns über sämtliche Verbesserungsvorschläge. Die Dokumentation
kann [direkt auf GitHub
editiert](https://github.com/software-challenge/docs) werden, einzige
Voraussetzung ist eine kostenlose Registrierung bei GitHub. Ist man
angemeldet, kann man ein Dokument auswählen (ein guter Startpunkt ist
die Datei
[index.md](https://github.com/software-challenge/docs/blob/master/index.md)
welche Verweise auf alle Sektionen der Dokumentation enthält) und dann
auf den Stift oben rechts klicken. Alternativ auch gern eine E-Mail an
<svk@informatik.uni-kiel.de>.

# Spielbeginn

Jeder Spieler erhält zu Beginn 68 Karotten und 5 Salate als Wegzehrung,
sowie je eine Karte „Rücke eine Position vor“, „Falle eine Position
zurück“, „Friss sofort einen Salat“ und „Karotten nehmen oder abgeben“.
Mit den Karotten bezahlt der Spieler das Vorrücken. Die Anzahl der
Karotten, die benötigt werden, um eine bestimmte Anzahl von Zügen zu
ziehen, ist dabei der folgenden Rennkarte zu entnehmen.

![hui bilder 003](../images/hui-bilder-003.png)

Das Spielfeld besteht aus 65 Feldern. Ziel des Spiels ist es das
Zielfeld (Feld 65) mit weniger als zehn Karotten und keinem Salat zu
erreichen.

# Felder

Es gibt acht verschiedene Spielfelder:

## Startfeld

Das Startfeld darf nur verlassen werden. Es ist nicht erlaubt das
Startfeld erneut zu betreten, sollte es einmal verlassen werden. Auf ihm
starten beide Spieler

## Karottenfeld

Ein Karottenfeld darf durch jede Bewegungsaktion (Vorwärtszug, Karten)
betreten werden. Nur auf ihm darf ein Karotten tauschen Zug stattfinden
(die Karotten tauschen Karte darf hier nicht benutzt werden).

## Hasenfeld

Darf nur betreten werden, wenn eine Karte gespielt werden kann. Sollte
sich ein Spieler am Ende seines Zuges auf einem Hasenfeld befinden, muss
dieses im nächsten Zug (wenn möglich) verlassen werden (es ist erlaubt
das Hasenfeld zu verlassen und dann durch nutzen von Karten wieder zu
betreten).

## Salatfeld

Darf nur betreten werden, wenn der Spieler mindestens einen Salat
besitzt. In dem Zug nach dem Betreten muss ein Salat gefressen werden.
Nur auf einem Salatfeld darf ein Salat gefressen werden (außer natürlich
durch die Karte Salat fressen). Das Salatfeld muss verlassen werden
(wenn möglich) sobald ein Salat gegessen wurde (es ist innerhalb des
Spiels trotzdem durch Rückzüge oder Karten möglich auf demselben
Salatfeld mehrere Salate zu essen).

## Igelfeld

Darf nur durch einen Rückzug betreten werden. Muss (wenn möglich) im
nächsten Zug wieder verlassen werden.

## Position-1 Feld

Das Position 1 Feld darf uneingeschränkt betreten werden. Sollte sich
ein Spieler am Anfang seines Zuges auf diesem Feld befinden und an
erster Stelle stehen, so erhält er zehn Karotten.

## Position-2 Feld

Das Position 2 Feld darf uneingeschränkt betreten werden. Sollte sich
ein Spieler am Anfang seines Zuges auf diesem Feld befinden und an
zweiter Stelle stehen, so erhält er 30 Karotten.

## Zielfeld

Das Zielfeld darf nur betreten werden, wenn der Spieler höchstens zehn
Karotten und keine Salate besitzt.

# Zugmöglichkeiten

Ein Spieler kann folgende Züge machen:

## Vorwärtszug

Durch einen Vorwärtszug bewegt sich der Spieler um die entsprechende
Zahl von Feldern nach vorne (mindestens 1). Dabei werden Karotten
entsprechend der Rennkarte verbraucht. Wenn ein Spieler sich auf dem
Startfeld befindet, muss ein Vorwärtszug gemacht werden. Wenn ein
Spieler sich auf einem Startfeld befindet oder die letzte Aktion, die
keine Aussetzaktion war, Salat fressen war, muss ein Bewegungszug
gemacht werden (Vorwärtszug oder Rückwärtszug). Ein Spieler darf nicht
auf ein Feld ziehen, dass bereits durch den Gegner besetzt ist, außer es
handelt sich um das Zielfeld. Durch einen Vorwärtszug dürfen alle Felder
außer das Igelfeld direkt betreten werden. Es ist nicht erlaubt das
Zielfeld zu betreten, wenn die Siegbedingungen (höchstens 10 Karotten
und 0 Salate) nicht erfüllt sind. Wenn durch einen Vorwärtszug ein
Salatfeld betreten wird, muss im nächsten Zug ein Salat gefressen werden
(sollte kein Salat vorhanden sein ist das Betreten nicht erlaubt). Wenn
durch einen Vorwärtszug ein Hasenfeld betreten wird, muss danach eine
Karte ausgespielt werden (wenn keine spielbare Karte vorhanden ist das
Betreten nicht erlaubt). Sollte durch einen Vorwärtszug kein Hasenfeld
betreten werden endet der Zug.

## Rückwärtszug

Durch einen Rückwärtszug zieht der Spieler zu dem nächsten Igelfeld mit
kleinerem Index, sollte dies nicht besetzt sein. Ist das vorherige
Igelfeld besetzt, darf kein Rückzug gemacht werden. Durch einen Rückzug
werden 10 mal zurückgezogene Felder viele Karotten aufgenommen. Nach
einem Rückwärtszug endet der Zug.

## Karte ausspielen

Eine Karte muss ausgespielt werden, wenn ein Hasenfeld neu betreten wird
und darf auch nur auf einem Hasenfeld ausgespielt werden. Das Betreten
eines Hasenfeldes ist entweder durch einen Vorwärtszug oder das
Ausspielen einer Karte möglich. Sollte es nicht möglich sein eine Karte
aus zuspielen ist das Betreten eines Hasenfeldes nicht erlaubt. Sollte
durch das Ausspielen einer Karte kein Hasenfeld neu betreten werden Ende
der Zug. Ein Spieler hat zu Beginn folgende Karten:

### Friss sofort einen Salat

Es wird ein Salat vom Spieler entfernt, je nach Position des Spielers
(Erster/Zweiter) erhält der Spieler Karotten (10/30). Diese Karte darf
nur eingesetzt werden, wenn der Spieler mindestens einen Salat hat. In
dem nächsten Zug muss das betretene Hasenfeld verlassen werden.

### Karotten nehmen oder abgeben

Der Spieler darf 20 Karotten abgeben oder aufnehmen oder nichts tun. Es
darf der Spieler nicht mehr Karotten abgeben als er besitzt. In dem
nächsten Zug muss das betretene Hasenfeld verlassen werden.

### Rücke eine Position vor

Kann nur ausgespielt werden, wenn der Spieler sich an zweiter Position
befindet. Der Spieler rückt auf das Feld vor dem gegnerischen Spieler
vor. Dies ist nicht erlaubt, sollte es sich bei dem so betretenen Feld
um ein Igelfeld handeln oder sollte der gegnerische Spieler sich im Ziel
befinden. Es ist außerdem nicht erlaubt, so ein Salatfeld zu betreten,
ohne mindestens einen Salat zu besitzen. Es kann so das Ziel erreicht
werden, wenn die Siegbedingungen erfüllt sind.

### Falle eine Position zurück

Kann nur ausgespielt werden, wenn der Spieler sich an erster Position
befindet. Der Spieler fällt auf das Feld hinter dem gegnerischen Spieler
zurück. Dies ist nicht erlaubt, sollte es sich bei dem so betretenen
Feld um ein Igelfeld handeln oder sollte der gegnerische Spieler sich
auf dem Startfeld befinden. Es ist außerdem nicht erlaubt, so ein
Salatfeld zu betreten, ohne mindestens einen Salat zu besitzen.

## Karotten tauschen

Kann nur ausgeführt werden, wenn sich der Spieler auf einem Karottenfeld
befindet. Es können entweder zehn Karotten abgegeben werden (dabei muss
der Spieler mindestens zehn Karotten besitzen) oder 10 Karotten
aufgenommen werden. Nach dieser Aktion endet der Zug.

## Salat fressen

Wenn sich der Spieler auf einem Salatfeld befindet und er in seiner
letzten Aktion, die kein Aussetzzug war, keinen Salat gefressen hat,
muss er einen Salat fressen. Der Spieler verliert einen Salat (dies ist
immer möglich, da ein Spieler nur mit mindestens einem Salat ein
Salatfeld betreten kann) und erhält je nach Position (Erster/Zweiter)
Karotten (10/30). Nach dieser Aktion endet der Zug.

## Aussetzen

Es Spieler darf nur Aussetzen, sollte sonst kein anderer Zug möglich
sein. Nach dieser Aktion endet der Zug.

## Zusammenfassung

Enthält ein Zug einen der folgenden Aktionen, kann er nur aus einer
Aktion bestehen: Rückwärtszug, Karotten tauschen, Salat fressen oder
Aussetzen. Eine Karte kann nur nach einem Vorwärtszug oder einer anderen
Karte gespielt werden (wenn durch die vorherige Aktion ein Hasenfeld
betreten wird). Ein Vorwärtszug, der auf kein Hasenfeld führt, kann
ebenfalls nur die einzige Aktion eines Zuges sein. Die einzige
Möglichkeit mehr als eine Aktion pro Zug zu machen ist durch Karten
möglich. Dies kann folgendermaßen passieren:  
Der Gegner befindet sich zwischen zwei Hasenfeldern. Der Spieler selbst
befindet sich hinter ihm. Der Spieler zieht mit einem Vorwärtszug auf
das Hasenfeld hinter dem Gegner. Daraufhin muss er eine Karte spielen.
Er spielt die Karte "Rücke eine Position vor". Dadurch steht er auf dem
Hasenfeld direkt vor dem Gegner und muss erneut eine Karte spielen. Er
spielt die Karte "Falle eine Position zurück". Dadurch steht er auf dem
Hasenfeld direkt hinter dem Gegner und muss erneut eine Karte spielen.
Er spielt "Friss sofort einen Salat". Es wird kein Hasenfeld neu
betreten, also endet der Zug. So ist es möglich maximal vier Aktionen in
einem Zug zu machen.

# Spielende

Das Spiel endet, sobald das Rundenlimit von 30 Runden erreicht ist oder
sich mindestens eine Spieler am Ende einer Runde im Ziel befindet.
Sollte der erste Spieler im Ziel sein, hat der zweite Spieler einen
Nachzug. Der erste Spieler bekommt keinen Nachzug. Es gewinnt der
Spieler, der am nächsten am Ziel befindet. Sollte beide Spieler sich im
Ziel befinden, gewinnt der Spieler mit weniger Karotten. Sollten beide
Spieler gleich viele Karotten besitzen, gewinnt der Startspieler, da er
zuerst das Ziel erreicht hat.

# Beispiel

Jasper steht unmittelbar vor einem Hasenfeld (Feld 34). Johannes steht
weit hinter Jasper (Feld 22) und hat nur noch den Hasenjoker „Rücke eine
Position vor“. Dann darf Johannes weder auf ein Hasenfeld vor Jasper
setzen (z. B. Feld 35), denn dort darf er seinen einzigen Hasenjoker
nicht einsetzen, noch darf er auf ein Hasenfeld hinter Jasper setzen
(z. B. Feld 25), denn wenn er dort seinen Hasenjoker „Rücke eine
Position vor“ einsetzen würde, käme er wieder auf ein Hasenfeld, was
aber nicht erlaubt ist, weil er dafür dann keinen Hasenjoker mehr hat.

![hui bilder 004](../images/hui-bilder-004.png)
