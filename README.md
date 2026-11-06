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
