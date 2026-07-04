TERRA PULSE

### Real-time Global Data Dashboard — PWA

> Monitor the whole world in real-time. One app, 31 live data views, 8 themes, zero backend.

**Created by [Rei](https://terrapulse.dpdns.org/)** · MIT License

---

## 🌍 What is TERRA PULSE?

TERRA PULSE is a single-page **Progressive Web App** that brings together real-time data from dozens of free, public APIs into one cohesive, beautiful dashboard. It tracks weather, climate, air quality, earthquakes, crypto, stocks, forex, commodities, world news, space launches, the ISS, internet activity, and much more — all in a single, responsive interface.

Built as **100% static HTML, CSS, and vanilla JavaScript**. There's no backend, no server-side code, no analytics, no tracking. Everything runs in your browser, and once installed it works offline thanks to a service worker that caches all assets.

---

##  Features

###  31 Live Data Views

| Category | Views |
|----------|-------|
| **Overview** | Global Overview, World Map, World Clocks, Command Palette |
| **Environment** | Weather, Air Quality, Earthquakes, Climate, Marine |
| **Markets** | Crypto, Stocks, Forex, Commodities, Calculators |
| **News & Social** | World News, Trends, Wikipedia Pulse |
| **Science & Space** | Space & ISS, Astronomy, Solar System, Launches |
| **Internet & Tech** | Internet Stats, GitHub Trending, Hacker News |
| **Society** | Population, Holidays, Health, Countries |
| **System** | Alerts, Shortcuts, Settings, About |

###  8 Themes
- **Dark** (Aurora — default)
- **Light**
- **AMOLED** (true black — `#000000`)
- **Sunset** (warm orange/pink)
- **Ocean** (deep teal)
- **Forest** (green)
- **Midnight** (deep purple)
- **Neon** (cyberpunk magenta/cyan)

Switch via the palette icon in the topbar, or press **Ctrl+;** to cycle.

###  Accurate World Map
- Real **world-atlas TopoJSON** data (177 countries, Natural Earth public domain)
- Custom TopoJSON decoder + equirectangular projection in vanilla JS
- Live event markers (earthquakes color-coded by magnitude, ISS position)
- Embedded directly in JS — works offline from `file://`

###  Live Animated Heatmaps
- **Forex**: 29-cell color-coded heatmap + 15-row animated bar graph + scrolling ticker
- **Stocks**: 30-symbol heatmap with live opacity flicker animation
- **Crypto**: 30-coin heatmap with embedded sparklines + live price ticker

###  Power-User Features
- **Command Palette** (Ctrl+K) — fuzzy search 40+ commands
- **Keyboard Shortcuts** (Ctrl+/) — full overlay with all shortcuts
- **Global Search** (`/` or Ctrl+K) — cities, coins, views
- **Quick nav** — press `g` then a letter (e.g. `g c` = Crypto)

###  PWA — Installable Everywhere
- Installable on **iOS, Android, Windows, macOS, Linux**
- Works **offline** (service worker caches all assets)
- **Responsive** — phones, tablets, desktops
- No app store required

###  Professional Design
- **Glassmorphism 2.0** UI with backdrop blur
- Animated aurora background + starfield with shooting stars
- 470+ custom SVG outline icons (no emoji)
- Smooth transitions, hover states, skeleton loaders
- Toast notifications + alerts panel
- Animated number counters + sparklines

---

##  Quick Start

### Option 1: Open Directly
```bash
# Download/clone the repo
git clone https://github.com/YOUR_USERNAME/terra-pulse.git
cd terra-pulse

# Just open index.html in any modern browser
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

### Option 2: Local Server (recommended for PWA features)
```bash
# Python
python3 -m http.server 8000

# Node
npx serve

# Then visit http://localhost:8000
```

### Option 3: Install as PWA
1. Open the app in **Chrome** or **Edge**
2. Click the **install icon** in the address bar
3. Or use browser menu → **"Install app"** / **"Add to Home Screen"**

---

## 🔌 Data Sources (all free, no API keys)

| Source | Data |
|--------|------|
| [Open-Meteo](https://open-meteo.com/) | Weather, air quality, climate archive, marine |
| [USGS](https://earthquake.usgs.gov/) | Real-time earthquake feeds |
| [CoinGecko](https://www.coingecko.com/) | Crypto markets & global stats |
| [open.er-api.com](https://www.exchangerate-api.com/) | Live forex rates |
| [Yahoo Finance / Stooq](https://stooq.com/) | Stocks & commodities |
| [Open Notify / NASA](http://open-notify.org/) | ISS, APOD, Mars weather |
| RSS feeds | BBC, NYT, Al Jazeera, Ars Technica, Bloomberg |
| [Hacker News (Algolia)](https://hn.algolia.com/) | Top stories |
| [Wikimedia](https://www.wikimedia.org/) | Recent edits, "On this day" |
| [The Space Devs](https://thespacedevs.com/) | Upcoming launches |
| [Nager.Date](https://date.nager.at/) | Public holidays |
| [disease.sh](https://disease.sh/) | COVID-19 statistics |
| [Cloudflare](https://www.cloudflare.com/) | Network trace, IP info |
| [REST Countries](https://restcountries.com/) | Country data |
| [world-atlas](https://github.com/topojson/world-atlas) | Accurate country boundaries (TopoJSON) |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Languages** | HTML, CSS, vanilla JavaScript |
| **Frameworks** | None (zero dependencies) |
| **Map data** | world-atlas TopoJSON (Natural Earth) |
| **Storage** | localStorage + Cache API |
| **Offline** | Service Worker |
| **Manifest** | Web App Manifest |
| **Icons** | Custom SVG outline library (470+) |
| **Build tools** | None — runs as-is |

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `/` | Focus search |
| `Ctrl+K` | Command palette |
| `Ctrl+/` | Keyboard shortcuts overlay |
| `Ctrl+;` | Cycle theme |
| `Esc` | Close overlay |
| `g` then `o` | Go to Overview |
| `g` then `m` | Go to World Map |
| `g` then `c` | Go to Crypto |
| `g` then `f` | Go to Forex |
| `g` then `s` | Go to Stocks |
| `g` then `n` | Go to News |
| `g` then `w` | Go to Weather |
| `g` then `e` | Go to Earthquakes |
| `g` then `p` | Go to Space & ISS |

---

## 📁 Project Structure

```
terra-pulse/
├── index.html                  # Main app shell
├── manifest.webmanifest        # PWA manifest
├── sw.js                       # Service worker
├── data/
│   └── world-110m.json         # TopoJSON world map (177 countries)
└── assets/
    ├── css/
    │   └── styles.css          # All styles + 8 themes
    ├── icons/
    │   ├── logo.svg            # Astonishing HD logo
    │   ├── icon-192.png        # PWA icon
    │   └── icon-512.png        # PWA icon
    └── js/
        ├── utils.js            # Helpers (formatting, geo, color)
        ├── store.js            # Reactive state + persistence
        ├── api.js              # All API wrappers
        ├── icons.js            # 270+ SVG icons
        ├── icons-extra.js      # 200+ more SVG icons
        ├── world-data.js       # Embedded TopoJSON
        ├── data-cities.js      # 250+ world cities
        ├── data-elements.js    # 118 periodic elements
        ├── starfield.js        # Animated canvas background
        ├── worldmap.js         # TopoJSON decoder + SVG renderer
        ├── app.js              # Main orchestrator
        └── views/              # 31 view modules
            ├── overview.js
            ├── worldmap.js
            ├── clocks.js
            ├── weather.js
            ├── crypto.js
            ├── forex.js
            ├── stocks.js
            └── ... (24 more)
```

---

##  Stats

- **50 files**
- **11,000+ lines** of code
- **31 views**
- **470+ icons**
- **8 themes**
- **15+ free APIs**
- **Zero dependencies**
- **~1MB total size**

---

##  Privacy

TERRA PULSE does **not** collect, store, or transmit any personal data.

- All settings saved locally in your browser's `localStorage`
- No analytics, no tracking pixels, no advertising SDKs
- No third-party scripts (other than direct API calls to data sources)
- Your IP address is sent only to public APIs you actively query — exactly as if you visited those services directly
- The app does not proxy any requests through a server

---

##  Browser Support

Works in all modern browsers:
-  Chrome / Edge 90+
-  Firefox 90+
-  Safari 15+
-  Samsung Internet
-  Brave, Arc, Vivaldi, Opera

PWA installation supported on all platforms.

---

##  Install as App

### Android (Chrome)
Menu → **"Install app"**

### iOS (Safari)
Share → **"Add to Home Screen"**

### Desktop (Chrome/Edge)
Click the **install icon** in the address bar

### Linux / macOS / Windows
Chrome → install

---

##  Contributing

Contributions are welcome! Please:

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

##  License

MIT License — free to use, modify, and distribute.

---

##  Author

**Created by Rei** ⚡

---

##  Acknowledgments

- [Natural Earth](https://www.naturalearthdata.com/) — public domain map data
- [world-atlas](https://github.com/topojson/world-atlas) — TopoJSON package
- All the free public APIs that make this possible
- The open-source community

---

<p align="center">
  <strong> TERRA PULSE</strong><br>
  <sub>Created by <strong>Rei</strong></sub>
</p>
