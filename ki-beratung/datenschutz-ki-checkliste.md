# Datenschutz bei KI-Nutzung – Praxis-Checkliste

*Stand: 05.11.2026 · für Kunden wiederverwendbar (Vermieter, Selbstständige, kleine Betriebe)*

> ⚠️ **Keine Rechtsberatung.** Das ist eine praktische Arbeitsweise, um datensparsam mit KI zu arbeiten. Rechtlich verbindliche Fragen mit Datenschutzbeauftragten, Anwalt oder Verband (z. B. Haus & Grund) klären.

---

## Grundprinzip: Die KI baut die Tabelle, sie sieht die Daten nicht

Fast alles, was der Kunde braucht, geht **ohne** echte personenbezogene Daten in der KI:

| Aufgabe | Datensparsamer Weg |
|---|---|
| Formeln, Struktur, Auswertungen bauen | Mit **Beispieldaten** oder einer **anonymisierten Kopie** arbeiten. Die fertige Formel kommt dann in die echte Tabelle |
| Automatik (Warnungen, Abgleich, Nebenkosten) | Läuft **lokal in Excel** (Formeln, bedingte Formatierung, Power Query). Es verlassen keine Daten den Rechner |
| Briefe und Mails an Mieter | KI schreibt **Vorlagen mit Platzhaltern** ([Name], [Betrag], [Datum]). Ausgefüllt wird lokal, z. B. per Word-Serienbrief aus Excel |
| Fragen zu einem konkreten Fall | Pseudonymisiert fragen: „Mieter A, Wohnung 2, Miete 850 €, zahlt seit 2 Monaten nicht…“ |

**Pseudonymisieren heißt:** Namen, Adressen, IBAN, Telefonnummern, Geburtsdaten durch Kürzel ersetzen (Mieter A, Wohnung 1). Die **Zuordnungstabelle** (Kürzel → echter Name) bleibt nur lokal und geht nie in die KI.

Damit sind die meisten Anwendungsfälle abgedeckt, ohne dass man ein Business-Abo braucht.

---

## Wenn die KI doch mit echten Daten arbeiten soll

Dann ist der KI-Anbieter **Auftragsverarbeiter** (Art. 28 DSGVO). Man braucht:

- [ ] **Auftragsverarbeitungsvertrag (AVV/DPA)** mit dem Anbieter. Den gibt es in der Regel nur bei **Business- oder Team-Tarifen** (z. B. Claude Team/Enterprise, ChatGPT Business/Enterprise, Microsoft 365 Business mit Copilot), **nicht** bei normalen Privat-Abos
- [ ] **Training mit den eigenen Daten ausgeschlossen** (bei Business-Tarifen meist Standard)
- [ ] **Datenübermittlung außerhalb der EU geregelt** (z. B. EU-US Data Privacy Framework oder Standardvertragsklauseln; beim Anbieter prüfen, ggf. Option für Datenspeicherung in der EU)
- [ ] Die Nutzung in einer kurzen **Übersicht der Verarbeitungstätigkeiten** festhalten

**Privat-Abo (Free/Plus/Pro):** Mindestens in den Einstellungen das **Training mit eigenen Chats abschalten**. Das senkt das Risiko, **ersetzt aber keinen AVV**. Also keine echten Mieterdaten hochladen.

**Für einen Privatvermieter mit wenigen Wohnungen** reicht in der Regel das Pseudonymisieren. Ein Business-Abo lohnt sich meist erst, wenn regelmäßig mit echten Daten gearbeitet werden soll.

---

## Datenschutz-Grundlagen für Vermieter (unabhängig von KI)

- [ ] **Speicherort:** Wo liegen die Excel-Dateien? Lokal ist am einfachsten. Bei OneDrive, Google Drive oder iCloud gilt dasselbe wie bei KI-Anbietern
- [ ] **Gerät absichern:** Passwort, Festplattenverschlüsselung (Windows BitLocker / Mac FileVault), Updates
- [ ] **Konten absichern:** Zwei-Faktor-Anmeldung für Mail, Cloud und KI-Konten
- [ ] **Backup:** Regelmäßig, idealerweise verschlüsselt
- [ ] **Nur nötige Daten erheben:** Keine Daten „auf Vorrat“
- [ ] **Löschen:** Daten abgelehnter Bewerber nach einigen Monaten löschen. Daten ehemaliger Mieter löschen, sobald die Aufbewahrungsfristen abgelaufen sind (Fristen mit dem Steuerberater klären)
- [ ] **Datenschutzinformation für Mieter** (Art. 13 DSGVO). Vorlagen gibt es z. B. bei Haus & Grund

---

## Spezialfall: Belege und Kontoauszüge in Claude hochladen und zuordnen lassen

### Erst unterscheiden: Was steht in den Dokumenten?
| Dokument | Wessen Daten? | Risiko |
|---|---|---|
| Rechnungen an ihn (Handwerker, Stadtwerke, Versicherung, Grundsteuer, Hausgeld) | Vor allem **seine eigenen** Daten und Firmendaten | **gering**. Über seine eigenen Daten darf er selbst entscheiden. Nur prüfen, ob ein **Mietername** draufsteht („Reparatur bei Frau X“) |
| Kontoauszug | **Mieternamen + IBAN** bei den Mieteingängen | **relevant** |
| Mietverträge, Selbstauskünfte, Übergabeprotokolle | Mieterdaten | **hoch**, nicht hochladen ohne AVV |

**Ehrlich gesagt:** Sobald Mieterdaten drin sind, ist das Hochladen in ein Privat-Abo ohne AVV rechtlich nicht sauber. Das praktische Risiko ist bei einem Privatvermieter überschaubar. Als Berater empfehle ich trotzdem den sauberen Weg.

