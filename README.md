# Module 1: Tabular Data

Working with larger-than-RAM data using duckdbfs

## Overview

This module explores high-performance workflows for tabular data analysis. We use `duckdbfs` to work with datasets larger than available RAM by leveraging DuckDB's streaming and remote file access capabilities.

## Case Study: Global Supply Chains

We analyze [EXIOBASE 3.8.1](https://source.coop/youssef-harby/exiobase-3), a global Multi-Regional Input-Output (MRIO) database that tracks economic transactions between sectors and regions, along with their environmental impacts.

**Dataset Details:**
- **Coverage**: 44 countries + 5 rest-of-world regions
- **Timeframe**: 1995–2022
- **Content**: Economic transactions (Z matrix), final demand (Y matrix), and environmental stressors (F matrix)
- **Format**: Cloud-optimized Parquet, partitioned by year and matrix type

## Learning Objectives

- Connect to remote datasets without downloading
- Filter data efficiently before loading into R
- Query large tabular datasets using dplyr syntax
- Analyze economic and environmental data from EXIOBASE

## Getting Started

See `tabular-data.qmd` for the module content and exercises.

## Requirements

- R 4.0+
- duckdbfs package
- dplyr package
