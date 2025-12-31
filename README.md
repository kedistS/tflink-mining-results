# TFLink Neural Subgraph Pattern Mining Results

## Overview

This repository contains pattern mining results from the human transcriptional regulatory network (TFLink database). Neural subgraph mining identified **503 hierarchical regulatory architectures** involving 374 genes (0.48% of the network).

## Dataset

- **Source**: [TFLink database](https://tflink.net)
- **Network size**: 78,686 genes, 6.4M regulatory relationships
- **Patterns found**: 503 instances across 18 topological classes (size 3-8, rank 1-3)

## Key Results

- **503 hierarchical patterns** detected
- **AGPAT5** (lipid metabolism): 238 appearances (47%)
- **IMPACT** (translation control): 168 appearances (33%)
- **99 diverse transcription factors** use the same hierarchical architecture
- **Convergent regulation**: 108 genes receive multi-input control

## Code

Pattern mining was performed using [SPMiner](https://github.com/rejuve-bio/neural-subgraph-matcher-miner) with the following configuration:

```bash
# Random walk sampling: 10,000 trials
# Neighborhood size: 20-29 genes
# Exploration radius: 3 steps
# Coverage: ~96% of network genes
```

## Repository Structure

```
tflink_10000_5000/
├── results/
│   └── out-patterns_all_instances.pkl    # NetworkX graphs of all patterns
├── cluster/
│   ├── size_3_rank_1/                     # Pattern visualizations
│   ├── size_4_rank_1/
│   └── ...
└── README.md
```
