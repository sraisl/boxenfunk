# Boxenfunk

Ein Arcade-Rennspiel mit Boxenstrategie, das komplett im Browser läuft. Die Perspektive liegt hinter dem Auto, das Rennen entscheidet sich aber am Kommandostand: Wer seine Stopps, Reifen und den Sprit klug plant, fährt vorne mit.

Das ganze Spiel steckt in einer einzigen Datei, [`index.html`](index.html), ohne Build-Schritt und ohne Abhängigkeiten (bis auf die Schriften von Google Fonts).

## Starten

`index.html` im Browser öffnen, fertig. Wer lieber einen lokalen Server nutzt:

```bash
python3 -m http.server 8000
```

Danach <http://localhost:8000> aufrufen.

## Am Kommandostand

Vor dem Start legst du fest:

- **Team:** sechs Teams (Karmin, Nordlicht, Blaufalke, Sunset, Goldhammer, Silberfuchs) mit unterschiedlichen Werten für Höchstgeschwindigkeit, Beschleunigung und Handling
- **Strecke:** Waldring, Küstenring, Sandoval (Wüste, hoher Reifenverschleiß) und der enge Stadtkurs Hafenstadt
- **Renndauer:** 5, 7 oder 10 Runden
- **Klasse:** Rookie (gemütlich), Profi (fordernd) oder Legende (gnadenlos)
- **Strategie:** Anzahl der Stopps und die Reifenmischung je Stint

## Reifen

| Mischung | Tempo | Haltbarkeit |
|----------|-------|-------------|
| Weich (W) | am schnellsten | ca. 2,5 Runden |
| Mittel (M) | ausgewogen | ca. 4,5 Runden |
| Hart (H) | etwas langsamer | ca. 7 Runden |

Driften frisst Reifen, Turbo kostet dreifach Sprit.

## Steuerung

| Taste | Aktion |
|-------|--------|
| Pfeile / WASD | Gas, Bremse, Lenken |
| Leertaste | Geradeaus: Turbo aus der Reserve (gelber Balken). Beim Lenken: Drift, Turbo beim Loslassen |
| Boxengasse | Vor Start/Ziel rechts raus, von der Strecke auf die Spur |
| In der Box | Reifen mit ←/→, Sprit mit ↑/↓, Enter gibt die Crew frei |
| Esc | Pause |
| M | Ton an/aus |

Auf Touch-Geräten erscheinen Bildschirmtasten.

Startest du genau beim Erlöschen der Ampel, bekommst du einen Blitzstart. Gibst du zu früh Gas, gibt es keinen.

## Rekordtafel

Bestzeiten werden pro Strecke, Klasse und Renndauer im `localStorage` des Browsers gespeichert und tragen ein Kürzel aus drei Buchstaben.
