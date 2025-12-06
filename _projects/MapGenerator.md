---
layout: page
title: MapGenerator
description: 🗺️ France population map makers
full_name: mpek29/MapGenerator
img: assets/img/projects/MapGenerator/main.png
importance: 1
git: https://github.com/mpek29/MapGenerator
github: https://github.com/mpek29/MapGenerator
category: Electronics
subcategory: Signal and Image Processing
---




**Main Project Goal**

The main objective of this project is to localize a small number of major cities in France (7–9), chosen so that they are few enough to be easily memorized. The idea is to divide France into 7–9 areas, each dominated by one of these key cities, with the goal that each area contains roughly the same amount of population and wealth. This approach aims to split and rebalance the country's population and economic activity, which is currently too concentrated in Paris, by promoting a more even distribution across the territory.

**MapGenerator** is a professional Python tool to generate and export a map of France showing population densities by municipality (commune), using official INSEE and administrative boundaries data.

## Features

- Reads French municipality boundaries (JSON) and population data (Excel)
- Handles Paris as a single commune by aggregating arrondissement data if needed
- Computes population density (inhabitants/km²) for each municipality
- Classifies density into 5 custom bins: 0–15, 15–30, 30–50, 50–100, 100+ hab/km²
- Visualizes the map with a professional 5-level red color scale
- Exports the map as a high-resolution PNG with a timestamped filename

## Requirements


Install dependencies with:

```bash
pip install -r requirements.txt
```


## Example Output


Below is an example of the generated map:

| Population Density Map | Population density threshold map | Repartition map |
|--------------|---------------|-------|
| <img src="france_density_map.png"> | <img src="france_density_threshold_map.png"> | <img src="france_repartition_map.png"> |

## Usage


1. Download the following datasets and place them in the project root:
	- `communes.json` (GeoJSON of French municipalities, e.g. from [data.gouv.fr](https://www.data.gouv.fr/fr/datasets/contours-des-communes-de-france/))
	- `POPULATION_MUNICIPALE_COMMUNES_FRANCE.xlsx` (INSEE population by commune, e.g. from [insee.fr](https://www.insee.fr/fr/statistiques/6011076))

2. Run the main script:

```bash
python main.py
```

The map will be displayed and automatically exported as a PNG file (e.g. `france_density_map_YYYYMMDD_HHMMSS.png`).

## Project Structure


- `main.py` — Minimal entry point
- `map_generator.py` — All core logic, modular and PEP-8 compliant
- `requirements.txt` — Python dependencies

## Customization


- You can adjust the density bins or color palette in `map_generator.py`.
- The export filename is timestamped for easy versioning.

