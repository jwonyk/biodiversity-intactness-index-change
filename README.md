# Phoenix Subdivision Biodiversity Intactness Analysis

### Biodiversity Intactness Index (BII) Change, 2017–2020

## About This Repository

This repository contains the analysis for a project examining changes in the Biodiversity Intactness Index (BII) in the Phoenix subdivision of Maricopa County, AZ, from 2017 to 2020. Using 100 m BII data, the project explores how rapid urban growth may be affecting local biodiversity. The analysis focuses on:

-   Extracting and clipping BII rasters for 2017 and 2020 to the Phoenix subdivision boundary.
-   Calculating the percentage of the subdivision area with BII ≥ 0.75 for both years.
-   Mapping areas that lost high BII values (≥ 0.75) between 2017 and 2020.
-   Situating the Phoenix subdivision within its broader geographic and urban context using additional vector/raster data and basemaps.

The goal is to provide an accessible, reproducible workflow for assessing biodiversity change in a rapidly developing metropolitan region.

## Final Output

REPLACE HERE FOR OUTPUT

## Repository Structure

``` bash
biodiversity-intactness-index-change
├── README.md
├── biodiversity-intactness-index-change.ipynb
└── .gitignore
```

## Data Access

This project uses publicly available geospatial datasets accessed via the Microsoft Planetary Computer and the U.S. Census Bureau datasets stored locally in the repository's `data/` directory. Following is the local `data/` directory structure:

``` bash
├── data
│   ├── tl_2020_04_cousub
│   │   ├── tl_2020_04_cousub.cpg
│   │   ├── tl_2020_04_cousub.dbf
│   │   ├── tl_2020_04_cousub.prj
│   │   ├── tl_2020_04_cousub.shp
│   │   ├── tl_2020_04_cousub.shp.ea.iso.xml
│   │   └── tl_2020_04_cousub.shx
```

\#### Biodiversity Intactness Index (BII) Time Series

BII data are taken from the `io-biodiversity` collection on the [Microsoft Planetary Computer STAC Catalog](https://planetarycomputer.microsoft.com/dataset/io-biodiversity), which provides global 100 m BII projections for 2017–2020. For this project, the 2017 and 2020 rasters covering the Phoenix subdivision (bounding box: `[-112.826843, 32.974108, -111.184387, 33.863574]`) are loaded and then clipped to the Phoenix subdivision boundary to calculate metrics such as the percentage of area with BII ≥ 0.75.

#### Phoenix Subdivision Shapefile

The Phoenix subdivision boundary retrieved from the [Census County Subdivision TIGER/Line](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html) shapefiles for Arizona. This polygon defines the analysis area, is used to clip the BII rasters, and provides geographic context for mapping within Maricopa County and the surrounding region.

## Authorship

This repository was created for the course EDS 220 – Working with Environmental Datasets, UC Santa Barbara.

-   The project author: **Jay Kim**
-   Instructor: **Carmen Galaz García**
-   Co-Instructor: **Annie Adams**

## References

\[1\] F. Gassert, J. Mazzarello, and S. Hyde, *Global 100m Projections of Biodiversity Intactness for the Years 2017–2020*, Technical Whitepaper, Aug. 2022. Available: <https://ai4edatasetspublicassets.blob.core.windows.net/assets/pdfs/io-biodiversity/Biodiversity_Intactness_whitepaper.pdf>. \[Accessed: Dec. 1, 2025\]

\[2\] Z. Levitt and J. Eng, *Where America's developed areas are growing: 'Way off into the horizon'*, The Washington Post, Aug. 2021. Available: <https://www.washingtonpost.com/nation/interactive/2021/land-development-urban-growth-maps/>. \[Accessed: Dec. 1, 2025\]

\[3\] Microsoft Planetary Computer, *Biodiversity Intactness Index (BII) Time Series, io-biodiversity Collection*, 2017–2020 \[data file\]. Available from the Microsoft Planetary Computer STAC catalog. <https://planetarycomputer.microsoft.com/dataset/io-biodiversity>. \[Accessed: Dec. 1, 2025\]

\[4\] U.S. Census Bureau, *County Subdivision Shapefiles, Arizona (TIGER/Line)* \[data file\]. Available from the U.S. Census Bureau TIGER/Line shapefile download portal. <https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html>. \[Accessed: Dec. 1, 2025\]