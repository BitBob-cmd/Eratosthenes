# Eratosthenes
ZbW ProgAdv Übung 1

Zentrum für berufliche Weiterbildung
Seite 1 von 2 Thomas Kehl
Programmentwicklung Advanced
Übungen Einführung I
Aufgaben
Das Primzahlsieb des Eratosthenes
Der griechische Mathematiker Eratosthenes (ca. 275 -
194 v.Chr.) beschrieb ein Verfahren, mit dem man in
der Reihe der natürlichen Zahlen alle Primzahlen
«aussieben» kann. Da Primzahlen nur durch 1 und
sich selbst teilbar sind, sind sie auch kein Vielfaches
von anderen Zahlen. Zahlen, die nicht prim sind, sind
Vielfache einer oder mehrerer anderer (und
kleinerer) Zahlen. Eratosthenes Verfahren beruht auf
dieser Vorüberlegung. Zur Ausführung streiche man
in einer zusammenhängenden Liste von natürlichen
Zahlen, die bei der 2 beginnt, alle «echten»
Vielfachen der ersten Zahl, also von 2, d.h.: 4, 6, 8,
10, ... Sodann streiche man alle echten Vielfachen der
3 (6, 9, 12, 15, ...). Man fahre mit der nächsten noch stehenden Zahl (es ist die 5, da die 4 als
Vielfaches von 2 bereits gestrichen wurde) analog fort und wiederhole den Vorgang, bis in der
Liste keine Zahl mehr ein Vielfaches einer anderen ist. Dann sind die Primzahlen übriggeblieben.
1. Aufgabe Entwickeln Sie ein Sieb des Eratosthenes in C# folgendermassen:
• Die Grösse des Siebes soll auf der Kommandozeile übergeben werden können.
Hinweis. Int32.Parse für die Umwandlung von String nach Int
• Die eigentliche Auswertung des Siebes soll in einer Methode Eratosthenes durchführt
werden, die das vollständige Sieb (als Array) zurück liefert:
PrimeType[] Eratosthenes(int size)
• Der Typ des Arrays sei eine Enumeration PrimeType mit den Werten Prim und
NotPrim
• Am Schluss soll der Array Zeilenweise à 10 Zahlen im Kommando-Fenster ausgegeben
werden.
Zentrum für berufliche Weiterbildung
Seite 2 von 2 Thomas Kehl
Hinweis:
Wenn die Liste bis zu einer Zahl n geht und man von der kleinsten Zahl ab nach dem o.g.
Verfahren vorgeht, so können alle noch verbliebenen Zahlen nur noch Vielfache in der Liste
haben, die grösser oder gleich ihres Quadrates sind, denn alle möglichen kleineren Teiler sind ja
bereits gestrichen. Es genügt also, das Verfahren nur für diejenigen Zahlen m durchzuführen,
für die m2 ≤ n gilt.
2. Aufgabe Es soll ein Array fixer Länge zurückgeliefert werden, das nur die Primzahlen enthält. Es soll
folgendes gelten: 02, 13, 25, 37, 411 usw.
3. Aufgabe Es soll ein Array variabler Länge (List<int> in System.Collections.Generics)
zurückgeliefert werden, das nur die Primzahlen enthält. Es soll folgendes gelten: 02, 13,
25, 37, 411 usw.
4. Aufgabe Es soll ein assoziatives Array (Dictionary<int,int> in
System.Collections.Generics) zurückgeliefert werden, das nur die Primzahlen
enthält. Es soll folgendes gelten: 02, 13, 25, 37, 411 usw.
