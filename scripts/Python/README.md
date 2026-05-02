# `scripts/Python/` — Python Auxiliary Scripts

Auxiliary Python pipeline. Use for: web scraping, text/PDF extraction from Chinese policy documents, geocoding, raster/GIS preprocessing, anything outside the Stata/R sweet spot.

## Naming convention

Numbered, lower-case, snake_case:

```
01_scrape_policy_text.py
02_extract_county_codes.py
03_geocode_villages.py
```

## Environment

Use a project-local `venv` or `conda env` and pin dependencies in `requirements.txt` or `environment.yml` (track in git, not the env itself).

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Outputs

- `_outputs/` (gitignored): intermediate JSON, parquet, scraped HTML.
- Cleaned outputs land in `data/raw/` (if treated as a new data source) or `data/processed/` (if derived from existing raw).

## Header template

```python
"""
Script: 0X_name.py
Purpose: [one-line]
Inputs: ...
Outputs: ...
Author: [name]
Created: YYYY-MM-DD
"""
```
