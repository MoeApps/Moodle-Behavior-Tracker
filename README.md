# 📚 Moodle Bulk Downloader + Behavior Tracker

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Chrome Web Store](https://img.shields.io/badge/Chrome-Extension-blue)](https://chrome.google.com/webstore/detail/)
[![Moodle](https://img.shields.io/badge/Moodle-3.9%2B-orange)](https://moodle.org)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)

> Stop downloading lecture PDFs one by one.  
> Understand your own learning behavior with automatic, client‑only tracking.

A lightweight Chrome extension for **Moodle LMS** that gives students two superpowers:

| Feature | What it does |
|--------|----------------|
| ⚡ **Bulk material download** | Scans the current course page for all lectures, labs, handouts, and downloads them with **one click** (throttled to be server‑friendly). |
| 📊 **Behavior tracker** | Records visits, time on page, click patterns, and scroll depth. Export as JSON for personal analysis or research (with consent). |

---

## 🔒 Privacy & Trust (read this first)

- ✅ **All data stays on your machine** – no external servers, no analytics, no telemetry.  
- ✅ Behavior tracking starts **only after you click "Start tracking"** in the popup.  
- ✅ JSON export is manual – the extension never uploads anything.  
- ✅ Requires minimal permissions (see [Permissions](#permissions) below).

---

## 📦 Installation

### Option 1: Chrome Web Store (recommended – once published)
[Add from Chrome Web Store](#) *(link will be added after publishing)*

### Option 2: Developer mode (sideload)
1. Download or clone this repo  
   ```bash
   git clone https://github.com/YOUR_USERNAME/moodle-bulk-downloader-tracker.git
