## Saisonpflege

Einmal je Prüfungsjahr, sobald die Aufgaben des Durchgangs auf dem
Bildungsserver stehen (Sommer). Ergebnis ist ein neuer Stand von msa.md
mit Datum und ein neuer Jahrgang im Katalog. Der Masterprompt wird dabei
nicht angefasst, es sei denn, Punkt 2 oder 3 hat sich geändert.

Quellen, in dieser Reihenfolge:
- Prüfungsaufgaben Mathematik Jahrgangsstufe 10 (Bildungsserver):
  https://bildungsserver.berlin-brandenburg.de/unterricht/pruefungen/pruefungen-10/pruefungsaufgaben-mathematik
- Fachbriefe Mathematik Brandenburg (Bildungsserver)
- Sek-I-Verordnung und Verwaltungsvorschriften (bravors.brandenburg.de),
  nur wenn ein Fachbrief eine Änderung ankündigt

Prüfen, je Punkt eine Zeile in msa.md:
1. Hefte: welche Niveaus, getrennt oder gemeinsam, Sternchenaufgaben
   ja/nein, Anzahl der Aufgaben, Gesamtpunkte, Seiten.
2. Hilfsmittel laut Arbeitshinweisen der ersten Seite, wortgleich.
3. Aufgabe 1: Punkte, Anzahl der Teilaufgaben, Antwortformate.
4. Formelblatt: Inhalt gegenüber Vorjahr.
5. Operatoren, die neu auftreten.
6. Aufgabentypen in Aufgabe 1 und im Kontextteil, die typen.csv nicht
   kennt. Neuer Typ → Zeile in typen.csv, bevor der Jahrgang eingelesen
   wird.

Danach: Jahrgang in katalog-basis.csv und katalog-kontext.csv aufnehmen
(Quellfeld = Dateiname des Hefts), Frequenzen neu zählen, Stand in
msa.md eintragen. Ändert sich Punkt 2 oder 3, Masterprompt 1.4 und die
Verfremdungsregel in blatt-konzept.md gegenlesen.

Stand 2026: EBR und FOR erstmals getrennte Hefte; kein Gymnasialheft
mehr; FOR-Heft 7 Aufgaben, 15 Seiten; Aufgabe 1 unverändert 10 Punkte,
a–j; Hilfsmittel unverändert (nicht programmierbarer, nicht
grafikfähiger Taschenrechner, Formelsammlung, Formelblatt,
Kurvenschablonen, Zeichengeräte, Wörterbuch).
