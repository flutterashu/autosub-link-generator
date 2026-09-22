# autosub-link-generator
⚡ A lightweight, zero-dependency web app to generate instant YouTube auto-subscribe links, UTM campaign tags, embed codes, and scannable QR codes. Boost subscriber conversions with one click.


<div align="center">

# 🔴 AutoSub Link Studio

**Instantly generate YouTube auto-confirmation subscription links, campaign tracking tags, and printable QR codes.**

[![License: MIT](https://img.shields.io/badge/License-MIT-red.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/Hosted%20with-GitHub%20Pages-blue.svg)](https://pages.github.com/)
[![Pure HTML/JS](https://img.shields.io/badge/Tech-HTML5%20%7C%20TailwindCSS%20%7C%20JS-18181b.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

[**Live Demo »**](https://flutterashu.github.io/autosub-link-generator/) · [Report Bug](https://github.com/flutterashu/autosub-link-generator/issues) · [Request Feature](https://github.com/flutterashu/autosub-link-generator/issues)

</div>

---

## 📖 Overview

When visitors visit a standard YouTube channel link, they are not prompted to subscribe. By adding the parameter `?sub_confirmation=1`, YouTube displays an automatic confirmation dialog: **"Confirm Channel Subscription"**.

**AutoSub Link Studio** is a client-side web utility that:
1. Normalizes any YouTube URL, `@handle`, or channel ID.
2. Injects the official confirmation parameter safely.
3. Attaches custom UTM campaign tags for cross-platform analytics (Instagram, TikTok, Twitter, newsletters).
4. Generates embeddable HTML buttons, Markdown badges, and high-resolution QR codes.
5. Provides an interactive in-browser preview simulating the native YouTube desktop confirmation popup.

---

## ✨ Features

- **Smart URL Parsing:** Handles `@handles`, bare usernames, custom vanity links (`/c/name`), and canonical channel IDs (`/channel/UC...`).
- **UTM Tag Builder:** Seamlessly append `utm_source`, `utm_medium`, and `utm_campaign` to track where subscribers originate.
- **Subscriber Modal Simulator:** Preview exactly what users see without opening YouTube in a new tab.
- **One-Click Export Formats:**
  - Standard generated URL with one-click clipboard copy.
  - Ready-to-paste HTML button with inline YouTube SVG.
  - Markdown snippet for GitHub profiles and documentation.
  - Social media bio text snippet.
- **Dynamic QR Code:** Auto-generated QR code ready to download for business cards, conference slides, or video end-screens.
- **Zero Dependencies:** Pure vanilla JavaScript and Tailwind CSS via CDN. No build steps, no npm install, no backend servers.

---

## 🚀 Quick Start / Deployment

### Deploy to GitHub Pages in 60 Seconds

1. Fork or push this repository to your GitHub account.
2. Navigate to **Settings** > **Pages** in your repository.
3. Under **Branch**, select `main` (or `master`) and set folder to `/ (root)`.
4. Click **Save**. Your site will be live at:
   ```text
   https://flutterashu.github.io/autosub-link-generator/
   ```

### Local Development

No package manager or build system is required. Clone and open:

```bash
git clone https://github.com/flutterashu/autosub-link-generator.git
cd autosub-link-generator

# Open in your default browser
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

---

## 🛠️ How It Works

Under the hood, the application parses the input string, identifies the channel slug or handle, strips existing conflicting query parameters, and attaches YouTube's native query string:

$$\text{Canonical URL} + \texttt{?sub\_confirmation=1}$$

### Supported Input Formats:
* `@username` &rarr; `https://www.youtube.com/@username?sub_confirmation=1`
* `username` &rarr; `https://www.youtube.com/@username?sub_confirmation=1`
* `https://youtube.com/c/Creator` &rarr; `https://youtube.com/c/Creator?sub_confirmation=1`
* `https://youtube.com/channel/UCxxxx` &rarr; `https://youtube.com/channel/UCxxxx?sub_confirmation=1`

---

## 🤝 Contributing

Contributions are welcome! If you'd like to improve the UI, add new embed templates, or enhance compatibility:

1. Fork the Project.
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`).
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the Branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---

## 📄 License

Distributed under the MIT License. See [LICENSE](LICENSE) for more information.
