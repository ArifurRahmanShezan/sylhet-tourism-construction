# Tourism, new construction and hazard exposure in the Sylhet tourism belt, Bangladesh

Code and validation data for the article *"Co-location rather than causation: tourism, new construction and hazard exposure in the Sylhet tourism belt, Bangladesh"*.

## Contents

| File | What it is |
|---|---|
| `Sylhet_analysis_notebook.ipynb` | The complete analysis in Google Colab: Part A (Stages 0–8, main analysis) and Part B (revision analyses: label validation, time-matched OpenStreetMap, attribution and prediction, COVID-19 test, hazard exposure, robustness). Outputs from the authors' runs are kept under each cell. |
| `data/manual_check_points.csv` | The 100 stratified points used for the manual validation of the construction labels |
| `data/manual_answers.csv` | The interpreter's answers (real new building yes/no) for those points |
| `results/` | Result tables (CSV) written by the notebook |
| `maps/` | Output GeoTIFFs (2035 construction probability, ecological sensitivity classes, planning zones), if included |

The notebook's first cells contain a table that links every notebook cell to the tables and figures of the paper and its Supplementary Material.

## How to run

1. Open `Sylhet_analysis_notebook.ipynb` in Google Colab (*File → Upload notebook*).
2. Put the input data in your Google Drive (see the "How to run" section in the notebook and Supplementary Table S1 of the paper). All inputs are open data. The World Database on Protected Areas cannot be redistributed and must be downloaded from https://www.protectedplanet.net.
3. Run the cells in order. Each cell saves its results to `MyDrive/Sylhet_outputs`, so you can stop and continue in a new session.
4. Cells 1B, 2D and M2 use Google Earth Engine: replace `'YOUR-GEE-PROJECT'` with your own Earth Engine project ID.

## Requirements

Google Colab (High-RAM runtime; a T4 GPU only for Stage 4), Google Drive and a Google Earth Engine Cloud project. Python packages missing from Colab are installed by Stage 0. Random seeds are fixed (`SEED = 42`).

## Data sources

Google Open Buildings 2.5D Temporal; Landsat 8/9 Collection 2; Sentinel-1 and Sentinel-2 (Copernicus); Dynamic World; VIIRS night-time lights; WorldPop R2025A; Copernicus DEM GLO-30; MERIT Hydro; JRC Global Surface Water; Global Forest Change; CHIRPS; OpenStreetMap (Geofabrik extracts of 1 January 2016, 2020 and 2023, and 26 October 2026); World Database on Protected Areas; administrative boundaries from HDX. Full citations are in the paper.

## License

Code: MIT License (see `LICENSE`). Please cite the article and the data providers when reusing this code.
