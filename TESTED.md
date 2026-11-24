# What Buck Tagger has been tested on

This page lists what has **actually been tested**, and what hasn't been tested yet. "Should work" means it's built for
that hardware or software but nobody has tried it there yet.

If you run Buck Tagger on something marked untested, please **[tell us how it went](../../issues/new/choose)**, good or
bad. That's how this list grows.

*Last updated: November 24, 2026 (computer app 2026.11.24, phone app 1.70)*

**Key:** ✅ tested on real hardware · 🧪 tested in a test setup (see notes) · ❔ should work, not tested yet · ❌ not supported

---

## 🐧 Linux computers

| Linux | Status | Notes |
|---|---|---|
| **Ubuntu 24.04** | ✅ | Main development computer: laptop, Intel Core i5-9300H, 8 GB RAM, X11 desktop. Used every day. The download installer was run start to finish on Nov 24, 2026. |
| Ubuntu 22.04 | 🧪 | Passed the full self-test on Nov 24, 2026 |
| Debian 12 | 🧪 | Passed the full self-test on Nov 24, 2026 |
| Debian 13 | 🧪 | Passed the full self-test on Nov 24, 2026 |
| Kali Linux (rolling) | 🧪 | Passed the full self-test on Nov 24, 2026 |
| Fedora 45 | 🧪 | Passed the full self-test on Nov 24, 2026 |
| Linux Mint 21+, Pop!_OS 22.04+, Zorin OS 17+ | ❔ | Based on Ubuntu 22.04 or 24.04, so these should work like Ubuntu |
| RHEL / Rocky / AlmaLinux 9+, openSUSE, Arch, Manjaro | ❔ | Meets the system requirements; the installer knows how to add missing parts on these |
| Wayland desktops | ❔ | Includes Wayland support, but it has only been used on X11 so far. GNOME and KDE on newer distros often use Wayland. |
| Older Linux (Ubuntu 20.04, Debian 11, Mint 20 and older) | ❌ | Too old. Needs glibc 2.34 or newer; the installer checks and tells you. |
| 32-bit PCs, Raspberry Pi and other ARM computers | ❌ | Only built for 64-bit Intel and AMD (x86_64) |

> **🧪 Test setup for Linux:** the app was run against each distro's own system files (downloaded from that distro),
> not on a separate computer with that distro installed. The self-test opens the full program window with every tab,
> loads the map, checks Wi-Fi and Bluetooth sync encryption, and reads the date stamp from a real trail cam photo.

## 🪟 Windows computers

| Windows | Status | Notes |
|---|---|---|
| Windows 10 / 11 (64-bit) | 🧪 | Built and checked on Linux with Wine, which runs Windows apps. The window and every tab open. **It has not been tried on a real Windows PC yet.** |
| Windows installer (Setup.exe) | ❔ | Built, but not yet run on Windows |
| Bluetooth sync on Windows | ❔ | Wine can't test Bluetooth |
| T.REX topo map on Windows | ❔ | Doesn't work under Wine because of a Wine limitation; untested on real Windows |
| Windows on ARM (Snapdragon laptops) | ❔ | Might run through Windows' built-in x64 emulation |
| Windows 7 / 8, 32-bit Windows | ❌ | Not supported |

## 🍎 Mac and Chromebook

❌ Not available yet.

---

## 📱 Android phones

| Phone / Android | Status | Notes |
|---|---|---|
| **Cat S22 Flip** (Android 11) | ✅ | Main test phone. Tested: map, pins, trails, GPS, photos, USB-cable sync, cable-free sync over Wi-Fi and Bluetooth, and the small outside screen. Its USB port can't power a card reader, so **Pull photos** from an SD card reader doesn't work on this phone (a hardware limit). |
| Android 12 | 🧪 | Android emulator (a virtual phone on the computer) |
| Android 14 | 🧪 | Android emulator |
| Android 16 | 🧪 | Android emulator, including a fresh install on a wiped phone with airplane mode on |
| Android 17 | 🧪 | Android emulator: home, map, screens, Back button, typing |
| Samsung Galaxy (newer models) | ❔ | An early version was blocked by Play Protect on a newer Samsung. That was fixed in version 1.27; not checked on a Samsung since. |
| Google Pixel, Motorola, OnePlus and other phones | ❔ | Should work on Android 5 or newer |
| Android 5 to 10 | ❔ | The app is built to run on these, but none have been tested |
| Tablets | ❔ | Should install; the layout was made for phones |
| Pull photos with a USB-C SD card reader | ❔ | Needs a phone whose USB port powers accessories (most newer phones do); not tested on one yet |
| iPhone | ❌ | Not available |

> **🧪 Emulator:** Google's Android emulator runs real Android on the computer. It can't test Bluetooth, real GPS, card
> readers or how fast a real phone is.

## 🔄 Syncing the phone with the computer

| How | Status |
|---|---|
| USB cable, Linux computer | ✅ Tested (Cat S22 Flip) |
| Without a cable over Wi-Fi or Bluetooth, Linux computer | ✅ Tested (Cat S22 Flip) |
| USB cable, Windows computer | ❔ Not tested |
| Without a cable, Windows computer | ❔ Not tested |

---

## 📷 Trail cameras (reading the date stamp)

Buck Tagger reads the date and time **printed on the photo** and can fix a wrong date by re-drawing the stamp in the
camera's own style. Cameras that haven't been tested still go through the automatic reader, which works out most
stamps by itself. If it can't read a photo, it offers to use the date the camera saved inside the file. It always
asks first.

| Camera | Status | Notes |
|---|---|---|
| **Muddy** | ✅ | Tested with photos from Muddy cameras in the field. The first camera it was made for. |
| Stealth Cam Fusion / Fusion Max (cellular) | 🧪 | Sample photos |
| Stealth Cam (other models) | 🧪 | Sample photos |
| Wildgame Innovations | 🧪 | Sample photos |
| Reconyx HyperFire / Professional | 🧪 | Sample photos |
| Tactacam Reveal (cellular) | 🧪 | Sample photos |
| Spartan / GoCam (cellular) | 🧪 | Sample photos |
| Cuddeback | 🧪 | Sample photos |
| Lone Wolf | 🧪 | Sample photos. One style, with white writing on a bright photo and no dark bar, can't be read. |
| Browning | 🧪 | Sample photos |
| Bushnell | 🧪 | Sample photos (white bar with black writing) |
| ScoutGuard / BolyMedia | 🧪 | Sample photos |
| Covert (older DLC models) | 🧪 | Sample photos |
| Moultrie | ❔ | No sample photos yet |
| Spypoint (cellular) | ❔ | No sample photos yet |
| Primos | ❔ | No sample photos yet |
| Any other camera | ❔ | Pick **Any other camera** and it works out the stamp by itself |

> **🧪 Sample photos:** real photos from these cameras, taken from public wildlife-research photo collections
> (such as LILA BC), not from cameras we own. Every photo was checked against the date the camera saved in the file.
> The stamp re-drawing was checked on 33 different camera models.
>
> **Have a camera marked ❔?** A few of its photos, with nothing in them that shows where you hunt, are the best way to
> get it tested. **[Open a suggestion](../../issues/new/choose)** to offer them.
