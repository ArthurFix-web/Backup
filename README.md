# Fix-it-IT Backup – Downloads

Installer für Fix-it-IT Backup (Windows, 64 Bit). Mehr Informationen: https://fix-it-it.de/fix-it-it-backup/

## Version 1.0.6 (aktuell, 20.10.2026)

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

Die Installer sind noch nicht digital signiert. Vergleichen Sie die Prüfsumme der heruntergeladenen Datei mit der Tabelle bzw. `1.0.6/SHA256SUMS.txt`:

```powershell
(Get-FileHash .\FixItBackup-Server-Setup-1_0_6.exe -Algorithm SHA256).Hash
```

## Version 1.0.5

| Version | Datei | SHA-256 |
|---|---|---|
| Standalone | `1.0.5/FixItBackup-Standalone-Setup-1_0_5.exe` | `bcbca7f3c8b2b75253e6dc4b35247bd49c5aaa9779a50f534daa783273b4d0c8` |
| Server | `1.0.5/FixItBackup-Server-Setup-1_0_5.exe` | `1de66d8940afed94ae81b7d7807425dd73215eabcb7c6d872bb49cb28c036513` |
| Agent | `1.0.5/FixItBackup-Agent-Setup-1_0_5.exe` | `66b72b67398f7a5d365bbca558f587dd7c1535a791d77f97bc77fde951479108` |
