# Awesome DuckDB Spatial   [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Long list of geospatial   analysis tools. Geospatial analysis, or just spatial analysis, is an approach to applying statistical analysis and other analytic techniques to data which has a geographical or spatial aspect.

![DuckDB_Spatial_Awesome](https://github.com/user-attachments/assets/ae9c1db3-fea1-4ff2-a0d5-a5d99df98cf2)

# Awesome DuckDB Geospatial

A curated list of resources related to **DuckDB’s geospatial capabilities** (the `spatial` extension and related ecosystem): docs, tutorials, benchmarks, repos, integrations, videos, and community discussions.

> DuckDB’s `spatial` extension brings PostGIS-like spatial SQL to an in-process OLAP engine, with built-in support for many vector formats via GDAL and a growing ecosystem of community extensions (e.g., H3).

---

## Contents

- [Official](#official)
- [Core docs: functions & I/O](#core-docs-functions--io)
- [Blog posts & articles](#blog-posts--articles)
- [Performance, indexing & optimization](#performance-indexing--optimization)
- [Interoperability (PostGIS, GDAL, tooling)](#interoperability-postgis-gdal-tooling)
- [Community extensions (H3, A5, etc.)](#community-extensions-h3-a5-etc)
- [Repositories & tools](#repositories--tools)
- [Web / WASM / Browser](#web--wasm--browser)
- [Servers & APIs](#servers--apis)
- [Books & courses](#books--courses)
- [Talks & videos](#talks--videos)
- [Community discussions](#community-discussions)
  
---

## Official

* [Spatial Extension — Overview (DuckDB Docs)](https://duckdb.org/docs/stable/core_extensions/spatial/overview.html) - Official overview, install/load instructions, and entry point to the spatial feature set.
* [PostGEESE? Introducing the DuckDB Spatial Extension (DuckDB Blog)](https://duckdb.org/2023/04/28/spatial.html) - Official announcement post introducing `GEOMETRY`, spatial SQL, reprojection, and format I/O.
* [Spatial Joins in DuckDB (DuckDB Blog)](https://duckdb.org/2025/08/08/spatial-joins.html) - Official deep dive into spatial join internals and performance (incl. `SPATIAL_JOIN` operator behavior).
* [duckdb/duckdb-spatial (GitHub)](https://github.com/duckdb/duckdb-spatial) - Source repository for DuckDB’s spatial extension (implementation, issues, PRs, discussions).
* [DuckDB Repositories (Docs)](https://duckdb.org/docs/stable/dev/repositories.html) - Official list of DuckDB project repositories (useful for contributors).

---

## Core docs: functions & I/O

* [Spatial Functions (DuckDB Docs)](https://duckdb.org/docs/stable/core_extensions/spatial/functions.html) - Complete function index, including constructors, predicates, transforms, and table functions.
* [GDAL Integration (DuckDB Docs)](https://duckdb.org/docs/stable/core_extensions/spatial/gdal.html) - How DuckDB bundles GDAL, supported drivers, and GDAL-based COPY/export behavior.
* [Extensions Overview (DuckDB Docs)](https://duckdb.org/docs/stable/extensions/overview.html) - General extension lifecycle (install/load/autoload) across DuckDB clients.

---

## Blog posts & articles

* [Getting started with modern GIS using DuckDB (MotherDuck)](https://motherduck.com/blog/getting-started-gis-duckdb/) - Practical intro to spatial concepts + DuckDB workflow (read/process/export).
* [Mastering Geospatial Analysis with DuckDB Spatial and MotherDuck (MotherDuck)](https://motherduck.com/blog/geospatial-for-beginner-duckdb-spatial-motherduck/) - Beginner-focused guide with hands-on queries and real datasets.
* [DuckDB: The Indispensable Geospatial Tool You Didn’t Know You Were Missing (CloudNativeGeo)](https://cloudnativegeo.org/blog/2023/09/duckdb-the-indispensable-geospatial-tool-you-didnt-know-you-were-missing/) - Why DuckDB is a great fit for file-native geospatial analytics (GeoParquet, large datasets).
* [DuckDB is Probably the Most Important Geospatial Software of the Last Decade (dbreunig.com)](https://www.dbreunig.com/2025/05/03/duckdb-is-the-most-impactful-geospatial-software-in-a-decade.html) - Opinionated overview of DuckDB’s impact on modern geospatial workflows.
* [DuckDB for Geospatial (geo.rocks)](https://geo.rocks/post/duckdb_geospatial) - Performance-oriented walkthrough (large points data, HTTPFS patterns).
* [Geospatial Analysis using DuckDB (Spatial Dev Guru)](https://spatial-dev.guru/2023/12/09/geospatial-analysis-using-duckdb) - Step-by-step tutorial using public datasets (points, transformations, queries).
* [Unlocking Cloud Data: Reading & Transforming Spatial Data with DuckDB (Philippe Massicotte)](https://www.pmassicotte.com/posts/2023-09-14-duckdb-parquet-spatial-s3) - Querying remote Parquet and building geometries with DuckDB Spatial.
* [Wrangling and Joining 130M Points with DuckDB + the Open Source Spatial Stack (Dewey Dunnington)](https://dewey.dunnington.ca/post/2024/wrangling-and-joining-130m-points-with-duckdb--the-open-source-spatial-stack) - Large-scale point workflows and join patterns with the broader spatial stack.
* [SedonaDB vs DuckDB vs PostGIS: Which Spatial SQL Engine is Fastest? (Matt Forrest)](https://forrest.nyc/sedonadb-vs-duckdb-vs-postgis-which-spatial-sql-engine-is-fastest) - Benchmark-style comparison for spatial analytics workloads.
* [Geospatial Analysis with Ibis and DuckDB (Redux) (Ibis Project)](https://ibis-project.org/posts/ibis-duckdb-geospatial-dev-guru) - Reproduces a DuckDB Spatial workflow via Ibis APIs.
* [Ibis + DuckDB Geospatial: A Match Made on Earth (Ibis Project)](https://ibis-project.org/posts/ibis-duckdb-geospatial) - Spatial analysis patterns using Ibis as a friendly layer over DuckDB.
* [More From The Duck Pond — Using DuckDB in ArcGIS Pro (Esri Community)](https://community.esri.com/t5/etl-patterns-blog/more-from-the-duck-pond-using-duckdb-in-arcgis-pro/ba-p/1373643) - ETL patterns and GIS tooling integration.
* [How to read OSM data with DuckDB (Medium)](https://medium.com/data-science/how-to-read-osm-data-with-duckdb-ffeb15197390) - Practical OSM/PBF ingestion concepts and data modeling.
* [Spatial Joins in DuckDB (DuckDB Blog)](https://duckdb.org/2025/05/23/spatial-joins.html) - Official deep dive into spatial join performance and the `SPATIAL_JOIN` operator.
* [Getting Started with Modern GIS using DuckDB (MotherDuck)](https://motherduck.com/blog/modern-gis-duckdb/) - End-to-end tutorial: load spatial data, run spatial SQL, and visualize results with a practical example.
* [A Beginner’s Guide to Geospatial with DuckDB Spatial and MotherDuck (Simon Späti)](https://motherduck.com/blog/beginners-guide-to-geospatial-with-duckdb-spatial-and-motherduck/) - Beginner-friendly walkthrough of installing DuckDB Spatial and running common GIS tasks.
* [DuckDB: The Indispensable Geospatial Tool You Didn’t Know You Were Missing (Chris Holmes)](https://cloudnativegeo.org/blog/2023/05/duckdb-geospatial-tool-you-didnt-know/) - Narrative guide showing why DuckDB is a strong fit for large, file-based geospatial analytics.
* [DuckDB for Geospatial (Geography & Coding)](https://geographycoding.com/duckdb-for-geospatial/) - Practical article with examples and performance discussion for large datasets.

---

## Performance, indexing & optimization

* [Spatial Queries in DuckDB with R-tree and H3 Indexing (Architecture & Performance)](https://architecture-performance.fr/ap_blog/spatial-queries-in-duckdb-with-r-tree-and-h3-indexing/) - Techniques for fast spatial filtering (H3 coarse indexing strategy).
* [Using DuckDB’s Hilbert Function with GeoParquet (CloudNativeGeo)](https://cloudnativegeo.org/blog/2025/01/using-duckdbs-hilbert-function-with-geoparquet) - Improving locality / filtering by spatial sorting before writing Parquet.
* [Efficient spatial join? (duckdb-spatial Discussion #303)](https://github.com/duckdb/duckdb-spatial/discussions/303) - Practical guidance and Q&A on point-in-polygon join patterns.

---

## Interoperability (PostGIS, GDAL, tooling)

* [Working with DuckDB (GDAL Docs)](https://gdal.org/en/stable/tutorials/vector_duckdb_tut.html) - Official GDAL tutorial covering DuckDB + extensions (spatial/parquet/httpfs/aws), and OGR usage patterns.
* [PostGIS meets DuckDB: Crunchy Bridge for Analytics goes Spatial (Crunchy Data)](https://www.crunchydata.com/blog/postgis-meets-duckdb-crunchy-bridge-for-analytics-goes-spatial) - Hybrid Postgres/PostGIS + DuckDB Spatial approach for fast analytics on external files.
* [Spatial Analytics (Crunchy Data Use Case)](https://www.crunchydata.com/use-cases/spatial-analytics) - Overview of delegating some PostGIS operations to DuckDB Spatial on GeoParquet.

---

## Community extensions (H3, A5, etc.)

* [DuckDB Community Extensions — Overview (Docs)](https://duckdb.org/docs/stable/extensions/community_extensions.html) - How community extensions work and how to install them.
* [DuckDB Community Extensions announcement (DuckDB Blog)](https://duckdb.org/2024/07/05/community-extensions.html) - Official intro to the community extension repository and workflow.
* [h3 — DuckDB Community Extension (Docs)](https://duckdb.org/community_extensions/extensions/h3.html) - Official community extension page for H3 hex indexing (install, functions, examples).
* [a5 — DuckDB Community Extension (Docs)](https://duckdb.org/community_extensions/extensions/a5.html) - Official community extension page for A5 DGGS / hierarchical indexing.

---

## Repositories & tools

* [tobilg/duckdb_featureserv (GitHub)](https://github.com/tobilg/duckdb_featureserv) - Lightweight geospatial feature server for DuckDB + duckdb-spatial (OGC API Features).
* [Query-farm/a5 (GitHub)](https://github.com/Query-farm/a5) - A5 geospatial indexing extension implementation (community extension).
* [isaacbrodsky/h3-duckdb (GitHub)](https://github.com/isaacbrodsky/h3-duckdb) - H3 extension repo implementing the H3 API in DuckDB.
* [davidgasquez/awesome-duckdb (GitHub)](https://github.com/davidgasquez/awesome-duckdb) - Broader Awesome list for DuckDB (often includes spatial-related ecosystem links).
* [paleolimbot/duckdb-geography](https://github.com/paleolimbot/duckdb-geography) - Community “GEOGRAPHY” extension using S2 Geometry for spherical/geodesic calculations (experimental, separate from the core spatial extension).

---

## Web / WASM / Browser

* [DuckDB Extensions, in DuckDB-Wasm! (DuckDB Blog)](https://duckdb.org/2023/12/18/duckdb-extensions-in-wasm.html) - Official post on extension support inside duckdb-wasm.
* [duckdb/duckdb-wasm-extensions-ci (GitHub)](https://github.com/duckdb/duckdb-wasm-extensions-ci) - CI + docs for WASM extensions (includes spatial-related internals/limitations notes).
* [A DuckDB-Wasm Web Mapping Experiment with Parquet (SparkGeo)](https://sparkgeo.com/blog/a-duckdb-wasm-web-mapping-experiment-with-parquet/) - Browser-based mapping experiment using DuckDB-Wasm over remote Parquet.
* [GeoParquet viewer with DuckDB spatial (Observable)](https://observablehq.com/@ericmauviere/geoparquet-viewer-with-duckdb-spatial) - Interactive notebook demonstrating GeoParquet/GeoJSON viewing with DuckDB spatial.
* [Honeycomb Maps](https://www.honeycombmaps.com) - An enterprise geospatial visualization platform that utilizes DuckDB-Wasm under-the-hood.

---

## Servers & APIs

* [duckdb_featureserv (GitHub)](https://github.com/tobilg/duckdb_featureserv) - OGC API Features server on top of DuckDB spatial (good base for WFS-like services).
* [tobilg/duckdb-tileserver](https://github.com/tobilg/duckdb-tileserver) - Lightweight **Mapbox Vector Tile (MVT) tileserver** for DuckDB + duckdb-spatial (Go), useful once your data lives in DuckDB tables/views.

---

## Books & courses

* [Spatial Data Management with DuckDB (Qiusheng Wu)](https://duckdb.gishub.org/) - Book + materials covering spatial SQL in DuckDB with examples.
* [giswqs/duckdb-spatial (GitHub)](https://github.com/giswqs/duckdb-spatial) - Companion code/examples for “Spatial Data Management with DuckDB”.

---

## Talks & videos

* [Is DuckDB the Secret to Unlocking Your GIS Potential? (YouTube)](https://www.youtube.com/watch?v=OuCY7_DzCTA) - Beginner-friendly walkthrough using DuckDB spatial + Python to build a heatmap.
* [Is DuckDB the Secret to Unlocking Your GIS Potential? (MotherDuck video page)](https://motherduck.com/videos/is-duckdb-the-secret-to-unlocking-your-gis-potential/) - Same video with MotherDuck context and related links.
* [The Journey of DuckDB Spatial Extension (YouTube)](https://www.youtube.com/watch?v=ZdcA4jViaaQ) - Interview-style video on the spatial extension’s roadmap and practical demos.
* [Geospatial Data Lakes! Maps from MotherDuck (duckdb) (YouTube)](https://www.youtube.com/watch?v=360BDapl4Hk) - Mapping-oriented talk/demo using MotherDuck/DuckDB for large-scale points.
* [Is DuckDB the Secret to Unlocking Your GIS Potential? (MotherDuck)](https://www.youtube.com/watch?v=9uZ8GbnU4Lw) - Video tutorial for beginners: install spatial extension and run common GIS queries.
* [DuckDB Spatial: Supercharged Geospatial SQL! (GeoPython 2024)](https://www.youtube.com/watch?v=zscJP1Yo7qk) - Talk introducing DuckDB Spatial capabilities, typical workflows, and demos.

---

## Community discussions

* [DuckDB Spatial Extension — Q&A / Discussions (GitHub)](https://github.com/duckdb/duckdb-spatial/discussions) - Main community forum for duckdb-spatial questions.
* [Issues — duckdb/duckdb-spatial (GitHub)](https://github.com/duckdb/duckdb-spatial/issues) - Bug reports and feature requests (useful to track roadmap topics).
* [Extensions (spatial extension) with DuckDB (Observable Forum)](https://talk.observablehq.com/t/extensions-spatial-extension-with-duckdb/8712) - Notes/issues using DuckDB spatial from Observable environments.
* [DuckDB’s Spatial Extension (Reddit thread)](https://www.reddit.com/r/dataengineering/comments/12g942e/duckdbs_spatial_extension/) - Community feedback and use cases.

---

## Libraries & Frameworks

### Python

* [kraina-ai/quackosm](https://github.com/kraina-ai/quackosm) - Read **OpenStreetMap PBF** with DuckDB, extract/filter, and produce analytics-friendly outputs (GeoParquet workflows).
* [ajl2718/whereabouts](https://github.com/ajl2718/whereabouts) - Fast local geocoding in Python that uses DuckDB as its query engine (no external geocoding API required).
* [duckdb-extension-spatial (PyPI)](https://pypi.org/project/duckdb-extension-spatial/) - Helper package for installing/loading the DuckDB spatial extension from Python environments.

### R

* [cidree/duckspatial](https://github.com/Cidree/duckspatial) - R package bridging `{sf}` with DuckDB spatial for memory-efficient vector analytics on large data.

### “SQL-first” / DataFrame APIs

* [Ibis + DuckDB geospatial (redux)](https://ibis-project.org/posts/ibis-duckdb-geospatial-dev-guru) - Geospatial workflows using Ibis with DuckDB as the backend (expressions → SQL).
* [From query to plot: Exploring GeoParquet Overture Maps with Ibis + DuckDB](https://ibis-project.org/posts/ibis-overturemaps/) - End-to-end example including visualization.

---

## Visualization & GIS Integration

* [developmentseed/lonboard](https://github.com/developmentseed/lonboard) - GPU-accelerated interactive vector viz in Jupyter and Python.
* [Lonboard docs: DuckDB Spatial](https://developmentseed.org/lonboard/latest/ecosystem/duckdb/) - Pass DuckDB queries directly into visualizations / layers.
* [QDuckDB (QGIS provider plugin docs)](https://oslandia.gitlab.io/qgis/qduckdb/) - QGIS data provider plugin for reading DuckDB databases as map layers.
* [QDuckDB source (GitLab)](https://gitlab.com/Oslandia/qgis/qduckdb) - Plugin repository.
* [QDuckDB on QGIS Plugin Repo](https://plugins.qgis.org/plugins/qduckdb/) - Install via QGIS plugin manager.
* [Kepler.gl](https://kepler.gl/) - Open-source geospatial analytics tool; includes DuckDB-Wasm-based workflows for client-side filtering/aggregation (varies by deployment).
* [duckdblabs/duckgl](https://github.com/duckdblabs/duckgl) - Geospatial visualization for DuckDB using deck.gl and MapLibre (experimental).

---
