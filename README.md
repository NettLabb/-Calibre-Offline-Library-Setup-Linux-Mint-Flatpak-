# 📚 Calibre Offline Library Setup (Linux Mint + Flatpak)

---

## 🧩 What it does

This project documents a stable setup for using **Calibre on Linux Mint (Flatpak)** as an **offline media library manager** for:

* 📖 Ebooks (EPUB, PDF)
* 🎧 Single-file audiobooks (MP3/M4B)
* 🎙️ Podcasts / interviews / long-form talks (downloaded files)
* 🧠 Organized offline knowledge library system

It focuses on solving **crashes, library confusion, and clutter management** while keeping everything fully offline.

---

## ⚙️ How it works

* Calibre runs via **Flatpak** to isolate system library conflicts
* Separate **physical libraries** are used instead of virtual libraries
* Media is organized using:

  * 📁 Dedicated folders per content type
  * 🏷️ Tags for subcategories (e.g., OPSEC, spirituality, fitness)
* Flatpak permissions are overridden to allow access to custom directories
* Stability is improved by disabling GPU acceleration and Qt conflicts

---

## 🛠️ Setup

### 1. Install Calibre (Flatpak)

```bash
flatpak install flathub com.calibre_ebook.calibre
```

---

### 2. Grant folder access

```bash
flatpak override --user --filesystem=/home/op/podcast com.calibre_ebook.calibre
```

---

### 3. Launch Calibre

```bash
flatpak run com.calibre_ebook.calibre
```

---

### 4. Create separate libraries

Inside Calibre:

* Library → Switch / Create Library
* Create folders like:

  * `/home/op/audiobooks`
  * `/home/op/podcast`

---

### 5. Recommended stable launch (if issues persist)

```bash
QT_STYLE_OVERRIDE=Fusion QT_ACCESSIBILITY=0 QTWEBENGINE_DISABLE_GPU=1 QT_QUICK_BACKEND=software flatpak run com.calibre_ebook.calibre
```

---

## 💻 Code

### Stable launch wrapper (recommended)

```bash
#!/bin/bash
QT_STYLE_OVERRIDE=Fusion \
QT_ACCESSIBILITY=0 \
QTWEBENGINE_DISABLE_GPU=1 \
QT_QUICK_BACKEND=software \
flatpak run com.calibre_ebook.calibre
```

---

### Optional: library-specific launch

```bash
flatpak run com.calibre_ebook.calibre --with-library "/home/op/podcast"
```

---

## 🧠 Key Learnings

* Calibre is best used as an **offline library manager**, not a media player
* Virtual libraries are **filters, not real separation**
* Separate **physical libraries = cleanest organization system**
* Tags are more powerful than folder splitting for subtopics
* Flatpak requires **explicit filesystem permissions**
* Most crashes come from:

  * GPU rendering issues
  * Qt/Cinnamon theme conflicts
  * corrupted UI configuration
* Disabling GPU + using Fusion theme improves stability significantly
* Single-file audiobooks work best; multi-file audio can cause instability
* Podcasts/TED talks should be treated as **cataloged media, not streamed content**

---
