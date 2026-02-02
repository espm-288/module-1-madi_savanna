# ⚓ Module 1: Tabular Data - A Pirate's Tale 🏴‍☠️

## 🗺️ Ahoy, Me Hearties!

Avast ye! This here treasure map demonstrates high-performance workflows fer wranglin' tabular data usin' DuckDB and duckdbfs, arr! We be handlin' datasets larger than the hold of the Black Pearl through streamin' and remote file access capabilities, savvy? ⛵

## 🌊 Case Study: Global Supply Chains o' the Seven Seas

This module be usin' [EXIOBASE 3.8.1](https://source.coop/youssef-harby/exiobase-3), a mighty global Multi-Regional Input-Output (MRIO) database that tracks economic transactions between sectors and regions, along with their environmental plunder! 💰

### 🏝️ Treasure Details
- **Coverage**: 44 countries + 5 rest-of-world regions across the seven seas! 🌍
- **Timeframe**: 1995–2022 (many a year o' plunderin'!) ⏰
- **Content**: Economic transactions (Z matrix), final demand (Y matrix), and environmental stressors (F matrix) - all the booty ye need! 📊
- **Format**: Cloud-optimized Parquet, partitioned by year and matrix type (organized like a proper ship's cargo!) 📦

## 📜 Ye Olde Files

- `tabular-data.qmd` - Main Quarto scroll with exercises and analysis, arr! 🗞️

## ⚔️ Required Tools fer the Voyage

```r
library(duckdbfs)  # Yer trusty compass! 🧭
library(dplyr)     # Yer sword fer data wranglin'! ⚔️
```

## 🚢 Settin' Sail - Gettin' Started

Open `tabular-data.qmd` in RStudio or Quarto and render the document to see the analysis and exercises, ye scurvy dog! 🦜

Shiver me timbers and may the wind be at yer back! 🌬️

## 🏴‍☠️ Captain o' This Ship

ESPM 288 - Module 1 ⚓👑
