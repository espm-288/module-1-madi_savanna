<<<<<<< HEAD
# ⚓ Module 1: Tabular Data - A Pirate's Tale 🏴‍☠️

Working with larger-than-RAM data using duckdbfs

## 🗺️ Ahoy, Me Hearties! (Overview)

Avast ye! This here treasure map demonstrates high-performance workflows fer wranglin' tabular data usin' DuckDB and duckdbfs, arr! We be handlin' datasets larger than the hold of the Black Pearl through streamin' and remote file access capabilities, savvy? ⛵

## 🌊 Case Study: Global Supply Chains o' the Seven Seas

This module be usin' [EXIOBASE 3.8.1](https://source.coop/youssef-harby/exiobase-3), a mighty global Multi-Regional Input-Output (MRIO) database that tracks economic transactions between sectors and regions, along with their environmental plunder! 💰

### 🏝️ Treasure Details (Dataset Details)
- **Coverage**: 44 countries + 5 rest-of-world regions across the seven seas! 🌍
- **Timeframe**: 1995–2022 (many a year o' plunderin'!) ⏰
- **Content**: Economic transactions (Z matrix), final demand (Y matrix), and environmental stressors (F matrix) - all the booty ye need! 📊
- **Format**: Cloud-optimized Parquet, partitioned by year and matrix type (organized like a proper ship's cargo!) 📦

## 🎓 What Ye'll Learn on This Voyage (Learning Objectives)

- Connect to remote datasets without downloadin' - like sendin' yer spyglass across the seas! 🔭
- Filter data efficiently before loadin' into R - only take the treasure ye need! 💎
- Query large tabular datasets using dplyr syntax - navigate the data like a seasoned sailor! 🧭
- Analyze economic and environmental data from EXIOBASE - understand the bounty and the cost! ⚖️

## 📜 Ye Olde Files

- `tabular-data.qmd` - Main Quarto scroll with exercises and analysis, arr! 🗞️

## ⚔️ Required Tools fer the Voyage (Requirements)

- R 4.0+ (A proper captain's toolkit! ⚓)
- duckdbfs package (Yer trusty compass! 🧭)
- dplyr package (Yer sword fer data wranglin'! ⚔️)

```r
library(duckdbfs)  # Yer trusty compass! 🧭
library(dplyr)     # Yer sword fer data wranglin'! ⚔️
```

## 🚢 Settin' Sail - Gettin' Started

Open `tabular-data.qmd` in RStudio or Quarto and render the document to see the analysis and exercises, ye scurvy dog! 🦜

Shiver me timbers and may the wind be at yer back! 🌬️

## 🏴‍☠️ Captain o' This Ship

ESPM 288 - Module 1 ⚓👑


(mic check) hello world, its brunjo 
ahoy! I redeemed ye file
=======
# Module 1: Tabular Data

This project demonstrates high-performance workflows for working with large tabular datasets in R, using the `duckdbfs` package and the EXIOBASE 3.8.1 global MRIO database.

## Overview
- **Goal:** Work with datasets larger than available RAM using DuckDB's streaming and remote file access.
- **Case Study:** EXIOBASE 3.8.1, a global Multi-Regional Input-Output (MRIO) database tracking economic transactions and environmental impacts.
- **Data Format:** Cloud-optimized Parquet, partitioned by year and matrix type, hosted remotely.

## Key Features
- Connect to remote S3-hosted datasets without downloading.
- Efficiently filter and query large datasets using `dplyr` and `duckdbfs`.
- Analyze economic and environmental data at scale.

## How to Use
1. **Install dependencies:**
	- R packages: `duckdbfs`, `dplyr`
2. **Connect to the dataset:**
	- Use `open_dataset()` with the provided S3 URL.
3. **Explore and filter data:**
	- Use `glimpse()` to view schema.
	- Filter before collecting data into R for efficiency.

## Example Code
```r
library(duckdbfs)
library(dplyr)

# Set up S3 connection (credentials may not be needed for public data)
duckdbfs::duckdb_secrets(
	 key = "",
	 secret = "",
	 endpoint = "s3.amazonaws.com",
	 region = "us-west-2"
)
s3_url <- "s3://us-west-2.opendata.source.coop/youssef-harby/exiobase-3/4588235/parquet/**"
exio <- open_dataset(s3_url)
glimpse(exio)

# Filter for US data in 2022 and preview
exio |>
	 filter(year == 2022, region == "US") |>
	 head() |>
	 collect()
```

## Exercises
- Connect to the EXIOBASE dataset and explore its schema.
- Filter for specific years, regions, or sectors.
- Query for top sectors by CO2 emissions or other environmental flows.

## References
- [EXIOBASE 3.8.1](https://source.coop/youssef-harby/exiobase-3)
- [duckdbfs documentation](https://github.com/duckdblabs/duckdbfs)
>>>>>>> 56e5cd0 (Update README with project details and usage instructions)
