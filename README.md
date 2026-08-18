# Goggles3Streamer

**Das Livebild der DJI Goggles 3 auf dem PC — über USB, ohne Umwege.**

Ein privates Feierabendprojekt. Kostenlos, ohne Konto, ohne Werbung, ohne
Internetzwang. Es läuft auf deinem Rechner und sonst nirgends.

➡️ **[Aktuelle Fassung herunterladen](../../releases/latest)**

---

## Was es kann

| | |
|---|---|
| **Livebild** | Im eigenen Fenster, mit Vollbild auf dem Monitor deiner Wahl |
| **Aufnahme** | Schneidet mit und wandelt beim Beenden nach MP4 |
| **Instant-Replay** | Sichert **rückwirkend** die letzten 30 Sekunden — auch wenn du vorher nichts gedrückt hast. Für den Crash, den man nie kommen sieht |
| **Screenshot** | Das laufende Bild als JPEG |
| **Virtuelle Kamera** | Das Bild als Webcam in Zoom, Teams, Discord |
| **Bildanpassung** | Helligkeit, Kontrast, Sättigung — wirken auch in der Aufnahme |
| **16:9-Zuschnitt** | Schneidet die schwarzen Seitenbalken weg (nur in der Anzeige) |
| **Zweisprachig** | Deutsch und Englisch, umschaltbar im laufenden Programm |

Das Netzwerk für die Brille richtet das Programm **selbst** ein. Einmal fragt
Windows nach Administratorrechten, danach nie wieder.

## Was du brauchst

- **DJI Goggles 3** mit einer O4 Air Unit
- **Windows 10 oder 11**, 64 Bit
- Ein **Datenkabel** — viele USB-Kabel sind reine Ladekabel
- Am Rechner möglichst einen **USB-A**-Anschluss (der flache, rechteckige).
  Bei USB-C zu USB-C meldet sich die Brille je nach Gerät nicht an; das liegt
  an der USB-C-Rollenaushandlung, nicht am Kabel.

> ### ⚠️ Ohne das geht gar nichts
>
> In der Brille muss die Kachel **„Live-Ansicht über Wi-Fi für Mobilgerät
> freigeben"** eingeschaltet sein (Schnellmenü: am Steuerkreuz nach unten
> wischen). Trotz „über Wi-Fi" im Namen schaltet sie **auch den Kabelweg**
> frei. Ist sie aus, kommt kein einziges Bild — und nichts weist darauf hin.
>
> Das ist mit Abstand der häufigste Grund, warum es bei jemandem nicht geht.

## Loslegen

1. ZIP aus den [Releases](../../releases/latest) herunterladen und entpacken
2. `Goggles3Streamer.exe` starten

   Beim ersten Mal meldet Windows *„Der Computer wurde durch Windows
   geschützt"*. Das kommt bei jedem Programm ohne gekaufte Signatur — auf
   **Weitere Informationen** klicken, dann **Trotzdem ausführen**.

3. Brille per USB anstecken
4. Drohne einschalten, bis in der Brille das Livebild steht

**Zuverlässiger Test:** Beim Anstecken muss im Explorer die **SD-Karte der
Brille** als Laufwerk auftauchen. Die Brille meldet Netzwerkkarte und
Laufwerk immer *gemeinsam* an — kommt die SD-Karte nicht, ist die Verbindung
unvollständig und es kommt auch kein Bild.

## Wenn kein Bild kommt

| Symptom | Ursache |
|---|---|
| Nichts passiert, Zähler bleibt auf 0 | Die Kachel in der Brille ist aus |
| „Port 12346 ist belegt" | Ein anderes Empfangsprogramm läuft noch |
| Windows sieht die Brille gar nicht | Ladekabel ohne Datenadern, oder USB-C zu USB-C → **USB-A nehmen**. Hilft das nicht: PC herunterfahren **und vom Strom trennen** (ein Neustart setzt die USB-Anschlüsse nicht zurück) |
| Bild zerrissen oder ruckelig | Taste `T` zeigt die Zähler — steigt „verworfen", kommt die Anzeige nicht nach |
| „Air Unit im Energiesparmodus" | Die Drohne schläft, kurz bewegen |

