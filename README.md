<p align="center">
  <img src="assets/logo.png" width="96" alt="Printheon logo">
</p>

<h1 align="center">Printheon</h1>

<p align="center">
  <b>One app for your 3D printer. Control, slicing, calibration and repairs, all in the same place.</b>
</p>

<p align="center">
  <a href="README.es.md">Leer en español</a> ·
  <a href="#features">Features</a> ·
  <a href="#supported-printers">Supported printers</a> ·
  <a href="#status">Status</a>
</p>

<p align="center">
  <img src="screenshots/dashboard.png" alt="Printheon dashboard" width="900">
</p>

---

Owning an FDM printer usually means juggling five programs: a slicer, the printer's web panel, a phone app for the camera, a spreadsheet for filament, and a pile of forum threads every time something goes wrong.

Printheon puts all of that in one desktop app. You connect your printer once, and from there you can prepare a model, send it, watch it print, and fix it when it misbehaves. It reads everything the printer knows about itself, so you don't have to type in your machine's settings.

It's built for two kinds of people. **Simple mode** shows only what you need to print and get out of trouble. **Advanced mode** opens up every parameter, the calibration tools, the firmware section and the print farm features.

## Features

### Control your printer
- Temperatures, axes, fans, lights, live speed and flow changes, and an emergency stop.
- Live camera, snapshots and timelapses.
- Files on the printer and a print queue, including a queue that spreads jobs across several printers.
- One dashboard for all your printers.

<img src="screenshots/control.png" alt="Printer control" width="800">

### It reads your printer for you
As soon as it connects, Printheon reads the machine: build volume, nozzle, maximum temperatures, firmware versions, probe offsets, bed mesh and more. It then compares that with the manufacturer's official specs and points out anything that doesn't match.

<img src="screenshots/printer-info.png" alt="Printer info sheet" width="800">

### When something goes wrong
This is the part I built Printheon for. When a printer throws an error, most people end up unplugging cables and swapping fans by hand to rule things out. Printheon automates that:

- **Test the printer piece by piece:** connection, thermistors, every fan one at a time, nozzle and bed heaters, endstops, probe, homing, motion, extruder, filament sensor, lights and camera. Each test turns things on, measures, asks you what you saw, and switches everything off at the end.
- **Error code lookup:** Bambu HMS codes, Prusa error numbers, Klipper and Marlin messages. It explains the error and offers to run the related tests.
- **Guided fixes:** for first layer problems, warping, stringing, under-extrusion, layer shifts, spaghetti, thermal errors and disconnections.

<img src="screenshots/troubleshooting.png" alt="Troubleshooting and printer tests" width="800">

### Unclog and change filament
Automatic or step-by-step unclogging chosen by symptom: hot purge, pulse extrusion, cold pull, heat creep and extruder gears. Temperatures always match the loaded material. Changing filament is guided too, so you swap colours without jams.

<img src="screenshots/unclog.png" alt="Unclog assistant" width="800">

### Calibration
- PID autotune for nozzle and bed. The app runs it, applies the values and saves them.
- Input shaper with the printer's accelerometer.
- Z offset with a sheet of paper, plus babystepping you can save permanently.
- Bed mesh: measure, view and save it.
- Guides for E-steps, pressure advance and belt tension.

<img src="screenshots/calibration.png" alt="Calibration" width="800">

### Failure detection
- **Spaghetti detection with the camera.** It runs on your own computer, needs no internet and no subscription, and can pause the print for you.
- **Telemetry watch.** It warns you about lost temperature, heaters that never reach target, a loose thermistor, a print that stopped advancing, or a lost connection.
- **Remote alerts** on Telegram, Discord or ntfy.

<img src="screenshots/failure-detection.png" alt="Failure detection" width="800">

### Firmware and backups
- Per-model firmware sheets: the official firmware, how to update it, alternative firmwares with their risks, and known issues.
- Update checks for Klipper, Bambu Lab and OctoPrint.
- Automatic backups of your configuration (printer.cfg and macros, RRF config, Marlin EEPROM) that you can restore later.

<img src="screenshots/firmware.png" alt="Firmware and backups" width="800">

### Printing
- **Built-in slicer** using the OrcaSlicer engine, with profiles matched to your printer and material.
- A/B profile comparison and cost estimate per part.
- **3D model search:** browse Printables and Thingiverse by category inside the app, with links to MakerWorld, Thangs, Cults3D and others.
- Filament inventory that subtracts what each print uses.
- Print history and statistics.
- Maintenance reminders based on printing hours.
- Quotes with the real cost of each part, your margin and VAT, and order tracking for people who sell prints.

## Safety first

Printheon will not let you break your printer. Every temperature, speed and flow change, and every command it sends, is checked against the printer's official limits. Anything that goes over them is blocked, whether it comes from a button, a macro, the terminal or a G-code file.

## Supported printers

| Connection | Printers |
|---|---|
| Klipper (Moonraker, Mainsail, Fluidd, RatOS) | Voron, RatRig, Sovol SV08, Elegoo Neptune 4, Qidi Plus4 / Q1 Pro and any other Klipper printer |
| Bambu Lab, local network | X1, P1, A1, H2 |
| PrusaLink | MK4, MK3.5, MINI+, XL, CORE One |
| OctoPrint | Any printer with OctoPrint |
| Duet / RepRapFirmware | Duet 2, Maestro, Duet 3 |
| ESP3D | BigTreeTech, MKS and other WiFi boards |
| Elegoo, local network | Centauri Carbon 2 |
| USB cable | Marlin printers: Ender, Prusa MK3S, Anycubic, Artillery and more |

The built-in catalogue has official specs for around 290 printer models from 58 brands, each one with its source.

## Status

Printheon is in active development and **not released yet**. I'm sharing it now to see if it's useful to other people and to collect ideas before the first public version.

- Platform: Windows (desktop app).
- Language: Spanish for now. English is next.
- Price: free. If you want to support development, there will be a Patreon. No paywalled features.

## Ideas, bugs, printers

Open an [issue](../../issues) if you want to:
- suggest a feature,
- ask for your printer to be supported,
- tell me which tools you use today that Printheon should replace.

---

<sub>Screenshots taken from the current development build with the built-in printer simulator. © Printheon. All rights reserved.</sub>
