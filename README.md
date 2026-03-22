# Chicago Homicides Analysis

Jupyter notebook analysis of the ICPSR 6399 dataset — _Homicides in Chicago, 1965–1995_ — covering gun crime trends, young male offender demographics, offender trait clustering, and an interactive neighborhood heatmap.

## Setup

```bash
# Create and activate virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook notebooks/analysis.ipynb
```

The first time Section 4 runs, it will fetch the Chicago community areas GeoJSON (~200 KB) and cache it to `data/chicago_community_areas.geojson`.

## Data

- `data/06399-0001-Data.por` — Part 1: victim-level records
- `data/06399-0002-Data.por` — Part 2: offender-level records
- `data/06399-0001-Codebook.pdf` — variable codebook for Part 1
- `data/06399-0002-Codebook.pdf` — variable codebook for Part 2

Source: Block, Carolyn Rebecca, Block, Richard L., and Illinois Criminal Justice Information Authority. _Homicides in Chicago, 1965–1995_. ICPSR 6399. https://doi.org/10.3886/ICPSR06399.v5

## Notebook Sections

| Section | Description                                                                        |
| ------- | ---------------------------------------------------------------------------------- |
| 1       | Gun crimes before vs. after July 1968 — bar chart and annual trend line            |
| 2       | Gun crimes by young male offenders (ages 15–40) — stacked bar by age category      |
| 3       | Offender trait analysis — frequency bars, co-occurrence heatmap, KMeans clustering |
| 4       | Chicago neighborhood heatmap — interactive folium choropleth by community area     |
