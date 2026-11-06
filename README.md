# Indonesia Geospatial Data (Administrative Boundaries & RBI)

This repository contains a curated collection of geospatial datasets covering the Republic of Indonesia. It includes administrative boundaries and base topographic layers suitable for GIS analysis, spatial database management, and web mapping applications.

---

## 📌 Repository Contents

- **Administrative Boundaries**: National, provincial, regency/city (*kabupaten/kota*), district (*kecamatan*), and village/sub-district (*desa/kelurahan*) boundary layers.
- **Indonesian Topographic Map (RBI - Rupabumi Indonesia)**: Fundamental topographic features including road networks, inland waters (rivers and lakes), coastlines, and geographic toponyms.
- **Supported Workflows**: Compatible with standard GIS desktop suites (QGIS, ArcGIS), geospatial databases (PostGIS), Python spatial pipelines (`geopandas`, `shapely`), and modern web mapping libraries (Mapbox GL JS, Leaflet, Deck.gl).

---

## 🌐 Data Source & Attribution

All spatial datasets in this repository originate from official Republic of Indonesia government portals:

1. **Geospatial Information Agency / Badan Informasi Geospasial (BIG)**
   - **Direct Drive Source**: [BIG Public Cloud Storage](https://drive.big.go.id/s/549RG7QoXoJ7Hry?opendetails=)
   - Official provider of national and regional base topographic datasets (*Peta Rupabumi Indonesia*).

2. **Ina-Geoportal (Tanah Air Indonesia)**
   - **Webmap Portal**: [tanahair.indonesia.go.id](https://tanahair.indonesia.go.id/portal-web/webmap)
   - The central node for the National Spatial Data Infrastructure (JIGN) managed by BIG under Indonesia's One Map Policy (*Kebijakan Satu Peta*).

---

## 🚀 Quick Start

### 1. GIS Desktop (QGIS / ArcGIS)
1. Clone this repository or download the release archives.
2. Unpack any compressed archive files (`.zip` / `.tar.gz`).
3. Drag and drop vector files (e.g., `.shp`, `.geojson`, or `.gpkg`) directly into your project canvas.
4. Verify the Coordinate Reference System (CRS) matches your spatial requirements (commonly **WGS 84 / EPSG:4326** or local UTM projections).

### 2. Python (`GeoPandas`)
```python
import geopandas as gpd

# Load vector layers directly into a GeoDataFrame
gdf = gpd.read_file("path/to/dataset.shp")

# Inspect coordinate reference system and initial rows
print(gdf.crs)
print(gdf.head())
```

## ⚖️ License & Attribution Notice

### Data Source & Ownership
The underlying spatial data and topographic features provided in this repository are produced, owned, and maintained by the **Badan Informasi Geospasial (BIG)** (Geospatial Information Agency of the Republic of Indonesia) through the official **Ina-Geoportal / Tanah Air Indonesia** initiative.

- **Data Provider**: Badan Informasi Geospasial (BIG) – Republic of Indonesia
- **Portals**: [Tanah Air Indonesia](https://tanahair.indonesia.go.id/portal-web/webmap) | [BIG Public Data Store](https://drive.big.go.id/s/549RG7QoXoJ7Hry?opendetails=)
- **Legal Context**: Governed under the framework of Indonesia's National Spatial Data Infrastructure (*Jaringan Informasi Geospasial Nasional - JIGN*) and One Map Policy (*Kebijakan Satu Peta* - Perpres No. 9/2016 jo. Perpres No. 23/2021).

### Terms of Attribution
This repository redistributes and organizes the public data for development, research, and analysis purposes. If you use, modify, or integrate these datasets into public applications, research papers, maps, or commercial products, you **must retain attribution** to the original source.

**Suggested Citation / Credit Line:**
> *Spatial data courtesy of Badan Informasi Geospasial (BIG), Republic of Indonesia (Ina-Geoportal: tanahair.indonesia.go.id).*

**BibTeX (for academic or research papers):**
```bibtex
@misc{BIG_Indonesia_Geospatial,
  author       = {{Badan Informasi Geospasial}},
  title        = {{Ina-Geoportal: Portal Informasi Geospasial Terpadu}},
  year         = {2026},
  howpublished = {\url{[https://tanahair.indonesia.go.id/](https://tanahair.indonesia.go.id/)}},
  note         = {Accessed via official repository/public cloud storage}
}
```

## Disclaimer
This dataset is provided "as is", without warranty of any kind, express or implied. The maintainer of this repository does not claim ownership of the underlying geospatial boundaries and is not liable for boundary disputes, administrative discrepancies, or positional inaccuracies originating from the source data. For legal, regulatory, or official land boundary matters, always refer to the verified datasets directly endorsed by the Geospatial Information Agency of Indonesia.
