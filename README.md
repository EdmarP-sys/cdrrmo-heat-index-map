# 🌡️ Palayan City CDRRMO Heat Index Monitoring Dashboard

[![Live Demo](https://img.shields.io/badge/Live_Demo-View_Map-e74c3c?style=for-the-badge&logo=leaflet)](https://edmarp-sys.github.io/cdrrmo-heat-index-map/)
[![Status](https://img.shields.io/badge/Status-Active-blue?style=for-the-badge)](#)
[![API](https://img.shields.io/badge/API-OpenWeather_&_OpenMeteo-60a5fa?style=for-the-badge)](#)

An interactive, responsive apparent temperature monitoring dashboard designed for the **Palayan City Local Government Unit (LGU) City Disaster Risk Reduction and Management Office (CDRRMO)**. This EOC tool tracks real-time thermal risks across all 19 barangays of the capital of Nueva Ecija, helping dispatchers and emergency services coordinate responses during periods of extreme heat.

---

## 🌟 Key Features

* **Double-API Resiliency (OpenWeather + Open-Meteo):** 
  * Powered by a primary **OpenWeather API** integration that fetches city-wide weather metrics.
  * Incorporates a silent, high-performance fallback to the keyless **Open-Meteo API** to ensure uninterrupted map operation during API key activation delays or rate limits.
  * Dynamically updates the top-bar weather badge indicator (`OPENWEATHER` or `LIVE METEO`) based on the active API source.
* **100% Geographically Accurate Markers:** Map markers are positioned at the precise geographical centers of the **19 legitimate barangays** (with non-existent barangays removed and renamed according to LGU guidelines).
* **Scientific apparent temperature (NOAA Rothfusz Algorithm):** Implements the official **US National Weather Service (NWS) Heat Index Regression Formula** in Vanilla JavaScript to compute accurate "felt" temperatures from ambient temperatures and relative humidity.
* **Interactive Dynamic Badges:** Circular map markers glow and pulse dynamically according to official hazard thresholds:
  * 🟢 **Normal:** < 27°C
  * 🟡 **Caution:** 27°C - 32°C
  * 🟠 **Extreme Caution:** 33°C - 41°C
  * 🔴 **Danger:** 42°C - 51°C
  * 🟣 **Extreme Danger:** >= 52°C
* **Sleek EOC Interface:** Incorporates a dark slate dashboard (`#050a15`), city-wide risk progress charts, custom safety advisories based on current active threat levels, and integrated direct-dial emergency hotlines (CDRRMO, City Health Office, and BFP).
* **Base Map Switcher:** Supports smooth tile transitions between **Satellite** (default), **Hybrid** (satellite with labels), and **Streets** views.
* **Embed Mode Ready:** Automatically detects the `?embed=true` URL parameter to hide the main EOC header and optimize panel spacings for responsive iframe embedding.

---

## 🛠️ Technology Stack

* **Mapping Engine:** Leaflet.js
* **Weather Services:** OpenWeather Current Weather API & Open-Meteo Forecast API
* **Front-End:** HTML5, CSS3 (Vanilla), JavaScript (Vanilla ES5)
* **GIS Shapefiles:** QGIS (Palayan Boundary Shapefile & Dark Mask Out-of-bounds layer)
* **Deployment:** GitHub Pages

---

## 📂 Repository Structure

The repository has been fully optimized to keep it exceptionally lightweight and clean:

```text
cdrrmo-heat-index-map/
├── index.html           # Main dashboard layout, UI styling, and Leaflet JS logic
├── LICENSE              # Open source license
├── README.md            # Repository documentation
├── css/                 # Leaflet and font styles
│   ├── leaflet.css
│   ├── qgis2web.css
│   ├── fontawesome-all.min.css
│   └── leaflet.photon.css
├── js/                  # Leaflet core libraries and shape mapping scripts
│   ├── leaflet.js
│   ├── Autolinker.min.js
│   ├── labelgun.min.js
│   ├── labels.js
│   ├── leaflet-hash.js
│   ├── leaflet.pattern.js
│   ├── leaflet.photon.js
│   ├── leaflet.rotatedMarker.js
│   └── multi-style-layer.js
└── data/                # Boundary GeoJSON layers
    ├── boundary_administrative_palayancity_1.js   (Neon-blue glowing city borders)
    └── Difference_2.js                            (Dark outer boundary blackout mask)
```

---

## 🔗 How to Embed the Map (HTML Code)

This map is fully prepared to be embedded into WordPress portals, LGU landing pages, or emergency command screens. Copy and paste this responsive `iframe` snippet:

```html
<iframe 
    src="https://edmarp-sys.github.io/cdrrmo-heat-index-map/?embed=true" 
    width="100%" 
    height="650px" 
    style="border: 2px solid #1e293b; border-radius: 16px; box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);"
    allow="geolocation"
    title="Palayan City CDRRMO Heat Index Monitoring Map">
</iframe>
```
