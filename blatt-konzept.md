# Blatt-Konzept – Nachhilfehefte aus dem Prüfungskatalog

Stand 2026-09-05, v0.1. Ergänzt `konzept.md` (Katalog). Für die Heft-Phase gilt bei Widerspruch diese Datei. Baumaschine ist der Masterprompt (v3.27+, Abschnitte 2.2 a–c, 3–6); diese Datei regelt nur, was sich durch den Katalog als Quelle ändert.

## 1 Ziel

Schüler werden themenweise an die P10-Prüfung (MSA) herangeführt, mit alten Prüfungsaufgaben als Maßstab. Nicht durch Vorlage ganzer Prüfungen (das erst am Ende), sondern durch Hefte, die ein Thema von leicht bis Originalniveau aufbauen. Eingabe sind wenige Begriffe; das Heft ist im ersten Lauf brauchbar, in der Stunde (90 min) und zu Hause.

## 2 Heftsorten

| Sorte | Inhalt | Auslöser |
|---|---|---|
| Themenheft | Ein Thema, alle Typen, jede Kette vollständig, Decke je Typ das Original | Thema genannt (Standard) |
| Basisheft | Aufgaben im Format des ersten Prüfungsteils (katalog-basis), quer durch alle Themen oder gefiltert („basis prozent") | „basis" |
| Vorbereitung | Fertigkeiten eine Stufe zurück, die das Thema braucht | Zuruf; ohne Zuruf vorangestellt, wenn das Thema an bekannten Vorwissenslücken scheitert (Prozent → Brüche/Dezimalzahlen, Gleichungen → Terme, Körper → Flächen) |
| Fokus | Ein Typ in der Tiefe, wie Masterprompt 2.3 | Typname genannt |
| Test | Prüfungsformat, wie Masterprompt 2.4 | „test", „prüfung" |

Kein eigenes „Problemheft": Ein Thema, das hakt, ist ein Themenheft oder ein Fokus.
Kein Bezug auf Schulfortschritt oder Themenreihenfolge: jedes Heft trägt für sich.

## 3 Rolle des Katalogs

Der Katalog liefert Rahmen, nicht Inhalt:
- Typenliste je Thema aus `typen.csv` – ersetzt das Erraten der Typen (Masterprompt 2.1). Der Schnitt ist damit reproduzierbar.
- Decke je Typ: das Original (Jahr, Aufgabe, Punkte) – ersetzt das geschätzte „Prüfungsniveau" (Masterprompt 2.2 c).
- Ankeraufgabe: Original mit neuen Werten (verfremdet).
- Prüfungsform als Muster für erfundene Aufgaben: Operatoren, Antwortform, Punktegewicht, echte Kontexte.

Der größte Teil des Hefts wird erfunden – Hinführung und Varianten nach der Merkmalskette (Masterprompt 2.2 b). Erfundene Aufgaben treffen die Prüfungsform, nicht nur das Niveau; Vorbild ist die jeweilige Katalogzeile.

## 4 Baurichtung

Rückwärts von der Decke: Welche Merkmale muss ein Schüler beherrschen, um das Original zu schaffen? Daraus die Kette, dann leichter Einstieg (2.2 a), eine Sprosse je Merkmal, Original am Ende. Typenliste und Ketten werden vor dem Bau für das ganze Heft geplant.

## 5 Festlegungen

- Heft ungeschnitten: ein Thema, ein Heft, eine Kette. Ob technisch in Abschnitten gebaut und zusammengesetzt wird, regelt der Prompt (Bauzeit), nicht das Konzept.
- Verfremdetes Original ist Standard-Decke; Zuruf „original" (unverändert) oder „ohne original" (erfundene Aufgabe auf Originalniveau nach Muster der Katalogzeile).
- Begründen bleibt Pflichtelement (Prüfungstyp „Behauptung prüfen"). Fehler-finden nur auf Zuruf, nicht Pflicht. Darstellungswechsel und tragender Kontext bleiben, soweit die Typen es tragen.
- Lösungen (überschreibt konzept.md „vorerst nur Ergebnisse"): Basis → Ergebnis; Kontext → Ergebnis mit Zwischenergebnissen; Original → knapper Lösungsweg mit Stichwort je Schritt, kein Text. Ergebnisse prüft das Skript; Lösungswege sind ungeprüft, daher knapp.
- Heftlänge ergibt sich aus Typen und Merkmalen, kein Zielumfang. Einfaches Thema → kurzes Heft. Schülerbezug („kurz", „schwach") per Freitext wie im Masterprompt.
- Keine Quelle auf dem Schülerblatt, Herkunft im Begleitteil (konzept.md).

## 6 Offen

- Basisheft: Umfang und Mischung der Themen; ob ohne Kette (Prüfungsform hat keine Progression) oder mit kurzer Hinführung je Typ.
- Architektur: Profil am Masterprompt oder eigenständiger MSA-Prompt, der Masterprompt 3–6 übernimmt. Entscheidung nach Stufe 2.
- Nachbau-Test: reichen die Katalogfelder, um Original und Skizze zu reproduzieren? Am ersten Typ prüfen.
- Bauweise ungeschnittener Hefte (ein Lauf vs. Abschnitte + Zusammensetzen); Folgen für protokoll.zip und Testauswertung.
- Testblatt: Typ/Thema noch nicht genannt.

## 7 Nächste Stufen

1. Baurichtung am echten Typ von Hand durchspielen (Kette rückwärts, Katalogfelder, Pflichtelemente).
2. Architektur festlegen.
3. Blatt-Prompt v0.1 und Testblatt über die Pipeline.
4. Basisheft-Logik.

## 8 Änderungslog

- 2026-09-05 v0.1: angelegt nach Chat „Blatt-Konzept" (Heftsorten, Rolle des Katalogs, Baurichtung, Festlegungen zu Umfang, Fehler-finden, Lösungen).
