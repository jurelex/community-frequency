# Offline Mapping and Terrain Preparation

## Community Frequency — Peru 2026 Field Research

**Status:** Phase 0 preparation
**Purpose:** Offline geographic, access, settlement, and terrain analysis for field research.

---

## 1. Purpose

Community Frequency uses offline geographic data to prepare for field observation in areas where conventional connectivity may be limited.

The mapping workflow supports research questions involving:

- settlement distribution
- road and trail access
- waterways
- terrain and elevation
- line-of-sight considerations
- potential mobility routes
- possible elevated observation environments
- GPS/GNSS field observations
- field-site documentation

The maps are research instruments. They do not determine deployment locations in advance.

---

## 2. Offline-First Principle

Field preparation should not depend on continuous Internet connectivity.

Source data is downloaded while connectivity is available, processed locally, and organized into a field-ready geographic workspace.

The local workspace is maintained separately from the public Git repository.

Large raster and vector datasets are intentionally excluded from the public repository.

---

## 3. OpenStreetMap Data

A Peru OpenStreetMap extract was obtained from Geofabrik for offline field preparation.

Snapshot:

`peru-260917.osm.pbf`

The source snapshot is dated September 17, 2026.

The original Peru extract is preserved locally as source data.

A filtered field-oriented extract was created containing:

- highways
- waterways
- places
- natural features
- amenities
- power infrastructure
- towers
- man-made infrastructure

The filtered data was converted into GeoPackage layers for local GIS analysis.

---

## 4. Core OSM Layers

A smaller core GeoPackage was prepared for field-oriented analysis.

### Places and Infrastructure

Contains settlement and infrastructure features such as:

- named places
- populated locations
- roads and references
- barriers
- man-made structures
- towers
- other relevant OSM attributes

### Transport, Water and Infrastructure

Contains linear features including:

- major roads
- secondary and tertiary roads
- tracks
- paths
- waterways
- railways
- aerialways
- barriers
- selected man-made infrastructure

These layers provide geographic context for field access and communications experiments.

---

## 5. Peru Mapping Workspace

The local mapping workspace is organized under:

`~/Community-Frequency/data/maps/peru/`

Major categories include:

- boundaries
- field-sites
- geopackages
- osm
- places
- roads
- terrain
- tracks
- water
- waypoints
- exports
- projects
- QGIS data

This organization separates source data, processed data, field observations, and GIS projects.

---

## 6. Terrain Data

Terrain preparation uses SRTM elevation data.

The workflow preserves original compressed elevation tiles and creates derived products separately.

The general processing sequence is:

**SRTM source → HGT → VRT mosaic → DEM → study-area DEM → projected DEM → land mask → land-only DEM → slope / hillshade**

Terrain products are generated locally with GDAL.

# Lima Study Area

## 7. Lima Study Envelope

The initial Lima terrain study area uses:

- West: `-77.30`
- East: `-76.55`
- North: `-11.70`
- South: `-12.55`

The study DEM was clipped from the larger mosaic and projected to UTM Zone 18 South for metric analysis.

CRS:

**EPSG:32718 — WGS 84 / UTM zone 18S**

The projected DEM uses approximately 30 m pixels.

---

## 8. Lima Terrain Products

The Lima workflow produced:

- canonical DEM
- clipped study DEM
- UTM projected study DEM
- Natural Earth land mask
- binary land mask
- land-only DEM
- slope raster
- hillshade raster

The land-only DEM removes ocean pixels from terrain analysis.

---

## 9. Lima Terrain Results

The processed Lima land-only DEM has approximately:

- Minimum elevation: `-31 m`
- Maximum elevation: `4707 m`
- Mean elevation: approximately `1000 m`
- Valid land coverage: approximately `61.6%`

The derived slope raster has:

- Minimum: `0°`
- Maximum: approximately `73.75°`
- Mean: approximately `18.51°`

These statistics describe the study envelope and are not predictions of communications performance.

# Punta Sal Study Area

## 10. Punta Sal Study Envelope

The Punta Sal research area uses a deliberately broad study envelope:

- West: `-81.45`
- East: `-80.85`
- North: `-3.75`
- South: `-4.25`

The project intentionally retains the full envelope rather than reducing the analysis to Punta Sal itself.

This allows comparison among coastal settlements, roads, smaller communities, inland areas, and terrain transitions.

The envelope includes:

- Punta Sal
- Cancas
- Nuevo Cancas
- Máncora
- Máncora Chico
- Vichayito
- Vichayito Norte
- Vichayito Sur
- Los Órganos
- El Ñuro
- Punta Mero
- smaller settlements and isolated dwellings

These locations are geographic research references, not predetermined deployment sites.

---

## 11. Punta Sal SRTM Coverage

The Punta Sal terrain preparation uses four SRTM tiles:

- `S04W081`
- `S04W082`
- `S05W081`
- `S05W082`

