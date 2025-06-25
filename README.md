# 💻 My CachyOS Linux Setup

[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](./README.pt-br.md)

Welcome to my personal configuration repository for **CachyOS**, a powerful and optimized Linux distribution based on Arch. This repo contains my customized settings, tools, and tips for turning your Linux environment into a productivity powerhouse.

---

## 🧠 About CachyOS

CachyOS is a performance-focused Linux distribution based on Arch Linux. It offers:

* ⚡ **Optimized performance** with BORE scheduler and compiled with performance flags
* 🧰 **A user-friendly GUI installer** with KDE Plasma and other desktop environments
* 🔄 **Rolling Release** updates with Arch's bleeding-edge ecosystem
* 📦 Access to AUR, Flatpak, Snap, and native packages
* 🎨 Beautiful theming and customization capabilities out-of-the-box

**Initial Release**: 2022
**Website**: [https://cachyos.org](https://cachyos.org)

---

## 🛠️ My System Overview

* **OS**: CachyOS (Arch-based)
* **DE**: GNOME
* **Terminal**: `kitty` with Dracula theme
* **Text Editor**: VS Code with custom `settings.json`
* **Fonts**: FiraCode Nerd Font

---

## 📥 How to Install CachyOS (Recommended with Ventoy)

1. **Download CachyOS ISO** from [https://cachyos.org/download](https://cachyos.org/download)
2. **Install Ventoy**:
   - **For Windows**:
     1. Download Ventoy from [https://www.ventoy.net/en/download.html](https://www.ventoy.net/en/download.html)
     2. Extract the ZIP file
     3. Run `Ventoy2Disk.exe` as administrator
     4. Select your USB drive and click "Install"
   
   - **For Linux**:
     ```bash
     sudo bash Ventoy2Disk.sh -i /dev/sdX
     ```
     *(Replace `/dev/sdX` with your USB device)*

3. **Copy the ISO** to the Ventoy USB drive by simply dragging and dropping it
4. **Boot from USB** and follow the **CachyOS GUI installer**

> ⚠️ **Warning**: Make sure to select the correct USB drive to avoid data loss!

---

## 💡 Ventoy and GRUB Customization

In addition to the standard installer, I use a customized Ventoy interface with the [Grub-theme-vimix](https://www.gnome-look.org/p/1009236) theme, making the boot menu more beautiful and modern.

There are several ways to apply this customization, but I followed the tutorial in this video: [YouTube - How to customize Ventoy with Vimix theme](https://www.youtube.com/watch?v=CuonyS3xdwg).

---

## 🧾 My VS Code Settings

You can open your VS Code user settings by pressing:

```bash
Ctrl + Shift + P → Preferences: Open Settings (JSON)
```

Paste the following:

```json
{
    // Files and saving
    "files.autoSave": "off",
    "window.confirmSaveUntitledWorkspace": false,

    // Editor appearance
    "editor.fontSize": 16,
    "editor.tabSize": 4,
    "editor.cursorSmoothCaretAnimation": "on",
    "editor.cursorBlinking": "phase",
    "editor.renderLineHighlight": "gutter",
    "editor.parameterHints.enabled": false,
    "breadcrumbs.enabled": true,

    // Terminal
    "terminal.integrated.fontSize": 16,

    // VS Code interface
    "workbench.iconTheme": "material-icon-theme",
    "workbench.activityBar.location": "top",
    "workbench.startupEditor": "none",
    "explorer.confirmDelete": false,
    "explorer.confirmDragAndDrop": false
}
```

---

## 🐱 Terminal: kitty

I use `kitty` as my terminal with:

* Font: `FiraCode Nerd Font`
* Font size: `16.0`
* Theme: `Dracula`
* Transparency and keybindings

To configure it:

```bash
mkdir -p ~/.config/kitty
nano ~/.config/kitty/kitty.conf
```

Example `kitty.conf` snippet:

```conf
# Font size
font_family      FiraCode Nerd Font
bold_font        auto
italic_font      auto
font_size        16.0

# Theme
include dracula.conf

# Useful shortcuts
map ctrl+shift+n new_os_window
map ctrl+shift+enter new_window

# Terminal border colors
background_opacity 0.75
window_padding_width 5

```

---

## 📌 To-Do / Future Additions

* [ ] Optional install script to auto-setup all configs
* [ ] Screenshots and video previews

---

## 📸 Screenshots

*(Screenshots: VS Code, GNOME Desktop, Kitty Terminal, etc)*

---

## 🙌 Contribute

Feel free to fork and adjust for your own Linux workflow. Pull requests are welcome!