<p align="center">
  <img src="https://goggles3streamer.micha3582.de/img/Goggles3Streamer-Banner-gh.jpg" alt="Goggles3Streamer Banner" width="100%">
</p>

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

- **DJI Goggles 3** (getestet und verifiziert mit Firmware `v01.00.14.00`)
- **O4 Air Unit**
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
> <p align="center">
>   <img src="https://goggles3streamer.micha3582.de/img/network-toggle.jpg" alt="Live-Ansicht über Wi-Fi für Mobilgerät freigeben" width="480">
> </p>
>
> Das ist mit Abstand der häufigste Grund, warum es bei jemandem nicht geht.

## Loslegen

1. ZIP aus den [Releases](../../releases/latest) herunterladen und entpacken.
2. `Goggles3Streamer.exe` starten:
   - Beim ersten Start meldet SmartScreen *„Der Computer wurde durch Windows geschützt“* (typisch für jedes unsignierte Programm) — auf **Weitere Informationen** klicken, dann **Trotzdem ausführen**.
   - Die Windows-Firewall-Abfrage mit **Zulassen** bestätigen, damit der lokale Datenstrom empfangen werden kann.

<p align="center">
  <img src="https://goggles3streamer.micha3582.de/img/win-smartscreen-warning.jpg" alt="SmartScreen Warnung" width="340">
  &nbsp;&nbsp;
  <img src="https://goggles3streamer.micha3582.de/img/network-permission.jpg" alt="Firewall Freigabe" width="340">
</p>

3. Brille per USB anstecken.
4. Drohne einschalten, bis in der Brille das Livebild steht.

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

Das Programm ist kostenlos und bleibt es — nur der Quelltext bleibt für sich.
Es stecken etliche Feierabende und Wochenenden drin, und die möchte ich mir
gerne bewahren. Wie etwas genau funktioniert, verrate ich aber trotzdem gern:
einfach in den [Issues](../../issues) fragen.

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

<p align="center">
  <img src="https://goggles3streamer.micha3582.de/img/Goggles3Streamer-Banner-gh.jpg" alt="Goggles3Streamer Banner" width="100%">
</p>

**Live video feed from the DJI Goggles 3 on your PC — via USB, straight and simple.**

A private after-work project. Free, no account, no ads, and no internet connection required. It runs locally on your PC and nowhere else.

➡️ **[Download latest release](../../releases/latest)**

---

## Features

| | |
|---|---|
| **Live View** | In a dedicated window, with fullscreen on the monitor of your choice |
| **Recording** | Captures the feed and converts it to MP4 upon exit |
| **Instant Replay** | **Retroactively** saves the last 30 seconds — even if you didn't press record beforehand. Perfect for that crash you never saw coming |
| **Screenshot** | Captures the current frame as a JPEG |
| **Virtual Camera** | Routes the video feed as a webcam into Zoom, Teams, Discord, etc. |
| **Image Adjustments** | Brightness, contrast, saturation — also applied to recordings |
| **16:9 Crop** | Crops black sidebars (display view only) |
| **Bilingual** | German and English, switchable on the fly |

The program configures the network interface for the goggles **automatically**. Windows will prompt for administrator privileges once, and never again after that.

## Requirements

- **DJI Goggles 3** (tested and verified on firmware `v01.00.14.00`)
- **O4 Air Unit**
- **Windows 10 or 11**, 64-bit
- A **data-capable USB cable** (many cables are charge-only)
- Preferably a **USB-A port** on your PC (the flat, rectangular one).  
  With USB-C to USB-C, the goggles often fail to enumerate properly; this is due to USB-C power/role negotiation, not the cable itself.
  