Neben dem Programm liegt `goggles3streamer.log`. Dort steht, was zuletzt
passiert ist — die erste Datei, in die man schaut.

## Virtuelle Kamera

Damit erscheint das Livebild in Zoom, Teams, Discord oder im Browser als ganz
normale Kamera. Einschalten in den Einstellungen unter **Virtuelle Kamera**,
dann dort in der Kameraauswahl `OBS Virtual Camera` nehmen.

Dafür muss einmal **[OBS Studio](https://obsproject.com)** installiert sein —
gebraucht wird nur der Kameratreiber, den es mitbringt. **OBS selbst muss
nicht laufen.** Fehlt der Treiber, bleibt der Schalter grau und sagt das auch.

## Tastenkürzel

| Taste | |
|---|---|
| `F11` / `F` | Vollbild ein/aus |
| `Esc` | Zurück ins Fenster |
| `R` | Aufnahme starten/beenden |
| `B` | Instant-Replay sichern |
| `S` | Screenshot |
| `T` | Technische Zähler (Fehlersuche) |

## Warum es hier keinen Quelltext gibt

Das Programm ist kostenlos und bleibt es. Der Quelltext bleibt trotzdem zu —
es steckt eine Menge Feierabendarbeit darin, und er soll nicht als fertiges
Produkt bei jemand anderem wieder auftauchen. Fragen zur Funktionsweise
beantworte ich trotzdem gern in den [Issues](../../issues).

## Danke

Wenn dir das Programm etwas wert ist:
**[ko-fi.com/micha3582](https://ko-fi.com/micha3582)** ☕

Freiwillig — es fehlt nichts, wenn du nie draufklickst.

## Rechtliches

© 2026 Micha3582. Alle Rechte vorbehalten. Benutzung auf eigene Gefahr.

Ein **privates** Projekt ohne gewerblichen Hintergrund. Kein Bezug zu DJI;
„DJI" und „Goggles" gehören ihren jeweiligen Inhabern.

Enthält **[mpv](https://mpv.io)** unter der GPL — unverändert übernommen aus
den [öffentlichen Windows-Bauläufen](https://sourceforge.net/projects/mpv-player-windows/),
wo auch der Quelltext von mpv erhältlich ist.

---

# English

**Live video from the DJI Goggles 3 on your PC, over USB.**

A private hobby project. Free, no account, no ads, no internet required.

➡️ **[Download the latest version](../../releases/latest)**

**What it does:** live video in its own window, recording to MP4, instant
replay of the last 30 seconds (retroactively — you don't have to press
anything beforehand), screenshots, a virtual camera for Zoom/Teams/Discord,
image adjustment, 16:9 crop, fullscreen, German and English interface. It
sets up the network adapter for the goggles by itself.

**You need:** DJI Goggles 3 with an O4 Air Unit, Windows 10/11 (64-bit), a
real data cable, and preferably a **USB-A** port on the computer (USB-C to
USB-C often fails to enumerate, that's USB-C role negotiation, not the cable).

> **⚠️ Nothing works without this:** In the goggles, the tile **"Share live
> view over Wi-Fi to mobile device"** must be ON. Despite the name it also
> enables the cable path. If it's off, not a single packet arrives and nothing
> hints at why.

**Reliable check:** when you plug in, the goggles' SD card must appear as a
drive in Explorer. Network adapter and storage always enumerate together — no
drive means the connection is incomplete and there will be no picture.

**Virtual camera:** requires the camera driver that comes with
[OBS Studio](https://obsproject.com) — OBS itself does not need to run.

**No source code here:** the program is free and stays free, but the source
stays closed. Questions about how it works are welcome in the
[issues](../../issues).

**Thanks:** [ko-fi.com/micha3582](https://ko-fi.com/micha3582) ☕ — entirely
optional.

© 2026 Micha3582. All rights reserved. Use at your own risk. A private
project, no affiliation with DJI. Includes [mpv](https://mpv.io) under the
GPL, taken unmodified from the
[public Windows builds](https://sourceforge.net/projects/mpv-player-windows/).
