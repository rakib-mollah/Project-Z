<div align="center">
  
# 🗺️ Project Z: Analytical Dashboard & AI Intelligence Platform

**An advanced, spatial-intelligence web application and prescriptive analytics platform built to ingest, map, and analyze political, demographic, and developmental data across Bangladesh.**

</div>

---

## 🎥 Project Demonstration

<div align="center">
  <video width="100%" controls>
    <source src="https://github.com/rakib-mollah/Project-Z/raw/main/project%20z%20demo.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <p><em>Interactive geospatial visualization featuring real-time AI policy generation.</em></p>
</div>

---

## 🚀 Overview
**Project Z** couples a responsive, client-side Leaflet visualization engine with an asynchronous Python backend hosting a context-adaptive Large Language Model (LLM) proxy. By blending interactive choropleth heatmaps with LLM-driven prescriptive analytics, the platform transitions raw regional data into immediate, localized policy frameworks and campaign strategies.

### ✨ Key AI Features
* **Context-Aware Ingestion:** Upon drilling down to a localized region (e.g., an Upazila), the built-in AI Assistant automatically loads the active demographic, economic, and infrastructure profiles for that specific boundary.
* **Natural Language Interactivity:** Users can bypass complex database filtering by typing conversational queries directly into the chat interface (e.g., *"how government should plan development here"*).
* **Dual-Persona Automated Strategy Synthesis:** The AI dynamically switches between a **Government Policy Mode** (prescribing socio-economic strategies like daycare hubs or digital financial inclusion) and a **Campaign Strategy Mode** (analyzing voting margins, coalition alignments, and grassroots mobilization).

---

## 🏗️ System Architecture

### 1. Frontend & Mapping Engine (`map_dashboard.html`)
The frontend is an offline-capable Single Page Application (SPA) focusing on high rendering performance.
* **Leaflet.js Rendering:** Utilizes GeoJSON coordinate structures converted to scalable SVG polygon layers for Jatiya Sangsad Constituencies (300 seats) and Upazilas (542 areas).
* **Dynamic Choropleth Scaling:** Applies algorithmic HSL color interpolation scales based on numerical variables (poverty quintiles, population density, institutional households, female NEET counts).
* **Static Script Bundling:** Bypasses CORS limitations by bundling spatial and tabular resources inside variable initializations in standard `.js` files.
* **Glassmorphic UI:** A premium, responsive interface featuring dynamic control sidebars, margin analyzers, and dark/light mode toggles.

### 2. Python Backend Data Pipelines (ETL)
Preparation and optimization of raw census data and geographic boundaries are orchestrated via standalone Python scripts:
* `compile_geojson_v2.py`: Correlates constituency-level metadata with historical poll statistics and high-res union geographies.
* `compile_upazila_geojson.py`: Formats boundary shapes for sub-districts and aggregates voter bases and winner margins.
* `compile_population_data.py`: Pulls socio-economic data (poverty ratios, female literacy, MFS penetration) to generate dedicated key-value map tables for Leaflet styling.

### 3. AI Chat Backend Microservice
An asynchronous, data-injected text generation pipeline providing real-time prescriptive insights.
* **FastAPI & Uvicorn:** High-speed, thread-safe asynchronous backend operations.
* **OpenRouter API Proxy:** Relays conversational payloads to advanced LLMs (defaulted to `google/gemini-2.5-flash`) for low-latency inference.
* **Real-Time Context Builder:** Extracts target area indicators on-the-fly, transforming raw variables (e.g., margin of victory, madrasa count, MFS penetration delta) into formatted system parameters injected ahead of the user conversation log.

---

## 💻 Tech Stack
* **Frontend:** HTML5, CSS3 (Glassmorphism), Vanilla JavaScript, Leaflet.js
* **Backend API:** Python 3.x, FastAPI, Uvicorn, HTTPX
* **Data Processing:** Python, Pandas, GeoJSON
* **AI/LLM:** OpenRouter API (Gemini 2.5 Flash)

---