> ### ⚠️ Nothing works without this
>
> Inside the goggles, the tile **"Share live view over Wi-Fi to mobile device"** must be enabled (Quick Menu: swipe down on the 5D button / joystick). Despite "over Wi-Fi" in the name, this toggle **also enables the USB connection**. If disabled, not a single video frame is transmitted — without any error or hint.
>
> <p align="center">
>   <img src="https://goggles3streamer.micha3582.de/img/network-toggle.jpg" alt="Share live view over Wi-Fi to mobile device" width="480">
> </p>
>
> This is by far the most common reason why it doesn't work.

## Getting Started

1. Download the ZIP from [Releases](../../releases/latest) and extract it.
2. Launch `Goggles3Streamer.exe`:
   - On first launch, Windows SmartScreen will prompt *"Windows protected your PC"* (standard for unsigned executables) — click **More info**, then **Run anyway**.
   - When prompted by Windows Firewall / Security, click **Allow** to permit local network streaming.

<p align="center">
  <img src="https://goggles3streamer.micha3582.de/img/win-smartscreen-warning.jpg" alt="SmartScreen Warning" width="340">
  &nbsp;&nbsp;
  <img src="https://goggles3streamer.micha3582.de/img/network-permission.jpg" alt="Network Permission" width="340">
</p>

3. Connect your goggles via USB.
4. Power on your drone until the live view appears inside your goggles.

**Reliable Check:** Upon connecting, the **goggles' internal SD card** must show up as a drive in Windows Explorer. The goggles always register the network adapter and mass storage *together* — if the SD card does not appear, the USB connection is incomplete and no video will be received.

## Troubleshooting

| Symptom | Cause / Solution |
|---|---|
| Nothing happens, frame counter stays at 0 | The sharing tile inside the goggles is turned off |
| "Port 12346 is already in use" | Another streaming tool is still running in the background |
| Windows does not detect the goggles at all | Charge-only cable used, or USB-C to USB-C issue → **Switch to a USB-A port**. If that fails: shut down the PC **and unplug the power cord briefly** (a standard reboot does not reset USB controller state) |
| Video is stuttering or tearing | Press `T` to inspect internal counters — if "dropped" rises, the display pipeline is lagging behind |
| "Air Unit in Low-Power State" | The drone is idling in sleep mode; move it briefly to wake it up |

The application writes runtime logs to `goggles3streamer.log` located next to the executable. This is the first place to check if anything goes wrong.

## Virtual Camera

This feature allows you to use the live stream as a standard webcam in Zoom, Teams, Discord, or web browsers. Enable it under **Settings → Virtual Camera**, then select `OBS Virtual Camera` in your target application.

This requires **[OBS Studio](https://obsproject.com)** to be installed once — only the virtual camera driver bundled with it is needed. **OBS Studio itself does not need to be running.** If the driver is missing, the toggle switch remains greyed out and informs you accordingly.

## Keyboard Shortcuts

| Key | Action |
|---|---|
| `F11` / `F` | Toggle Fullscreen |
| `Esc` | Exit Fullscreen (return to windowed) |
| `R` | Start / Stop Recording |
| `B` | Save Instant Replay |
| `S` | Capture Screenshot |
| `T` | Show Technical Metrics / Counters (Debugging) |

## Why is there no source code?

The program is free and will stay free — but the source code remains closed. A significant amount of evening and weekend work went into this, and I would like to keep it that way. However, if you are curious about how specific parts work under the hood, feel free to ask in the [Issues](../../issues).

## Support / Buy Me a Coffee

If you find this tool useful and want to support it:  
**[ko-fi.com/micha3582](https://ko-fi.com/micha3582)** ☕

Completely optional — no features are locked behind donations.

## Legal & Disclaimer

© 2026 Micha3582. All rights reserved. Use at your own risk.

A **private**, non-commercial hobby project. Not affiliated with, endorsed by, or connected to DJI; "DJI" and "Goggles" are trademarks of their respective owners.

Bundles **[mpv](https://mpv.io)** under the GNU General Public License (GPL) — included unmodified from the [public Windows builds](https://sourceforge.net/projects/mpv-player-windows/), where the corresponding mpv source code is available.
