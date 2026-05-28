# 🗺️ Palayan City Interactive Tourism Map

[![Live Demo](https://img.shields.io/badge/Live_Demo-View_Map-27ae60?style=for-the-badge&logo=leaflet)](https://edmarp-sys.github.io/palayan-tourism-map/)
[![Status](https://img.shields.io/badge/Status-Active-blue?style=for-the-badge)](#)

An interactive, web-based digital tourism guide built for the **Palayan City Local Government Unit (LGU)**. This mapping application helps residents and tourists discover premium hotels, local attractions, historical landmarks, and key government offices throughout the capital of Nueva Ecija.

---

## ✨ Key Features

* **Custom UI Interface:** A modern, branded header and a custom collapsible sidebar panel that replaces the standard mapping controls.
* **Dynamic Category Filtering:** Users can toggle different establishment categories (Hotels, Resorts, Attractions, Cafes, etc.) on and off with a single click.
* **Interactive Tourism Cards:** Clicking a map marker opens a beautifully styled, mobile-friendly popup card featuring photos, descriptions, quotes, and direct website links.
* **Dual Basemaps:** Seamlessly switch between a high-resolution **Google Satellite** view and a clean **Google Streets** view directly from the sidebar.
* **Mobile Responsive:** Designed to work perfectly on desktop browsers and scale smoothly down to smartphone screens.
* **WordPress Ready:** Built to be easily embedded directly into the official Palayan City tourism landing page via `iframe`.

---

## 🛠️ Technology Stack

This project was initially exported using QGIS and heavily customized with front-end web technologies:

* **Mapping Engine:** [Leaflet.js](https://leafletjs.com/)
* **GIS Software:** QGIS (Quantum GIS) + `qgis2web` plugin
* **Frontend:** HTML5, CSS3, JavaScript (Vanilla)
* **Icons:** FontAwesome
* **Deployment:** GitHub Pages

---

## 📂 Repository Structure

```text
palayan-tourism-map/
├── index.html           # Main application layout, UI structure, and map logic
├── css/                 # Stylesheets for Leaflet and custom UI elements
├── js/                  # Leaflet core libraries and mapping scripts
├── data/                # GeoJSON files containing Palayan City shapefiles and points
└── images/              # Local image assets used in the popup tourism cards