### Option 1: Hybrid (meine Empfehlung für den Start)
1. **Mieteingänge macht Excel, nicht die KI.** Eine Zuordnungstabelle IBAN → Mieter (bzw. Kürzel), dann ordnet XVERWEIS die Zahlungen lokal zu. Das ist zuverlässiger als KI und datenschutzmäßig kein Thema.
2. **Kontoauszug bereinigen:** In Excel ein Blatt „Für KI“, das nur die **Ausgaben** enthält. Namen von Privatpersonen werden per Formel durch Kürzel ersetzt.
3. **Nur die bereinigten Ausgaben** an Claude geben und kategorisieren lassen (Prompt siehe unten), dann das Ergebnis zurück in Excel kopieren.
4. **Belege (PDF/Foto):** Vor dem Hochladen kurz prüfen, ob ein Mietername draufsteht. Wenn ja, schwärzen (viele Scan-Apps und PDF-Programme können das) oder diesen Beleg von Hand erfassen.
5. Training mit eigenen Chats in den Claude-Einstellungen **abschalten**.

### Option 2: Business-Tarif mit AVV
- KI-Tarif für Teams/Unternehmen mit AVV (z. B. Claude Team, ChatGPT Business, Microsoft 365 Business mit Copilot). Dann darf er auch Dokumente mit Mieterdaten hochladen.
- Nachteil: teurer, teils mit Mindestanzahl an Nutzern. Aktuelle Preise und Bedingungen vorher prüfen.
- Variante für später: Ich baue ihm ein kleines Tool über die **API** (Geschäftsbedingungen + AVV, Abrechnung nach Verbrauch, meist nur wenige Euro im Monat). Das wäre ein eigenes Projekt mit Wartungsaufwand.

### Option 3: Fertige Vermieter-Software
- Viele Vermieter-Programme bieten **Belegerfassung per Foto, Bankabgleich und Nebenkostenabrechnung**, oft mit AVV und Servern in Deutschland. Das ist genau sein Anwendungsfall.
- Kosten meist ein paar Euro pro Wohnung und Monat. Funktionen, Export nach Excel und AVV vor einer Empfehlung prüfen.
- Nachteil: Er müsste von Excel weg (zumindest teilweise).

### Option 4: Lokale KI (für Technik-Fans)
- KI-Modell läuft auf dem eigenen Rechner (z. B. mit LM Studio oder Ollama), es verlassen keine Daten den PC.
- Nachteile: schwächere Ergebnisse beim Lesen von Belegen, braucht einen guten Rechner, mehr Einrichtungsaufwand. Eher nichts für ihn, aber ein spannendes Thema für mich als Berater.

### Prompt-Vorlage: Belege auslesen
> Du bekommst Belege für die Vermietung meiner Wohnungen (Wohnung 1, 2, 3). Erstelle eine Tabelle mit den Spalten: Datum | Lieferant | Betrag brutto | Kategorie | Wohnung | Umlagefähig (ja/nein/unklar) | Bemerkung.
> Kategorien: Instandhaltung, Versicherung, Grundsteuer, Hausgeld, Energie/Wasser, Müll, Hausmeister, Verwaltung, Sonstiges.
> Wenn du dir bei etwas nicht sicher bist, schreib „unklar“ statt zu raten. Gib die Tabelle so aus, dass ich sie direkt in Excel einfügen kann.

### Prompt-Vorlage: Kontoauszug-Ausgaben kategorisieren
> Hier sind Ausgaben aus meinem Vermietungskonto (Datum | Empfänger | Verwendungszweck | Betrag). Ordne jeder Zeile eine Kategorie und, wenn erkennbar, die Wohnung zu. Kategorien: [wie oben]. Markiere Unsicheres mit „unklar“. Ausgabe als Tabelle zum Einfügen in Excel.

**Wichtig:** Die KI-Zuordnung immer kurz prüfen, vor allem „umlagefähig“ und alles, was steuerlich relevant ist. Die KI bereitet vor, die Verantwortung bleibt bei ihm bzw. beim Steuerberater.

---

## Für mich als Berater: Wie ich mit Kundendaten umgehe

- **Am liebsten gar keine echten Kundendaten bekommen.** Ich baue mit einer anonymisierten Kopie oder mit Beispieldaten und übergebe die fertige Tabelle.
- Wenn ich mit echten Daten arbeiten muss, dann **beim Kunden am Rechner**, z. B. vor Ort oder per Bildschirmfreigabe, wobei er die Kontrolle behält.
- Wenn Kundendaten doch bei mir landen, bin ich selbst Auftragsverarbeiter. Dann **einen AVV mit dem Kunden** abschließen (Mustervorlagen z. B. von Bitkom oder der GDD) und die Daten nach dem Projekt löschen.
- **Im Angebot erwähnen:** „Ich arbeite datensparsam. Ihre Mieterdaten verlassen Ihren Rechner nicht.“ Das ist gleichzeitig ein **Verkaufsargument**.
- Keine Datenschutzberatung anbieten, sondern eine **datensparsame Arbeitsweise**. Ich bin kein Datenschutzbeauftragter.

---

## Kurzfassung für den Kunden (zum Weitergeben)

1. Echte Namen und Kontodaten kommen **nicht** in die KI.
2. Die KI baut Formeln, Vorlagen und Strukturen mit Beispieldaten.
3. Die echten Daten bleiben in Excel auf dem eigenen Rechner.
4. Bei konkreten Fragen pseudonymisieren: „Mieter A“ statt Name.
5. Training mit den eigenen Chats in den KI-Einstellungen abschalten.
6. Rechner, Konten und Backups absichern.
