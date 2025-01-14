---
name: Idee implementieren
index: 8
---

# Eine Idee implementieren

Man hat einige Spiele absolviert und sich eine gute Strategie
ausgedacht. Damit hat man zwar schon einen wichtigen Teil der Arbeit
geleistet, aber irgendwie muss dem
[Computerspieler](software/client) noch beigebracht werden, nach
dieser Strategie zu spielen.

Anhand einer kleinen Aufgabe soll gezeigt werden, wie man eine Idee
formal beschreiben und in ein Programm überführen kann. Dabei nehmen wir
an, dass wir einen Stapel mit Karten haben, der sortiert werden soll.

## Vorraussetzungen

-   eine beliebige Anzahl an Spielkarten

-   eine Reihenfolge, in der die Spielkarten sortiert werden sollen

### Idee formalisieren

Als erstes muss die Idee formal beschrieben werden. Oftmals kann man
zunächst beschreiben, wie man als Mensch vorgehen würde.

1.  Gehe den Stapel durch und merke die Position, an der sich die
    kleinste Karte befindet.

2.  Tausche die Position der kleinsten Karte mit der untersten Karte im
    Stapel.

3.  Die kleinste Karte ist jetzt an der richtigen Position.

4.  Führe die Schritte nochmal für den Reststapel (ohne die sortierten
    Karten) aus.

### Idee implementieren

Nachdem man seine Idee formal niedergeschrieben hat, kann sie ganz
leicht in ein Programm überführt werden:

    /**
      * Das Array a[] symbolisiert den Stapel der unsortierten Karten. Dabei steht
      * eine Zahl immer für eine spezielle Karte. Eine kleinere Zahl bedeutet,
      * dass es sich um eine kleinere Karte handelt.
      *
      * start gibt die Position an, wo der Reststapel beginnt (am Anfang: start = 0)
      */
     public static void sortiere(int[] a, int start) {
         //Position der kleinsten Karte
         int pos = start;

         // Gehe Array durch und merke die Position der kleinsten Karte 
         for (int i = start+1; i < a.length; i++) {
             // Wenn eine kleinere Karte gefunden wurde...
             if (a[i] < a[pos]) {

                 ... neue Position merken
                 pos = i;
             }
         }

         // kleinste Karte mit erster Karte des Reststapels tauschen  
         int temp = a[start]; // erste Karte merken
         a[start] = a[pos];   // kleinste Karte nach vorne bringen
         a[pos] = temp;       // gemerkte Karte in die Mitte des Stapels schreiben

         // Wenn es noch einen Reststapel gibt, soll dieser weitersortiert werden 
         if (start < a.length) {
              sortiere(a, start+1);
         }
     }

-   Gehe den Stapel durch und merke die Position, an der sich die
    kleinste Karte befindet.

-   Tausche die Position der kleinsten Karte mit der untersten Karte im
    Stapel.

-   Die kleinste Karte ist jetzt an der richtigen Position.

-   Führe die Schritte nochmal für den Reststapel (ohne die sortierten
    Karten) aus.
