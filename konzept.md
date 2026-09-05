# KONZEPT – Arbeitsblätter aus alten Prüfungen
Stand 05.09.2026 · maßgebliche Grundlage; getroffene Entscheidungen werden ohne neuen Anlass nicht wieder aufgerollt

## 1 Ziel

Ein Nachhilfeschüler wird über Wochen gezielt auf die schriftliche Prüfung P10 Mathematik (Brandenburg, FOR-Niveau = MSA) vorbereitet. Grundlage sind die alten Prüfungen: Sie zeigen, welche Aufgabentypen vorkommen, in welcher Sprache und auf welcher Höhe. Aus ihnen entstehen immer wieder neue, druckfertige Arbeitsblätter zu einzelnen Typen oder Themen. Am Ende kann der Schüler eine vollständige Originalprüfung lösen.

Erfolgskriterium eines Blatts: Der Schüler löst danach Aufgaben dieses Typs auf Prüfungshöhe selbständig, und der Lehrer sieht am Blatt, an welcher Stufe er hängt.

## 2 Bausteine

    katalog-prompt.md          Kern: Methode der Erfassung, prüfungsunabhängig
    profile/p10-bb.md          Profil: alles, was an der P10 hängt (Quellen, Aufbau, Kürzel, Themenliste, Beispielzeilen)
    blatt-prompt.md            Blatt-Prompt (noch zu schreiben)
    konzept.md                 diese Datei
    p10-bb/pruefungen.md       Heftliste mit Erfassungsstatus
    p10-bb/vorgaben.md         amtliche Vorgaben aus den Fachbriefen, Jahrescheck; gesonderter Baustein
    p10-bb/typen.csv           Typvokabular, wächst beim Erfassen
    p10-bb/katalog-basis.csv   Zeilen der Basisaufgaben
    p10-bb/katalog-kontext.csv Zeilen der Kontextaufgaben
    p10-bb/typenbibliothek.md  abgeleitet aus dem Katalog, wird erzeugt, nie editiert (noch nicht vorhanden)
    p10-bb/pdf/                Archiv der Hefte (noch nicht angelegt)

Ablage: eigenes Repo hz-0801/pruefungskatalog (öffentlich, damit curl ohne Anmeldung liest; die Basis-URL steht im Profil und ist die einzige Stelle, die bei anderer Ablage geändert wird). Claude liest per curl, der Lehrer lädt geänderte Dateien hoch. Geschrieben wird nur beim Aufbau und einmal im Jahr.

## 3 Entscheidungen

