# Awesome DuckDB Spatial   [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Long list of geospatial   analysis tools. Geospatial analysis, or just spatial analysis, is an approach to applying statistical analysis and other analytic techniques to data which has a geographical or spatial aspect.

![DuckDB_Spatial_Awesome](https://github.com/user-attachments/assets/ae9c1db3-fea1-4ff2-a0d5-a5d99df98cf2)

## Official

* [DuckDB Spatial Extension (Docs)](https://duckdb.org/docs/stable/core_extensions/spatial/overview) - Official documentation for DuckDB’s spatial extension: `GEOMETRY` type, spatial functions, and reading/writing spatial formats.
* [duckdb/duckdb-spatial (GitHub)](https://github.com/duckdb/duckdb-spatial) - Source code for the DuckDB spatial extension (functions, types, GDAL/PROJ integration, development notes).
* [PostGEESE? Introducing the DuckDB Spatial Extension (DuckDB Blog)](https://duckdb.org/2023/04/28/spatial.html) - Official announcement post introducing DuckDB Spatial, design goals, and key capabilities.
* [Spatial Joins in DuckDB (DuckDB Blog)](https://duckdb.org/2025/05/23/spatial-joins.html) - Official deep dive into spatial join performance and the `SPATIAL_JOIN` operator.

## Extensions

* [isaacbrodsky/h3-duckdb](https://github.com/isaacbrodsky/h3-duckdb) - DuckDB community extension for Uber’s H3 hex indexing: convert lat/lng ↔ cells, neighborhood queries, and aggregation workflows.
* [paleolimbot/duckdb-geography](https://github.com/paleolimbot/duckdb-geography) - Community “GEOGRAPHY” extension using S2 Geometry for spherical/geodesic calculations (experimental, separate from the core spatial extension).

## Tutorials & Guides

* [Getting Started with Modern GIS using DuckDB (MotherDuck)](https://motherduck.com/blog/modern-gis-duckdb/) - End-to-end tutorial: load spatial data, run spatial SQL, and visualize results with a practical example.
* [A Beginner’s Guide to Geospatial with DuckDB Spatial and MotherDuck (Simon Späti)](https://motherduck.com/blog/beginners-guide-to-geospatial-with-duckdb-spatial-and-motherduck/) - Beginner-friendly walkthrough of installing DuckDB Spatial and running common GIS tasks.
* [DuckDB: The Indispensable Geospatial Tool You Didn’t Know You Were Missing (Chris Holmes)](https://cloudnativegeo.org/blog/2023/05/duckdb-geospatial-tool-you-didnt-know/) - Narrative guide showing why DuckDB is a strong fit for large, file-based geospatial analytics.
* [DuckDB for Geospatial (Geography & Coding)](https://geographycoding.com/duckdb-for-geospatial/) - Practical article with examples and performance discussion for large datasets.

## Performance, Indexing, and Optimization

* [Spatial Queries in DuckDB with R-tree and H3 Indexing (Architecture & Performance)](https://architecture-performance.fr/ap_blog/spatial-queries-in-duckdb-with-r-tree-and-h3-indexing/) - Hands-on performance exploration and an approach to fast spatial filtering via H3 indexing patterns.
* [Using DuckDB’s Hilbert Function with GeoParquet (Cloud Native Geospatial Forum)](https://forum.cloudnativegeo.org/t/using-duckdbs-hilbert-function-with-geoparquet/207) - Discussion and examples of ordering spatial data via Hilbert curves to improve locality and query performance.

## Raster & Imagery (Experimental / In-Progress)

* [Managing Raster Data in DuckDB with the Spatial Extension (Part I) (Medium)](https://medium.com/@antoniohuar/duckdb-spatial-extension-for-raster-data-part-i-af3ddf9f0d59) - Proposal + proof-of-concept notes for raster support via GDAL inside DuckDB workflows.
* [Managing Raster Data in DuckDB with the Spatial Extension (Part II) (Medium)](https://medium.com/@antoniohuar/duckdb-spatial-extension-for-raster-data-part-ii-aec2e3bfc12c) - STAC + raster processing experiments demonstrating a potential end-to-end imagery workflow.

## R / Python Ecosystem Integrations

* [duckspatial (CRAN)](https://cran.r-project.org/package=duckspatial) - R package bridging DuckDB Spatial with the `sf` ecosystem for efficient GIS operations in R.
* [GeoPandas + DuckDB workflows (Example Article)](https://www.usdsi.org/blog/2026/01/12/exploring-geographic-data-efficiently-with-geopandas-and-duckdb/) - Practical patterns: push heavy filtering/aggregation to DuckDB, then use GeoPandas for geometry-heavy operations and visualization.

## Books

* [Spatial Data Management with DuckDB (Qiusheng Wu)](https://duckdb.gishub.org) - Book + companion materials covering spatial SQL, formats, performance, and real-world geospatial analytics in DuckDB.
* [Spatial Data Management with DuckDB (Leanpub)](https://leanpub.com/spatial-data-management-with-duckdb) - Book distribution page (often includes updates and downloadable formats).

## Talks & Videos

* [DuckDB Spatial: Supercharged Geospatial SQL! (GeoPython 2024)](https://www.youtube.com/watch?v=zscJP1Yo7qk) - Talk introducing DuckDB Spatial capabilities, typical workflows, and demos.
* [Is DuckDB the Secret to Unlocking Your GIS Potential? (MotherDuck)](https://www.youtube.com/watch?v=9uZ8GbnU4Lw) - Video tutorial for beginners: install spatial extension and run common GIS queries.

## Community, Forums, and Discussions

* [DuckDB Spatial Extension Discussions (GitHub)](https://github.com/duckdb/duckdb-spatial/discussions) - Q&A, ideas, and community problem-solving around DuckDB Spatial.
* [Cloud Native Geospatial Forum (DuckDB tag)](https://forum.cloudnativegeo.org/tag/duckdb) - Community discussions on GeoParquet, optimization, formats, and DuckDB spatial patterns.

## Non-English

### Spanish

* [Gestión de Datos Espaciales con DuckDB (Leanpub)](https://leanpub.com/gestion-de-datos-espaciales-con-duckdb) - Spanish-language learning resource/book on DuckDB Spatial.

