# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## About this repository

Cartographic project (QGIS) supporting the doctoral dissertation:
**« Les vases communicants. Les savoirs scientifiques anciens au sein des interactions entre les pays d'Islam et l'Empire romain d'Orient (640–867) »**
by Jakub Sypiański (Sorbonne Université, dir. Mathieu Tillier).

The map covers the eastern Mediterranean, 600–900 CE, focusing on the Romano-Sassanid and Romano-Arab frontiers.

## Structure

```
mediterranee-orientale-600-900.qgz   — QGIS project (open this to work)
vecteurs/                            — vector layers
rasters/                             — DEM rasters (source for montagnes.gpkg)
```

## Working with the QGIS project

- Open via `mediterranee-orientale-600-900.qgz`. All layer paths are relative — keep the folder structure intact.
- To inspect or modify `.gpkg` files programmatically, use `ogrinfo` / `ogr2ogr` bundled with QGIS:
  `/Applications/QGIS-LTR.app/Contents/MacOS/bin/ogrinfo`
  `/Applications/QGIS-LTR.app/Contents/MacOS/bin/ogr2ogr`
- The `.qgz` file is a zip archive containing `doctorat.qgs` (XML) and `vHZWda_styles.db`. To edit the project XML: unzip, edit, rezip, replace.

## Key layers

| File | Notes |
|------|-------|
| `vecteurs/terre.gpkg` | World countries basemap (Natural Earth 50m) — displayed as white land fill |
| `vecteurs/frontière_sassanide.gpkg` | Romano-Sassanid frontier |
| `vecteurs/frontière_arabe.gpkg` | Romano-Arab frontier |
| `vecteurs/fortresses.gpkg` | Partial selection of fortresses mentioned in the thesis |
| `vecteurs/grandes_villes.gpkg` | Cities relevant to the thesis — not exhaustive |
| `vecteurs/montagnes.gpkg` | Mountain polygons with `ELEV_MIN`/`ELEV_MAX` attributes; vectorised from DEMs at 1 500 m threshold, 500 m intervals up to 4 500 m |
| `rasters/*.tif` | Source DEMs for montagnes.gpkg; kept for potential regeneration with different parameters |

## Important conventions

- All filenames use underscores, no spaces.
- All `.gpkg` layers are in WGS 84 (EPSG:4326).
- The raster files follow the naming pattern `raster(resolution).tif` (e.g. `raster(0,05).tif`).
- Geographic data reflects places relevant to the thesis — not representative of overall historical significance in the region.
