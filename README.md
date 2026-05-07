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
   git clone https://github.com/YOUR_USERNAME/moodle-bulk-downloader-tracker.git
2. Open `chrome://extensions` in Chrome  
3. Enable **Developer mode** (top right)  
4. Click **Load unpacked** → select the `src/` folder from this repo  
5. The extension icon appears in your toolbar  

---

## 🚀 Usage

1. **Open any Moodle course page** (tested on Moodle 3.9 / 4.x)  
2. **Click the extension icon** in Chrome's toolbar  
3. Two main tabs:

   - **📂 Download materials**  
     → Click "Scan course page" → see list of files → "Download all"  
     *(Files are saved to your default Chrome downloads folder with throttling to avoid server overload)*

   - **📈 Behavior tracker**  
     → Click "Start tracking" → browse Moodle normally → "Export as JSON"  
     *(Export includes: page URLs, entry/exit timestamps, time spent, number of visits, click count, scroll %)*

4. **Optional** – Click "Clear all tracked data" to reset behavior history.

---

## 🧪 Example JSON output (behavior tracker)

{
  "sessionId": "2025-04-07T10-23-15",
  "events": [
    {
      "pageUrl": "https://moodle.myuni.com/course/view.php?id=42",
      "visitStart": "2025-04-07T10:23:18Z",
      "visitEnd": "2025-04-07T10:47:42Z",
      "durationSec": 1464,
      "clickCount": 23,
      "maxScrollPercent": 84
    }
  ]
}

---

## 🛠 Permissions (why & how used)

| Permission | Why needed |
|------------|-------------|
| activeTab | Scan the current open Moodle tab for file links |
| downloads | Save bulk files + export JSON behavior data |
| storage | Store behavior events locally (chrome.storage.local) |

---

## ⚠️ Limitations (realistic expectations)

- **Only works on standard Moodle course sections** (default "Resources" block). Custom themes may break scanning.  
- **Some files require session tokens** – the extension opens them in background tabs; you may need to manually save the first one for some institutions.  
- **Behavior tracking** does not record keyboard input or mouse movement (by design – privacy first).

---

## 🧠 For researchers & teachers

If you use this extension in a study:
- You MUST obtain informed consent from students.  
- All tracking is **opt‑in** via the extension's start button.  
- Data never leaves the student's machine unless they manually export and share it.

---

## 🤝 Contributing

Issues and PRs are welcome!  
Please follow Conventional Commits (https://www.conventionalcommits.org/).

1. Fork the repo  
2. Create a branch: feat/your-feature or fix/your-bug  
3. Test locally  
4. Open a Pull Request  

---

## 📄 License

MIT © [Your Name] – free for academic and personal use.

---

## 🙏 Acknowledgments

- Built for the Moodle community  
- Inspired by real student frustration with manual downloads  
- Uses no external libraries – pure vanilla Chrome extension
