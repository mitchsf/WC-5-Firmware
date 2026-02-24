
# WordClock-5

A WiFi-based colorful word clock by [Angry Electrons](https://angryelectrons.co). Displays the time in words illuminated within what appears to be a random matrix of letters, in full color with animated effects.

Clocks are available for purchase at [Stocks Clocks](https://stocksclocks.com/index.php/word-clocks-angry-electrons/).

---

## Hardware

- **Display:** 8 rows × 16, 32, or 48 columns of RGB LEDs (1, 2, or 3 boards)
- **16-column:** Time in 5-minute increments
- **32-column:** Time to the minute
- **48-column:** Time to the second
- **Power:** 5V DC, 5.5/2.1mm center positive — **NOT compatible with 12V supplies**
- **Minimum current:** 2A (single board), 4A (double board)

---

## Features

- Displays time in words with full RGB color animations and transitions
- NTP time source with automatic DST adjustment
- UTC offset support including 30 and 45-minute increments
- Three override modes (dim, effects change) by time range and day type
- Color Wheel Timer effect encodes sub-increment time visually
- Optional scrolling announcements from SD card
- Open-source format files — customizable display layout and language
- Web browser configuration via built-in access point
- OTA firmware updates

- Clocks are available for purchase at [Stocks Clocks](https://stocksclocks.com/index.php/word-clocks-angry-electrons/).

---

## Quick Start

1. Connect 5V DC power supply — **do not use 12V**
2. **AP** blinks on the display indicating access point mode
3. Connect to Wi-Fi network **WordClock-5** from any device
4. Enter `192.168.4.1` in a browser
5. Select your Wi-Fi network, enter password, adjust settings, press Save
6. Clock displays **WC5** → **WiFi** → **NTP** → correct time

---

## Buttons

| Button | Action |
|---|---|
| SW1 press | Cycle color effects |
| SW1 press during override | Restore original settings temporarily |
| SW1 hold at power-on | Cycle LEDs through RGB (assembly test) |
| SW1 press at WC5 display | Enter debug mode (fast time cycle) |
| SW2 press | Cycle brightness (10 levels) |
| SW2 hold 5s | Enter AP configuration mode |
| SW2 hold at power-on | Fix RGB color order (release at WC5) |
| SW1+SW2 at power-on | Factory reset + AP mode (release at WC5) |

---

## Configuration

All settings via web browser at `192.168.4.1` while in AP mode. Key settings:

- **Access Point Name** — default is WordClock-5
- **Network SSID / Password** — Wi-Fi to connect to
- **NTP Server** — defaults to `us.pool.ntp.org`
- **Animation / LED Effect / Brightness** — display appearance
- **Override Modes 1–3** — scheduled dim/effect changes by hour and day
- **UTC Offset / DST** — timezone and daylight saving configuration
- **Announcement Color** — color for SD card announcements
- **Cancel Override Timer** — duration SW1 restores settings during override

---

## Announcements

Optional file at `/Announce/Announce.txt` on SD card. Format: `MM-DDMessage text/`

Setting month to `00` repeats the announcement on that day every month. Up to 75 entries, 62 characters each.

---

## Format Files

Format files define LED positions and display logic for each language and board configuration. The single-board English layout is built in. All others require an SD card with a `Language/` folder containing one `.fmt` file.

Format files can be downloaded from [stocksclocks.com](https://stocksclocks.com).

---

## License

Copyright © 2026 Mitchell Feig, d/b/a Angry Electrons. Exclusively distributed by StocksClocks LLC. All Rights Reserved.
