# One Rung Up: Nearest Neighbor

**Live page:** https://all-things-ava.github.io/nearest-neighbor/

The first data analysis and visualizations behind
[Bridging NYC: An Agentic Prototype for Navigating the Opportunity Landscape](https://all-things-ava.github.io/bridging-nyc/).

Inspired by Alex "Sandy" Pentland's *Shared Wisdom*, which argues that the most useful social bridges
connect a community to one that is one rung higher on the socioeconomic ladder, this analysis groups
New York City's 197 residential neighborhoods into four Opportunity Atlas mobility rungs and measures
how long it takes, by subway, to reach a neighborhood one rung higher.

## Repository contents

| Path | Contents |
|---|---|
| `index.html` | The project page (served by GitHub Pages) |
| `nearest-neighbor.ipynb` | The full analysis, from raw data to every figure |
| `data_raw/` | Input data, plus `results/all_analysis.csv` (the origin-destination dataset) |
| `figures/` | Charts and interactive maps produced by the notebook (Figures 1 to 9) |
| `findings/` | Figure 10, produced in a separate AI session (AI-generated) |

## Running the notebook

1. Install Python 3.11+ and the packages in `requirements.txt`:
   `pip install -r requirements.txt`
2. Get a free Census API key at https://api.census.gov/data/key_signup.html and set it as an
   environment variable before starting Jupyter:
   - macOS/Linux: `export CENSUS_API_KEY="your-key"`
   - Windows (PowerShell): `$env:CENSUS_API_KEY="your-key"`
3. Start Jupyter from this folder and run all cells. The notebook downloads the 2020 Neighborhood
   Tabulation Area boundaries and Census population counts, so it needs an internet connection.

Figures are written to `figures/`.

## Data sources

- Opportunity Atlas (Chetty et al., NBER Working Paper 25147, 2018), via Opportunity Insights
- HUD 2010 to 2020 Census Tract Crosswalk
- 2020 Decennial Census population (U.S. Census Bureau API)
- NYC Department of City Planning, 2020 Census Tracts to 2020 NTAs and CDTAs Equivalency, and 2020 NTA boundaries
- MTA New York City Transit subway GTFS feed

Full citations, transformations and equations are in the
[Bridging NYC Methods](https://all-things-ava.github.io/bridging-nyc/#methods) and
[Appendix](https://all-things-ava.github.io/bridging-nyc/#appendix).
