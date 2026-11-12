# Modelle und Testumfang

Stand: 12. November 2026. **Bisheriger Hardware-Pilot: ein Bose SoundTouch 20.** Ergebnisse sind nicht automatisch auf andere Serien oder Firmwarestände übertragbar.

## Nachweise auseinanderhalten

1. **Bose-Familie:** Bose nennt das Modell als SoundTouch-kompatibel.
2. **API erreichbar:** Das konkrete Gerät antwortet auf `/info` und weitere benötigte Endpunkte.
3. **Bedienung geprüft:** Lautstärke, Wiedergabe und Standby sind tatsächlich bestätigt.
4. **Radio hörbar:** Der Stream wird auf dem richtigen Gerät wiedergegeben, ohne ungewollte zweite Ausgabe.
5. **Native Presets geprüft:** Die originale Fernbedienung löst den richtigen Sender aus, auch nach Neustart. Das ist ein gesonderter Test mit vorheriger Freigabe.

Ein HTTP-200-Ergebnis oder ein erfolgreiches Unit-Test-Ergebnis belegt keine hörbare Wiedergabe.

## Matrix

| Funktion | SoundTouch 20 im Pilot | Andere SoundTouch-Geräte |
| --- | --- | --- |
| Lokale Grundsteuerung und Standby | Im Betrieb bestätigt | Modell-/Firmwaretest erforderlich |
| Lautstärke und Nachführen externer Änderungen | Im Pilot bestätigt | Zu prüfen |
| Bass | Verwendet | Unterstützung über Gerätefähigkeiten prüfen |
| App-Radio und sechs Favoriten | Im Pilot verwendet | Quellen und Streamformat prüfen |
| Originale Tasten 1–6 | Nach separater Bridge-Einrichtung bestätigt | Nicht zugesagt; gesonderte Freigabe |
| Multiroom | Anbindung vorhanden; kein umfassender Mehrgerätetest dokumentiert | Noch zu prüfen |
| Browserausgabe iPad/iPhone | UI und lokaler Ausgabepfad vorhanden | Betriebssystem, Autoplay und tatsächliches Audioziel prüfen |
| Bluetooth / AirPlay | Systemauswahl angebunden; Kachel ist keine Verbindungsprüfung | Realgerätetest erforderlich |

## Empfohlener Modelltest nach Freigabe

- Modell, Serie, Firmware und Betriebssystemversion dokumentieren, ohne Seriennummer oder Geräte-ID zu veröffentlichen.
- Verbindung lesen und aktuellen Lautstärkewert anzeigen.
- Lautstärke in kleinen Schritten ändern und mit Originalfernbedienung vergleichen.
- Bass nur prüfen, wenn das konkrete Gerät ihn unterstützt.
- Radioquelle starten, pausieren, stoppen und Standby testen.
- SoundTouch ↔ lokale Browserausgabe wechseln; dabei auf doppelte Wiedergabe achten.
- Browseransicht in Hoch- und Querformat prüfen.
- Native Presets nur nach eigener Abstimmung und gesicherter Ausgangskonfiguration prüfen.

## Quellen und Einordnung

- [Bose SoundTouch API](https://assets.bosecreative.com/m/496577402d128874/original/SoundTouch-Web-API.pdf): beschreibt unter anderem Geräteinformationen, Lautstärke, Presets und modellabhängige Klangeinstellungen.
- [Bose: SoundTouch-kompatible Produkte](https://support.bose.com/article/ls650-speakerht5-download-the-bose-soundtouch-app-for-compatible-products---ka08c000000hgwkaau?language=en_US): Produktfamilie, kein Klangraum-Testnachweis. Ältere Zeitangaben dieser Produktseite sind nicht als aktueller Supportstatus zu verwenden.
- [Bose: aktueller Supportstatus](https://www.bose.com/soundtouch-end-of-life): maßgebliche Herstellerseite für das Ende der Cloud-Unterstützung.
