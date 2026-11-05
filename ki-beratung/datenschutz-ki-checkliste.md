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
