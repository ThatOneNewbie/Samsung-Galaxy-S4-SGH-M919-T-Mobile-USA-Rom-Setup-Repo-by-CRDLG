# Samsung-Galaxy-S4-SGH-M919-T-Mobile-USA-Rom-Setup-Repo-by-CRDLG
# Samsung Galaxy S4 — SGH-M919

Note:The files required have been split into 2 releases due to github upload limits so make sure you have (PT1) and (PT2) with folders "01-06"

A preservation and modification archive for the **T-Mobile USA Samsung Galaxy S4 (SGH-M919)**.

This repository contains the files, tools, recoveries, firmware, ROMs, and notes used to modify **our specific SGH-M919** and install LineageOS 18.1.

> [!WARNING]
> **DEVICE-SPECIFIC REPOSITORY**
>
> The files and instructions in this repository are preserved specifically for the **Samsung Galaxy S4 SGH-M919 (T-Mobile USA)**.
>
> **Do not assume these files or instructions are safe for other Galaxy S4 models.**
>
> Galaxy S4 variants can have different hardware, firmware, partitions, recoveries, and installation requirements. Flashing the wrong files can result in a failed installation or an unusable device.
>
> This repository documents what was tested on **our SGH-M919**. It is not intended to be a universal Galaxy S4 modification guide.

## Device

* **Model:** Samsung Galaxy S4
* **Model number:** SGH-M919
* **Carrier:** T-Mobile USA
* **Storage:** 16 GB
* **RAM:** 2 GB
* **Codename / platform:** jfltexx
* **Original OS:** Samsung Android / TouchWiz
* **Target ROM:** LineageOS 18.1

Samsung's documentation identifies the T-Mobile Galaxy S4 as the SGH-M919. LineageOS documentation also lists the SGH-M919 among the Galaxy S4 variants associated with jfltexx.

## What's in this repository

### `tools/`

Tools used during the modification process.

* Odin
* Samloader-rs
* Other utilities used during the project

### `drivers/`

Drivers required for communication between the phone and Windows.

### `firmware/`

Original Samsung firmware preserved for this specific device.

* `stock/` — original Samsung firmware
* `extracted/` — extracted firmware files when applicable

The stock firmware is preserved so the phone can be returned to Samsung software if necessary.

### `recovery/`

Recovery images used or tested during the project.

* TWRP 3.2.3-0 jfltexx
* TWRP 3.3.1-0 jfltetmo
* Lineage Recovery

### `roms/`

Custom ROMs used in the project.

* LineageOS 18.1 for jfltexx

### `gapps/`

Google Apps packages used with the ROM.

* MindTheGapps 11

### `checksums/`

Checksums for preserved files where available.

These help verify that a downloaded or copied file has not changed.

### `references/`

Links and archived references to useful documentation.

* Official documentation
* XDA resources
* GitHub projects

### `notes/`

Project-specific documentation.

* `device-info.md`
* `flashing-log.md`
* `troubleshooting.md`

These notes record what actually happened during the modification instead of relying entirely on generic guides.

---

# Known-Good Modification Procedure

**This procedure is specifically for our SGH-M919.**

The exact files used for this procedure are preserved in this repository.

## 1. Verify the phone

Before flashing anything, confirm that the phone is:

```text
Samsung Galaxy S4
SGH-M919
T-Mobile USA
```

**STOP if the model does not match.**

Do not substitute another Galaxy S4 variant just because it looks identical.

## 2. Preserve the stock firmware

Keep a copy of the appropriate SGH-M919 T-Mobile stock firmware in:

```text
firmware/stock/
```

Samloader-rs can be used to retrieve Samsung firmware.

The firmware version preserved during this project should be recorded in `device-info.md`.

## 3. Install the required computer tools

Install/use the tools preserved in:

```text
tools/
```

and the appropriate Samsung USB drivers from:

```text
drivers/
```

Verify that the computer can communicate with the phone before attempting to flash anything.

## 4. Enter Download Mode

Power off the S4 and enter Samsung Download Mode using the hardware button combination.

Connect the phone to the computer and verify that the flashing tool detects it.

## 5. Install the recovery used by this project

Use the recovery image documented in `flashing-log.md`.

The recovery must be compatible with the SGH-M919/jfltexx configuration being used.

**Do not substitute a recovery for a different S4 variant.**

## 6. Boot directly into recovery

After installing the custom recovery, boot directly into recovery rather than allowing the stock system to boot first.

Verify that the expected recovery is actually running.

## 7. Wipe/format the required partitions

From recovery, perform the wipes required by the LineageOS installation procedure.

**This deletes data from the phone.**

Make sure anything important has been backed up before continuing.

## 8. Install LineageOS 18.1

Install the preserved LineageOS 18.1 package from:

```text
roms/lineageos-18.1/
```

Use the installation method documented in `flashing-log.md`.

## 9. Install Google Apps

If Google Apps are desired, install the preserved MindTheGapps package from:

```text
gapps/mindthegapps-11/
```

Install it during the same installation process, before the first normal boot.

## 10. Reboot

After all required packages have been installed, reboot the phone.

The first boot can take considerably longer than a normal boot.

## 11. Verify the installation

Once Android starts, verify:

* LineageOS boots normally
* Touchscreen works
* Display works
* Cameras work
* Wi-Fi works
* Bluetooth works
* Cellular functions work where available
* Audio works
* Charging works
* Internal storage works
* microSD works if applicable

Record the results in:

```text
notes/flashing-log.md
```

---

# Important Notes

This repository is a **preservation project**, not an official Samsung or LineageOS distribution.

Files are kept here because older Android modification projects can become difficult to reproduce when downloads disappear, links break, or documentation is lost.

Whenever possible, preserve:

* Original filenames
* Original versions
* Download sources
* Checksums
* Device-specific notes
* Failed attempts
* Successful procedures

Do not replace an older working file with a newer version without documenting the change.

## If something goes wrong

**Do not immediately flash random files from another Galaxy S4 guide.**

First:

1. Stop.
2. Identify the exact model currently shown by the phone.
3. Check `notes/troubleshooting.md`.
4. Check `notes/flashing-log.md`.
5. Verify that the recovery, firmware, and ROM all correspond to the SGH-M919/jfltexx configuration.
6. Use the preserved stock firmware when a return to Samsung software is necessary.

The goal of this repository is to make it possible to reproduce the modification **without having to rediscover the entire process years later.**

