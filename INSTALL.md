# How to install Buck Tagger

Buck Tagger has three downloads. Get the one for your computer, and the phone app if you want it.

| You have | Download | Size |
|---|---|---|
| 🐧 **Linux** computer | [BuckTagger-Linux-Installer.run](../../releases/latest/download/BuckTagger-Linux-Installer.run) | 270 MB |
| 🪟 **Windows** computer | [BuckTagger-Windows-Setup.exe](../../releases/latest/download/BuckTagger-Windows-Setup.exe) | 264 MB |
| 📱 **Android** phone | [BuckTagger-phone.apk](../../releases/latest/download/BuckTagger-phone.apk): see **[the phone guide](INSTALL-ANDROID.md)** | 111 MB |

All downloads are also on the **[Releases page](../../releases/latest)**.

No account and no administrator password are needed. Buck Tagger installs for your own user only, and once it's
installed it works without internet. It goes online only for map pictures and weather.

To see which computers, phones and cameras it has actually been tested on, read **[TESTED.md](TESTED.md)**.

---

## 🐧 Linux

**You need:** a regular 64-bit PC (Intel or AMD) running Ubuntu 22.04 or newer, Debian 12 or newer, Linux Mint 21 or
newer, Fedora 35 or newer, or another Linux from 2022 or later. You also need about 900 MB of free space while it
installs; it takes about 450 MB once installed. Raspberry Pi and other ARM computers won't work.

### Option A: with the mouse

1. Download **BuckTagger-Linux-Installer.run**. It lands in your **Downloads** folder.
2. Open **Downloads** in your file manager.
3. Right-click an empty spot in the folder and pick **Open in Terminal**.
4. Type this and press **Enter**:
   ```
   bash BuckTagger-Linux-Installer.run
   ```
5. Wait about a minute while it unpacks. When it says Buck Tagger is installed, you're done.
   **Buck Tagger** is now on your desktop and in your app menu.

> **Why a terminal?** Most Linux desktops won't run a downloaded program when you double-click it. Typing that one line is the
> simplest way that works on every Linux. Don't add `sudo`: the installer works under your own user and asks for your
> password only if it needs to.

### Option B: all in the terminal

Copy and paste these lines into a terminal:

```bash
cd ~/Downloads
wget https://github.com/Rudolf-Radio/buck-tagger-public/releases/latest/download/BuckTagger-Linux-Installer.run
bash BuckTagger-Linux-Installer.run
```

(If your computer doesn't have `wget`, use `curl -LO` followed by the same address.)

### If it says something is missing

Some smaller Linux setups don't have every system part a windowed app needs. The installer checks for this. If
anything is missing, it shows the exact parts, asks whether to install them, and then asks for your password. Answer
**Y**. To say yes to that question ahead of time, run:

```bash
bash BuckTagger-Linux-Installer.run --yes
```

### Updating

Download the new installer and run it the same way. Close Buck Tagger first. Your photos, sites, marks and settings
are kept.

### Uninstalling

Paste this into a terminal:

```bash
rm -rf ~/.local/share/bucktagger ~/.local/share/applications/bucktagger.desktop ~/Desktop/bucktagger.desktop
```

This removes the program only. Your photos stay in **Pictures ▸ Buck-tagger**, and your settings stay in
`~/.config/BuckTagger`.

---

## 🪟 Windows

**You need:** Windows 10 or 11, 64-bit, on a regular PC, with about 500 MB of free space.

1. Download **BuckTagger-Windows-Setup.exe**.
2. Double-click it.
3. Windows will probably show a blue **"Windows protected your PC"** box. Click **More info**, then **Run anyway**.
   Windows says this about any program that isn't from a big company that pays Microsoft to sign its programs.
4. Click **Install**. When it's finished, leave **Open Buck Tagger now** ticked and click **Finish**.
5. **Buck Tagger** is now on your desktop and in the Start menu.

The first time it starts, Windows Firewall may ask about network access. Allow it on **private networks**. Buck
Tagger needs that for map pictures, weather and syncing with the phone over Wi-Fi.

> ⚠️ **The Windows version is new.** It has been built and checked on Linux with Wine, a program that runs Windows apps,
> but not yet on a real Windows PC. If anything goes wrong, please
> **[report it](../../issues/new/choose)** so it can be fixed.

### Updating

Close Buck Tagger, then run the new **BuckTagger-Windows-Setup.exe**. Your photos and settings are kept.

### Uninstalling

Open **Settings ▸ Apps**, find **Buck Tagger** and click **Uninstall**. This removes the program only. Your photos
stay in **Pictures\Buck-tagger**.

---

## 🍎 Mac, iPhone, Chromebook

These aren't supported yet. If you'd like one of them, **[leave a suggestion](../../issues/new/choose)**.

---

## Make sure your download isn't damaged (optional)

The Linux installer checks itself every time it runs. To check a file by hand, compare its SHA-256 fingerprint with
the one listed on the [Releases page](../../releases/latest):

- Linux: `sha256sum BuckTagger-Linux-Installer.run`
- Windows (PowerShell): `Get-FileHash BuckTagger-Windows-Setup.exe`
