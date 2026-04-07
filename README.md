# Cartographie — Thèse de doctorat

Travail cartographique réalisé sous QGIS dans le cadre de la thèse de doctorat :

> **[« Les vases communicants. Les savoirs scientifiques anciens au sein des interactions entre les pays d'Islam et l'Empire romain d'Orient (640–867) »](https://www.orient-mediterranee.com/training/soutenance-de-these-de-jakub-sypianski/)**

Cette carte couvre la Méditerranée orientale entre 600 et 900, avec un focus sur les frontières entre les empires sassanide et arabe. Les données géographiques (villes, points, régions, etc.) reflètent les lieux mentionnés ou pertinents dans le cadre de la thèse et ne sont pas représentatives à cent pour cent de l'importance historique de ces lieux dans la région.

## Structure du projet

```
carte_dr/
├── mediterranee-orientale-600-900.qgz   — projet QGIS principal
├── vecteurs/           — couches vectorielles
└── rasters/            — couches raster
```

## Couches vectorielles (`vecteurs/`)

| Fichier | Contenu |
|---------|---------|
| `terre.gpkg` | Pays du monde (fond de carte) |
| `centres_d'étude.gpkg` | Centres d'étude et monastères |
| `fleuves.kml` | Réseau hydrographique (format KML) |
| `fleuves_grandes.gpkg` | Grands fleuves |
| `fortresses.gpkg` | Sélection de forteresses mentionnées dans la thèse — liste non exhaustive |
| `frontière_sassanide.gpkg` | Frontière romano-sassanide |
| `frontière_arabe.gpkg` | Frontière romano-arabe |
| `grandes_villes.gpkg` | Grandes villes |
| `montagnes.gpkg` | Massifs montagneux |
| `points.gpkg` | Points divers |
| `régions.gpkg` | Délimitation des régions |

## Couches raster (`rasters/`)

Modèles numériques de terrain (MNT) utilisés pour générer la couche `montagnes.gpkg`. La vectorisation a été effectuée à partir d'un seuil de **1 500 m d'altitude**, avec des tranches de 500 m jusqu'à 4 500 m. Ces fichiers sont conservés pour permettre une éventuelle régénération de la couche avec des paramètres différents (seuil, emprise, résolution).

| Fichier | Résolution |
|---------|------------|
| `raster(0,05).tif` | 0,05° |
| `raster(0,1).tif` | 0,1° |
| `rater(0,02).tif` | 0,02° |
| `rater(0,2).tif` | 0,2° |

> Note : le préfixe `rater` dans deux fichiers est une coquille pour `raster`.

## Utilisation

Ouvrir le fichier `mediterranee-orientale-600-900.qgz` avec QGIS. Les chemins vers les couches sont relatifs — conserver la structure des dossiers telle quelle.
