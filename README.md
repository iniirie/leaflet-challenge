# Earthquake & Tectonic Plate Map

An interactive web map built with **Leaflet**, **D3**, and the **USGS Earthquake API** that visualizes the past week’s global seismic activity alongside tectonic‑plate boundaries.

## Features

- Two switchable base‑maps (OpenStreetMap Standard & Humanitarian HOT)
- Circle markers **sized by magnitude** and **colored by depth**
- Live data feed – the map refreshes whenever the USGS GeoJSON endpoint updates
- Overlay of tectonic‑plate boundaries
- Legend explaining the depth‑to‑color ramp
- Layer control to toggle basemaps and overlays

## Demo

![Add a screenshot or GIF here (e.g. `docs/screenshot.png`).](C:\Repos\leaflet-challenge\Code_HTML_Images\Code_HTML_Images\Images\Screenshot 2025-04-10 090604.png)

## Getting Started

### 1. Clone or download the repo

```bash
git clone https://github.com/iniirie/leaflet-challenge.git
```

### 2. Serve the files locally

Because the app fetches remote GeoJSON it must be run from an **HTTP server**, not directly from the filesystem. The quickest way is with Python:

```bash
# Python 3.x
python -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000/) in your browser.

### 4. Folder structure

```
.
├── index.html
├── static
│   ├── css
│   │   └── style.css
│   └── js
│       └── logic.js
└── README.md
```

## Customization

| Task                             | Location                                      |
| -------------------------------- | --------------------------------------------- |
| Change basemap tiles             | `logic.js` → `basemap` & `street` definitions |
| Adjust color ramp / depth breaks | `logic.js` → `getColor()` & legend section    |
| Resize or scale markers          | `logic.js` → `getRadius()`                    |

## Data Sources

- **Earthquakes:** USGS Earthquake Hazards Program weekly GeoJSON feed
   [https://earthquake.usgs.gov](https://earthquake.usgs.gov/)
- **Tectonic Plates:** PB2002 boundaries by Peter Bird, hosted on GitHub
   https://github.com/fraxen/tectonicplates