1. Die Einheit ist der Aufgabentyp, nicht die Aufgabe. Ein Typ ist eine Fertigkeit, die man als Einheit übt. Das Original ist Muster und Messlatte.
2. Auf dem Blatt gibt es drei Sorten Aufgaben: hinführende (leichter, eigene Struktur), die Originalfassung (Struktur und Wortlaut des Originals, neue Werte, leicht umformuliert) und weitere Varianten desselben Typs (gleiche Struktur, anderer Kontext). Struktur ändern nie – dann ist es ein anderer Typ. Auffüllende Aufgaben nach didaktischem Bedarf.
3. Decke ist das Original. Über das Prüfungsniveau geht kein Blatt hinaus.
4. Progression je Typ: hinführen, Anker, halten – nach dem Muster der Progressionsregeln aus dem Masterprompt (jede Hauptnummer beginnt leicht, endet auf Prüfungshöhe).
5. Keine Quellenangabe auf dem Schülerblatt; Herkunft (Jahr, Aufgabe) nur im Begleitteil.
6. Lösungen vorerst nur Ergebnisse. Punkte stehen im Katalog, ein späterer Umstieg auf Erwartungshorizont-Stil braucht keine neue Analyse.
7. Kein Log je Schüler. Wiederholung steuert der Lehrer; jedes Blatt hat neue Werte, eine ungeplante Wiederholung schadet nicht.
8. Keine Reserveprüfung. Für den Abschlusstest nimmt der Lehrer die Prüfung, die er am wenigsten verwendet hat.
9. Häufigkeit ist Auskunft, keine Priorität und kein Filter. Ein einziges Vorkommen ist ein vollwertiger Typ. Der Rahmenlehrplan setzt den Rahmen dessen, was kommen kann; er ist Hintergrund, keine Quelle für Typen.
10. Katalog vor Blatt: Alle Hefte werden einmal vollständig erfasst; Blätter entstehen nur aus dem Katalog. Die Hefte selbst holt der Blatt-Prompt nur für Wortlaut oder Bild einer Ankeraufgabe.
11. Der Katalog erfasst Fakten, nicht Nutzung: Zeile = kleinste Einheit mit eigener Punktangabe; Fakten getrennt von Deutung; Nachbau-Test als Erfolgskriterium; kein Volltext, sondern Verweis plus Strukturbeschreibung. Spätere Wünsche sind Umsortieren, im Ausnahmefall ein Nachtragslauf für ein Feld, nie ein Neustart.
12. Kern und Profil getrennt. Erstes und derzeit einziges Profil: P10-BB. Weitere Profile (Abitur, andere Länder) erst bei Bedarf; Vokabular und Häufigkeit gelten nie über Profile hinweg.
13. Vokabular in drei Ebenen: Leitidee und Thema fest im Profil (aus Rahmenlehrplan, Fachbrief-Inhaltsliste, Lehrwerkgliederung), Typ wächst aus den Heften in typen.csv, Abgleichlauf nach dem letzten Heft. Der Lehrer sieht die fertige Typenliste einmal durch; das ist optional.
14. Zwei Katalogdateien, Basis und Kontext, gleiches Schema; eine Typenliste.
15. Dateiform CSV mit Semikolon; Durchsicht über eine Prüftabelle im Chat, nicht in der Datei.
16. Ergebnisse sind eigene Rechnung, per Skript geprüft; Unsicheres trägt „?". Amtliche Lösungen gibt es nur für die Musteraufgaben 2028.
17. Skizzen werden nicht übernommen, sondern aus dem Feld skizze mit der Vorlage neu gezeichnet; das Original-PDF ist Referenz. Foto und technische Zeichnung: Nachbau mit zeichenbarer Figur, Originalausschnitt nur als Notlösung.
18. Bestand: Oberschulhefte 2014–2026 und Musteraufgaben 2028. Gymnasialhefte nicht (seit 2025/26 keine P10 am Gymnasium).
19. Amtliche Vorgaben (Fachbriefe, Rundschreiben) werden gesondert in vorgaben.md geführt, mit einem jährlichen Check als eigenem Schritt. Der Katalog-Prompt liest sie nicht.
20. Die PDF-Pipeline aus dem Masterprompt (mathblatt.sty, xelatex, Skriptprüfung, Ausgabeblock) bleibt für die Blätter.
21. Versteckte Leistungen in einer Einheit bleiben eine Zeile; alle Leistungen werden in gesucht, ergebnis, format, typ und typ_neben erfasst; Punkte werden nicht geschätzt aufgeteilt.
22. Arbeitsweise Schritt für Schritt: Claude liefert Dateien mit Pfad und Namen, der Lehrer legt sie ab und meldet sich; dann nennt Claude den nächsten Schritt. Aufwendige Aktionen werden vorher angekündigt.

## 4 Verworfen

- Häufigkeitsschwelle und „Kerntypen": schließt aus, was die Prüfung trotzdem bringen kann.
- Reserveprüfung: Wiedererkennung bei neuen Werten klein, Bestand endlich.
- Log je Schüler: Schreibaufwand bei jeder Sitzung, Nutzen gering.
- Live-Analyse der Hefte je Blatt: langsam, teuer, jedes Mal anders kategorisiert.
- Virtuelle Unterzeilen mit geschätzten Punkten: Deutung im Faktenfeld.
- Volltext im Katalog: Kopie aller Hefte, sprengt Kontext und Projekt.
- Markdown-Tabelle als Katalog: bei 37 Feldern nicht lesbar.
- Ein Prompt für alle Prüfungen ohne Profil: verliert die konkreten Regeln, die Zeilen gut machen.
- Google Drive als Ablage: möglich, aber Dateien laufen bei jeder Sitzung durch den Kontext; Aktualisieren über den Konnektor ungetestet. Bleibt Alternative, falls das Hochladen zu lästig wird.

## 5 Offen

- Ablageort bestätigen (Basis-URL im Profil).
- Prüfungsjahr des Schülers: Annahme 2027 (aktuelles Format). Bei 2028 rücken hilfsmittelfreier Teil und Musteraufgaben nach vorn.
- Themenliste des Profils im Probelauf prüfen.
- Blatt-Prompt: noch nicht begonnen; Entwurf nach dem Probelauf, damit er gegen echte Katalogzeilen geschrieben wird.
- PDF-Archiv anlegen.

## 6 Ablauf

1. Entwurf: abgeschlossen (Kern, Profil, Dateien, Vorgaben).
2. Probelauf: Hefte 2025, 2026 FOR, 2024 erfassen, je eines pro Antwort, Prüftabelle je Heft.
3. Typenliste nach drei Heften festziehen; Blatt-Prompt v0.1; zwei, drei Testblätter aus dem Katalog. Fehlt ein Feld, wird es jetzt ergänzt.
4. Restliche Hefte und Musteraufgaben 2028 erfassen; Abgleichlauf; Typenbibliothek ableiten.
5. Blatt-Prompt fertigstellen.
Jährlich: Vorgabencheck (vorgaben.md), neues Heft erfassen, Typenbibliothek neu ableiten.

## 7 Änderungen

- 2026-09-05: angelegt.
