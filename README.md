# Cartographie — Thèse de doctorat

Travail cartographique réalisé sous QGIS dans le cadre d'une thèse de doctorat portant sur la géographie historique des régions orientales, et plus particulièrement sur les frontières entre les empires sassanide et arabe.

## Structure du projet

```
carte_dr/
├── doctorat.qgz        — projet QGIS principal
├── vecteurs/           — couches vectorielles
└── rasters/            — couches raster
```

## Couches vectorielles (`vecteurs/`)

| Fichier | Contenu |
|---------|---------|
| `centres d'étude.gpkg` | Centres d'étude et monastères |
| `fleuves.kml` | Réseau hydrographique (format KML) |
| `fleuves_grandes.gpkg` | Grands fleuves |
| `fortresses.gpkg` | Fortifications et forteresses |
| `frontière sassanide.gpkg` | Tracé de la frontière sassanide |
| `frontière_arabe.gpkg` | Tracé de la frontière arabe |
| `grandes villes.gpkg` | Grandes villes |
| `montagnes.gpkg` | Massifs montagneux |
| `points.gpkg` | Points divers |
| `régions.gpkg` | Délimitation des régions |

## Couches raster (`rasters/`)

| Fichier | Résolution |
|---------|------------|
| `raster(0,05).tif` | 0,05° |
| `raster(0,1).tif` | 0,1° |
| `rater(0,02).tif` | 0,02° |
| `rater(0,2).tif` | 0,2° |

## Utilisation

Ouvrir le fichier `doctorat.qgz` avec QGIS. Les chemins vers les couches sont relatifs — conserver la structure des dossiers telle quelle.