The compressed source tiles are preserved locally.

The tiles were verified before processing and decompressed into HGT files.

---

## 12. Punta Sal Terrain Processing

The terrain workflow was:

1. Preserve compressed SRTM source files.
2. Verify source archives.
3. Decompress HGT files.
4. Build an SRTM VRT mosaic.
5. Create a canonical WGS84 DEM.
6. Clip the Punta Sal study envelope.
7. Reproject the study DEM to UTM Zone 17 South.
8. Prepare a Natural Earth land polygon.
9. Reproject the land polygon to the DEM CRS.
10. Rasterize the land polygon to the DEM grid.
11. Create a binary land mask.
12. Generate a land-only DEM.
13. Generate slope.
14. Generate hillshade.

CRS:

**EPSG:32717 — WGS 84 / UTM zone 17S**

The projected terrain products use approximately 30 m pixels.

---

## 13. Punta Sal Terrain Results

The processed Punta Sal land-only DEM has approximately:

- Minimum elevation: `-122 m`
- Maximum elevation: `537 m`
- Mean elevation: `126 m`
- Valid land coverage: approximately `27.0%`

The derived slope raster has:

- Minimum: `0°`
- Maximum: approximately `55.87°`
- Mean: approximately `7.52°`

These statistics are descriptive terrain measurements only.

---

## 14. Land Mask Method

Natural Earth 10m land polygons are used to separate land from ocean within coastal study areas.

The source polygon is first clipped in its native WGS84 geographic CRS and then reprojected to the UTM CRS used by the DEM.

The polygon is then rasterized against the DEM grid.

This avoids incorrectly assigning a geographic CRS to already projected coordinates.

The resulting binary mask distinguishes:

- `1` — land
- `0` — non-land

The land-only DEM assigns NoData to non-land pixels.

---

## 15. Punta Sal Access Network

A field-oriented access dataset was derived from the OSM transport and infrastructure layer.

The extracted feature classes include:

- trunk roads
- primary roads
- secondary roads
- tertiary roads
- unclassified roads
- tracks
- paths
- waterways

The access dataset is used to understand how potential research environments relate to roads, tracks, paths, waterways, and other transportation features.

The extraction is intentionally broader than a simple road-only dataset.

---

## 16. Named Access Features

Examples of named routes identified in the Punta Sal study area include:

- Carretera Panamericana Norte
- Carretera Costanera I
- Valle de Fernández
- Carretera Punta Sal

The presence of a mapped route does not establish that the route is currently passable, publicly accessible, safe, or suitable for field work.

Field verification is required.

---

## 17. Research Environment Classification

The mapping workflow is intended to identify different **research environments**, rather than select predetermined deployment sites.

Possible environment categories include:

- open coastal line-of-sight
- dense settlement
- road/mobile testing
- terrain-obstructed
- inland or valley environment
- elevated terrain
- isolated settlement
- potential elevated/repeater environment

Each candidate environment must eventually be evaluated using field observations.

Relevant factors include:

- actual RF conditions
- terrain and vegetation
- access
- safety
- weather
- power availability
- antenna placement
- community context
- permissions and regulatory requirements
- local technical capacity
- consent and privacy considerations

---

## 18. Mapping and Communications Research

Terrain and mapping data are not treated as substitutes for RF measurements.

A map may suggest that two locations have a clear geographic relationship, but actual communications performance can differ because of:

- vegetation
- buildings
- antenna height
- antenna characteristics
- transmitter configuration
- receiver conditions
- interference
- atmospheric/environmental conditions
- obstructions not represented in the map data

Therefore, geographic analysis is used to formulate and compare field experiments.

---

## 19. Data Integrity

The project follows a preserve-first approach.

Where practical:

1. Preserve original source data.
2. Record source date and provenance.
3. Create derived datasets separately.
4. Do not overwrite source evidence.
5. Record processing steps.
6. Record CRS and spatial extent.
7. Validate output geometry and raster statistics.
8. Keep raw field observations separate from processed products.

Generated GIS datasets remain on the field workstation unless a specific smaller derivative is appropriate for publication.

---

## 20. Reproducibility

The public repository documents methodology and processing logic.

Large source datasets and generated raster/vector products remain outside GitHub because of size and because they are derived research data.

The intended reproducible workflow is:

**Acquire → Preserve → Filter → Process → Validate → Analyze → Document**

Processing tools currently used include:

- GDAL
- PROJ
- GEOS
- SpatiaLite
- osmium
- QGIS

---

## 21. Research Status

The mapping and terrain work represents **Phase 0 preparation**.

It establishes a geographic baseline for field research but does not establish that a particular location should receive a communications installation.

Actual field-site decisions require:

- field observation
- communications testing
- access verification
- regulatory review
- community engagement
- safety assessment
- evidence from repeated experiments

The purpose of this preparation is to make those future observations more systematic and reproducible.

---

**Last updated:** September 2026
