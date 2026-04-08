# ElegooNeptune3ProMods

A beginner-friendly walkthrough on my journey modding my Elegoo Neptune 3 Pro.
Written by me as I go — I didn't create any of the software, just documenting the process
to make it easier for others to follow along. Thanks to everyone who helped!

## Requirements
- Elegoo Neptune 3 Pro
- Raspberry Pi 3B or newer
- 1x Micro SD card (will be wiped)
- A good attention span

## Klipper

- [Klipper on GitHub](https://github.com/klipper3d/klipper)
- [Raspberry Pi Imager](https://www.raspberrypi.com/software/)

## 1. Flashing Klipper Firmware to the Printer
1.Format the Micro SD card as FAT32
2. Put the [Firmware](https://github.com/TheFeralEngineer/Klipper-for-Elegoo-Neptune-series-3D-Printers/tree/main/Neptune%203%20Pro%20config/board%20firmware/USB%20communication) on the card
3. **Turn off printer** and **Unplug** the screen 
4. Insert SD card into the printer. **Turn printer back on**
> If you has issues with this later on you can plug the screen back in, which might fix the problem. The screen will forever say "Updating Firmware"

### 2. Installing Mainsail OS
Plug in a micro SD into your computer with the imager (other storage can work, this is just what I'm using).
While in the imager select:
1. **Device:** The Pi you have
2.  **OS:** Other specific purpose → 3D Printing → Mainsail OS
3. **Storage:** Select the storage device you are using (this will be wiped)
4. **Customization:** Set your username and hostname as you want. I will be setting both as `klipper`

Insert the micro SD into the Pi and power it on. It will start the setup process — once it's done, restart if it didn't already and log in.

Your Klipper is now ready. Go to `http://klipper.local` (or whatever hostname you set).

#### 3. Adding Config
> **NOT MINE** This config was created by [TheFeralEngineer](https://github.com/TheFeralEngineer/Klipper-for-Elegoo-Neptune-series-3D-Printers/tree/main) — all credit goes to them.

1. In the Mainsail interface, navigate to the config file editor.
2. Upload or paste the contents of [printer.cfg](printer.cfg) into your `printer.cfg` file.

### 4. Printing
In the Klipper console enter 
```
BED_MESH_CALIBRATE
```
you might have to adjust the Z offset or level a few times.

Find the model you would like to print and put it into the slicer of your choice, set the settings how you would normally. Instead of printing, export the G-code and upload it into Klipper and hit print. You can adjust the speed and extrusion rate in the dashboard for faster prints.

# Physical Printer Modifications
> This section is a work in progress — check back for updates.

## Hotend Upgrades (higher temps)

## Part Cooling

## Bed Upgrades

