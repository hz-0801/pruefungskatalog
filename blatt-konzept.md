# Blatt-Konzept – Nachhilfehefte aus dem Prüfungskatalog

Stand 2026-09-06, v0.5. Ergänzt `konzept.md` (Katalog). Für die Heft-Phase gilt bei Widerspruch diese Datei. Baumaschine ist der MSA-Prompt (§5), der nur als Projektanweisung im Aufgaben-Projekt liegt, nicht im Repo: Abschnitte 0–2 eigen, Abschnitte 3–6 aus dem Masterprompt v3.27 übernommen. Diese Datei regelt, was sich durch den Katalog als Quelle ändert; die Bauregeln selbst stehen im Prompt.

## 1 Ziel

Schüler werden themenweise an die P10-Prüfung (MSA) herangeführt, mit alten Prüfungsaufgaben als Maßstab. Nicht durch Vorlage ganzer Prüfungen (das erst am Ende), sondern durch Hefte, die ein Thema von leicht bis Originalniveau aufbauen. Eingabe sind wenige Begriffe; das Heft ist im ersten Lauf brauchbar, in der Stunde (90 min) und zu Hause.

## 2 Heftsorten

| Sorte | Inhalt | Auslöser |
|---|---|---|
| Themenheft | Ein Thema, alle Typen, jede Kette vollständig, Decke je Typ das Original. Entspricht dem ungeschnittenen Lernblatt des Masterprompts: Beispielzeile je Verfahrenstyp, Grundfall drei- bis viermal, Voraussetzungscheck als Aufgabe 1, Hilfe-Seite an | Thema genannt (Standard) |
| Basisheft | Aufgaben im Format des ersten Prüfungsteils (katalog-basis), quer durch alle Themen oder gefiltert („basis prozent"), ohne Hinführung – üben tut das Themenheft | „basis" |
| Vorbereitung | Fertigkeiten eine Stufe zurück, die das Thema braucht | Zuruf; ohne Zuruf vorangestellt, wenn das Thema an bekannten Vorwissenslücken scheitert (Prozent → Brüche/Dezimalzahlen, Gleichungen → Terme, Körper → Flächen) |
| Fokus | Ein Typ in der Tiefe, wie Masterprompt 2.3 | Typname genannt |
| Probeprüfung | Das Format der Prüfung, jede Aufgabe eine verfremdete Katalogzeile. Der Freitext steuert die Auswahl der Zeilen (Jahr, schwer, leicht, Thema, Dauer), nie die Form | „prüfung", „test" |

Kein eigenes „Problemheft": Ein Thema, das hakt, ist ein Themenheft oder ein Fokus.
Kein Bezug auf Schulfortschritt oder Themenreihenfolge: jedes Heft trägt für sich.

## 3 Rolle des Katalogs

Der Katalog liefert Rahmen, nicht Inhalt:
- Typenliste je Thema aus `typen.csv` – ersetzt das Erraten der Typen (Masterprompt 2.1). Jede Hauptnummer ist ein Katalog-Typ, die Kette läuft innerhalb des Typs von leicht bis Decke. Das überschreibt Masterprompt 2.1 („Formel und Umkehrung = ein Typ"): Der Katalog führt Prozentwert, Grundwert und Prozentsatz als drei Typen mit je eigener Decke.
- Häufigkeit je Typ ist Auskunft für den Begleitteil, keine Gewichtung und kein Filter (konzept.md Nr. 9).
- Distraktoren und Fehler-finden-Aufgaben speisen sich aus dem Katalogfeld `fehlerquelle`.
- Alle Originale eines Typs werden Sprossen seiner Kette, nach Niveau geordnet, nicht nach Jahr; Originale gleicher Merkmale sind eine Sprosse (Vorbild das jüngere); Decke ist das Original mit den meisten Merkmalen (bei Gleichstand Punkte, dann jüngeres Jahr) – ersetzt das geschätzte „Prüfungsniveau" (Masterprompt 2.2 c).
- Ankeraufgabe: Original mit neuen Werten (verfremdet).
- Prüfungsform als Muster für erfundene Aufgaben: Operatoren, Antwortform, Punktegewicht, echte Kontexte.

Der größte Teil des Hefts wird erfunden – Hinführung und Varianten nach der Merkmalskette (Masterprompt 2.2 b). Erfundene Aufgaben treffen die Prüfungsform, nicht nur das Niveau; Vorbild ist die jeweilige Katalogzeile.

## 4 Baurichtung

Rückwärts von der Decke: Welche Merkmale muss ein Schüler beherrschen, um das Original zu schaffen? Daraus die Kette, dann leichter Einstieg (2.2 a), eine Sprosse je Merkmal, Original am Ende. Typenliste und Ketten werden vor dem Bau für das ganze Heft geplant.

## 5 Architektur

Eigener MSA-Prompt, kein Profil am Masterprompt. Entscheidung nach Stufe 2, Begründung:
- Abschnitte 0–2 des Masterprompts (Rolle, Blatttypen, Eingabe deuten, Typenliste, Budget und Schnitt in Teile, Teil 0/1, Eingangscheck, Lernblatt kurz) beschreiben einen anderen Mechanismus: Thema → geratene Typenliste → geschnittene Teile. Das MSA-Heft geht von Katalog → Typen → ungeschnittenes Heft aus. Ein Profil müsste den größten Teil dieser Abschnitte überschreiben; was übrig bliebe (Leitziel, Rangfolge, Konventionen, Anspruchslage, Personalisierung, Progression 2.2 a–d, Fokus 2.3, Testformat 2.4), wird übernommen.
- Masterprompt 1.4 ist für Kl. 10 sachlich veraltet („P10 für alle drei Schulformen"; seit 2025/26 keine P10 am Gymnasium, seit 2026 getrennte EBR/FOR-Hefte). Im MSA-Prompt ist der Stoffstand fest: Kl. 10, FOR. Befund für die nächste Masterprompt-Fassung.
- Abschnitte 3–6 werden wortgleich übernommen mit gezielten Abweichungen: 3.1 kein Übersichtskasten (siehe Festlegungen), 3.4 Lösungen, 4.1 Reihenfolge ohne Kasten, 4.2 Hilfe-Seite mit Verweis auf die Formelsammlung, 4.6 Dateinamen mit Typkürzel (`Heft`, `Basis`, `Vorb`, `Fokus_[Typ]`, `Pruefung`) und Rolle (`Schueler`, `Loesungen`, `Start`), Datum nur im Archiv, 6.3 ohne Orientierungszeile (kein Schnitt), protokoll.txt mit Kapitelstruktur statt Schnitt.

Regel gegen Auseinanderlaufen: Änderungen an 3–6 werden zuerst im Masterprompt gemacht und dann in den MSA-Prompt übertragen; der Kopf des MSA-Prompts nennt die Masterprompt-Version, aus der 3–6 stammen. Die Testauswertung gilt für beide Prompts.

Verworfen: gemeinsamer Kern 3–6 als eigene Datei für beide Prompts – sauberer, aber Neustrukturierung des Masterprompts und zwei Dateien je Upload; erst wieder prüfen, wenn ein drittes Profil (abi) dazukommt.

## 6 Festlegungen

- Heft ungeschnitten: ein Thema, ein Heft, eine Kette. Ein Lauf baut das ganze Heft; kein Hauptnummern-Budget, das Protokoll zählt nur. Die Struktur hält der Katalog (Typen, Originale); „folge" baut dasselbe Heft mit neuen Zahlen und Kontexten neu. Keine Spezdatei.
- Verfremdungsregel: Typ, Aufgabenstruktur, Distraktoren-Logik und Rückwärts-Charakter bleiben; Zahlen (glatt, kopfrechenbar) und Kontext wechseln.
- Verfremdetes Original ist Standard-Decke; Zuruf „original" (unverändert) oder „ohne original" (erfundene Aufgabe auf Originalniveau nach Muster der Katalogzeile).
- Begründen bleibt Pflichtelement (Prüfungstyp „Behauptung prüfen"). Fehler-finden nur auf Zuruf, nicht Pflicht. Darstellungswechsel und tragender Kontext bleiben, soweit die Typen es tragen.
- Lösungen (überschreibt konzept.md „vorerst nur Ergebnisse"): Basis → Ergebnis; Kontext → Ergebnis mit Zwischenergebnissen; Original → knapper Lösungsweg mit Stichwort je Schritt, kein Text. Ergebnisse prüft das Skript; Lösungswege sind ungeprüft, daher knapp.
- Heftlänge ergibt sich aus Typen und Merkmalen, kein Zielumfang. Einfaches Thema → kurzes Heft. Schülerbezug („kurz", „schwach") per Freitext wie im Masterprompt.
- Keine Quelle im Heft, auch nicht im Begleitteil; Herkunft und Häufigkeit nur im Protokoll (überschreibt konzept.md Nr. 5).
- Kopfzeile Thema · Heft oben (`\blattkopf`), Seite und Sternlegende unten. Übergeben werden je Heft genau `…_Schueler.pdf` (Aufgaben + Hilfe), `…_Loesungen.pdf`, auf „start" davor `…_Start.pdf`, und das Protokoll-Archiv; das ungeteilte Kompilat nur im Archiv.
- Aufgabenteil mit weiteren Zeilen (`\weit`, Vorlage ab 2026-09-06c); Begleitteil und Hilfe eng. Stern = Niveaumarke, nicht Positionsmarke: jede verfremdete Katalogzeile trägt ihn, auch mitten in der Kette. Legende „⋆ = Prüfungsaufgabe", nie „darf übersprungen werden"; den Text liefert der Prompt als Argument von `\blattkopf*` (Vorlage ab 2026-09-06d), die Vorlage enthält keinen Legendentext.
- Vorablauf nur auf „start": Aufgabe 1–2 zuerst als eigenes PDF, dann das ganze Heft.
- Probeprüfung wortgleich wird nicht gebaut; das Original liegt auf dem Bildungsserver. Ein Jahr in der Eingabe heißt Probeprüfung wie dieses Jahr.
- Kopf-/Fußzeile bleibt: Dateiname, Protokoll und Testauswertung hängen daran. Kein Clean sheet ohne Kopfzeile.
- Kein Übersichtskasten in keinem Heft: Die Prüfung erlaubt die Formelsammlung, der Schüler übt mit ihr. Formeln werden nirgends abgedruckt; Hilfe-Seite und Wissensblock verweisen auf die Formelsammlung.
- Kein eigener Test: Die Generalprobe ist die Originalprüfung (konzept.md Nr. 8). Die Probeprüfung ist ihre verfremdete Fassung mit freier Zeilenauswahl, nie über dem Niveau der Originale.
- Katalogfeld voraussetzungen ist Hinweis, keine Liste: Es enthält aufgabenbezogene Hinweise und Schritte des Themas selbst. Die Fertigkeiten für Check und Vorbereitung leitet der Prompt aus den Rechenschritten ab, eine Stufe zurück.
- Hilfsmittel FOR: Taschenrechner, Formelsammlung, Formelblatt 2014–2026 durchgehend erlaubt, auch in Aufgabe 1. Ab Prüfungsjahr 2028 (Musteraufgaben) hilfsmittelfreier Teil, 10 BE. „Kopfrechenbar" für die Basis-Decke gilt bis dahin aus Gewohnheit, danach aus Vorgabe.
- Prüfungslage 2026: EBR und FOR getrennte Hefte, keine Sternchen; FOR 7 Aufgaben, 15 Seiten; Aufgabe 1 unverändert 10 P, a–j. Kein Gymnasialheft.

## 7 Offen

- Bauzeit: Prozentrechnung (10 Hauptnummern) 504 s und 479 s, Probeprüfung 2025 (7 Aufgaben, 13 Grafiken) 258 s – fast alles Schreibzeit. Ein großes Thema (Lineare Funktionen, 14 Typen) steht als Messung noch aus; Abschnittsbau bisher nicht nötig.
- Vorlage: Dreieck-Makro setzt den Winkel nur an der oberen Ecke (Probeprüfung 1 g musste cos statt sin nehmen); rechte Winkel in Skizzen nicht markierbar.
- niveau_geschaetzt ist eine Erfassungsschätzung; ob „prüfung schwer" trifft, zeigt der erste Bau.
- Nachbartypen (Anregung „MSA-Arbeitsheft": 2–3 schulübliche Typen je Kapitel, die nicht im Katalog stehen): Empfehlung verwerfen – der Katalog ist der Maßstab, Klassenarbeiten sind Sache des Masterprompts. Vom Lehrer nicht entschieden.
- Basisheft: Umfang (Annahme im Prompt 20–30 Teilaufgaben in Zehnerblöcken) am ersten Bau prüfen.
- Skizzen-Probe: reichen die Katalogfelder für Figuren und Netze? Am Typ Winkel oder Pythagoras prüfen (Nachbau für Basis und Kontext ohne Skizze bestanden).
- Heft A (Originalsammlung mit Lösungen): Scope unklar, getrennte Layoutarbeit, nicht Teil dieses Konzepts.
- Vom Lehrer unbestätigt: Vorbereitung ohne Zuruf bei bekannten Vorwissenslücken (§2).
- Katalog prüfen: keine Gymnasial-Aufgabe-1 (hilfsmittelfrei 2019–2025) enthalten; papier-Feld sieht sauber aus.

## 8 Nächste Stufen

1. Baurichtung am echten Typ von Hand durchspielen – abgeschlossen (Prozentrechnung, Übergabe 06.09.2026).
2. Architektur festlegen – abgeschlossen (§5).
3. MSA-Prompt v0.1 – abgeschlossen (blatt-prompt.md, 06.09.2026).
4. Themenheft Prozentrechnung – zweimal gebaut und ausgewertet (06.09.2026), Prompt v0.4.
5. Probeprüfung 2025 – gebaut und ausgewertet (06.09.2026).
6. Themenheft Lineare Funktionen: Bauzeit und Skizzen-Probe.
7. Basisheft einmal bauen.

## 9 Änderungslog

- 2026-09-05 v0.1: angelegt nach Chat „Blatt-Konzept" (Heftsorten, Rolle des Katalogs, Baurichtung, Festlegungen zu Umfang, Fehler-finden, Lösungen).
- 2026-09-06 v0.2: Architektur entschieden (eigener MSA-Prompt, §5). Hauptnummer = Katalog-Typ (§3). Festlegungen ergänzt: Spezdatei, Serienmodell, Verfremdung, Fußzeile, Hilfsmittel, Prüfungslage 2026. Offen bereinigt: Bauweise aufgelöst, Testblatt = Prozent; neu Bauzeitgrenze, Kasten 3.1, Nachbartypen, Heft A. Nach Chat „Stufe 2 Prozentrechnung".
- 2026-09-06 v0.3: nach Durchsprache des Prompts. Originale als Sprossen nach Niveau; ein Lauf ohne Budget; Spezdatei und Serienmodell gestrichen (Katalog hält die Struktur); Check bleibt, voraussetzungen nur Hinweis; Basisheft ohne Hinführung; Test → Probeprüfung mit Freitext-Auswahl; kein Übersichtskasten; Basis-URL auch im Prompt. Stufen 3–6 neu.
- 2026-09-06 v0.4: nach Auswertung Themenheft 2 und Probeprüfung 2025. Herkunft nur im Protokoll; Kopfzeile, zwei PDFs, Vorablauf auf Zuruf; Originale gleicher Merkmale eine Sprosse; Probeprüfung nie wortgleich; Prompt nur als Projektanweisung. Vorlage 2026-09-06c (blattkopf, weit, kreissektor, leerfeld, drei Reparaturen).
- 2026-09-06 v0.5: nach Auswertung Themenheft Prozent 3 („start") und Lineare Funktionen 1. Stern = Prüfungsaufgabe (Niveaumarke); Hilfe-Seite ohne Ergebnisse des Hefts; Dateirollen, Datum nur im Archiv; Skriptausgabe mit Sollwerten; 4.3/5.1 c ohne Widerspruch (Achsenbereich statt Grafik), Seitenfüllung als Maß. Vorlage 2026-09-06d (Legende als Argument). Befund: 2026-09-06c war nicht im Repo, beide Läufe bauten gegen b.
