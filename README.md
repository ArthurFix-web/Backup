# Fix-it-IT Backup – Downloads

Installer für Fix-it-IT Backup (Windows, 64 Bit). Mehr Informationen: https://fix-it-it.de/fix-it-it-backup/

## Version 1.0.10 (aktuell, 24.10.2026) – Sicherheitsupdate

| Version | Datei | SHA-256 |
|---|---|---|
| Standalone | `1.0.10/FixItBackup-Standalone-Setup-1_0_10.exe` | `f29f05c2f8475cea4dc1caf6ee62b239a8cdef90e15c1b83765c8d6dc2a2ffd7` |
| Server | `1.0.10/FixItBackup-Server-Setup-1_0_10.exe` | `6087b80bef2748feeed2481a862f1ac1438374762e8e6395e33f479398ee3c23` |
| Agent | `1.0.10/FixItBackup-Agent-Setup-1_0_10.exe` | `59f76b99dd8c5b9c67cbbb9a5329ca094ca66b42f1535816088741eeda98280d` |

Neu in 1.0.10 – bitte Server und Agents aktualisieren:
- **Wiederherstellung:** Pfade aus einer Sicherung, die aus dem Zielordner hinausführen würden (z. B. `..\`), Gerätepfade und Datenströme werden übersprungen und protokolliert – auch bei VMs und Systemabbildern.
- **Sofortstart:** Die aus der Sicherung bereitgestellten Platten sind nur noch mit einer zufälligen CHAP-Anmeldung je Sitzung erreichbar; andere Programme auf dem Hyper-V-Host haben keinen Zugriff mehr.
- **Agent:** Sicherere Übergabe von VM-Namen und Pfaden an PowerShell (auch typografische Anführungszeichen).
- **Server:** Rechner können Läufe nur noch für eigene Jobs melden.

## Version 1.0.9 (24.10.2026)

| Version | Datei | SHA-256 |
|---|---|---|
| Standalone | `1.0.9/FixItBackup-Standalone-Setup-1_0_9.exe` | `857c91d7f04071cd5f5b337866e74bf2a19eecd7bc5a3b706cf539557a31c5bd` |
| Server | `1.0.9/FixItBackup-Server-Setup-1_0_9.exe` | `100250d8a8f19c334d7560c236144c5273efb780fb59f8a2e5676f7a4c3fa355` |
| Agent | `1.0.9/FixItBackup-Agent-Setup-1_0_9.exe` | `79ae76f9f646ce19b225f0ea3bf07aa3b6237e4d3fee6cd0e94650eb2e2128d4` |

Neu in 1.0.9:
- **Sofortstart (Boot from Backup):** Hyper-V-VMs direkt aus der Sicherung starten – in Minuten statt Stunden. Danach **Abschließen** (die VM wird im laufenden Betrieb zurückgesichert und mit einem kurzen Neustart auf eigene Dateien umgestellt) oder **Verwerfen** (für Wiederherstellungstests). Vorher prüft der Agent, ob der Host genug Arbeitsspeicher frei hat.
- Konsole: Hinweis nach dem Abschließen, Fortschritt aktualisiert sich selbst; alle Zeiten werden jetzt richtig in Ortszeit angezeigt (vorher 1–2 Stunden zu früh).
- Lizenz: Rechner mit Hyper-V-Sicherung zählen als Server-Lizenz (alle VMs inklusive) – auch unter Windows 10/11 Pro.
- Lesbare Fehlermeldungen statt PowerShell-Ausgaben.

Alle Funktionen im Überblick: https://fix-it-it.de/leistungsuebersicht/

## Version 1.0.7 (21.10.2026)

| Version | Datei | SHA-256 |
|---|---|---|
| Standalone | `1.0.7/FixItBackup-Standalone-Setup-1_0_7.exe` | `9aa43d48cbe417d1b52d2cd482aba42d703fec739beb1a9e7b8251e0a3767496` |
| Server | `1.0.7/FixItBackup-Server-Setup-1_0_7.exe` | `eff99b4e8505ee9c3c438151674b475d6fbfa050112c199fdbe5132bcc532aac` |
| Agent | `1.0.7/FixItBackup-Agent-Setup-1_0_7.exe` | `121a790ee469677accfe527edd89265e01b701433bc70a3d06728ff736733bcc` |

Neu in 1.0.7:
- Konsole → „Rechner hinzufügen“ → **Installationsdatei herunterladen**: Die Datei lädt das Agent-Setup, prüft die Prüfsumme und bindet den Agent fest an Ihren Server – Schutz vor einem gefälschten Server im Netz.
- Mehr automatische Tests (Lizenzablauf, Testphase, Lizenzserver nicht erreichbar).

## Version 1.0.6 (20.10.2026)

| Version | Datei | SHA-256 |
|---|---|---|
| Standalone | `1.0.6/FixItBackup-Standalone-Setup-1_0_6.exe` | `b0528cbf881590a8c4256bcbad9f702603f8283f1453efbaef4ab0e3f66ef449` |
| Server | `1.0.6/FixItBackup-Server-Setup-1_0_6.exe` | `eff9c1311c6e881f32d659c0fc91282f3319b719b481990987ad83cf8c510d85` |
| Agent | `1.0.6/FixItBackup-Agent-Setup-1_0_6.exe` | `6badcb1864c854ce5f4860bc340798bd76349f369cc94f5ebb0a05a422f9ab31` |

Neu in 1.0.6:
- Sicherheit: Automatisch angemeldete Rechner müssen in der Konsole freigegeben werden; jeder Rechner erhält nur die Zugangsdaten der Ziele, die er braucht; Datenordner des Servers nur für Administratoren lesbar.
- „Verbindung testen“ an einem Offsite-Ziel legt kein eigenes Repository mehr an (die Offsite-Kopie scheiterte danach).
- Als neue VM wiederhergestellte Hyper-V-Maschinen werden standardmäßig ohne Netzwerkverbindung angelegt.
- Lizenzvertrag ergänzt (Anbieterangaben, nur für Unternehmer, übermittelte Daten).

Update: Setup einfach über die vorhandene Version installieren – Einstellungen, Jobs und Sicherungen bleiben erhalten.

### Download prüfen

Die Installer sind noch nicht digital signiert. Vergleichen Sie die Prüfsumme der heruntergeladenen Datei mit der Tabelle bzw. `1.0.10/SHA256SUMS.txt`:

```powershell
(Get-FileHash .\FixItBackup-Server-Setup-1_0_10.exe -Algorithm SHA256).Hash
```

## Version 1.0.5

| Version | Datei | SHA-256 |
|---|---|---|
| Standalone | `1.0.5/FixItBackup-Standalone-Setup-1_0_5.exe` | `bcbca7f3c8b2b75253e6dc4b35247bd49c5aaa9779a50f534daa783273b4d0c8` |
| Server | `1.0.5/FixItBackup-Server-Setup-1_0_5.exe` | `1de66d8940afed94ae81b7d7807425dd73215eabcb7c6d872bb49cb28c036513` |
| Agent | `1.0.5/FixItBackup-Agent-Setup-1_0_5.exe` | `66b72b67398f7a5d365bbca558f587dd7c1535a791d77f97bc77fde951479108` |
