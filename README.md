# 🪸 Attractor vs Producer: Artificial Reef Fish Assemblages 🐠
**Zenodo Release Wrapper Repository**

## Overview 

This repository is a **release wrapper** that archives the full analytical workflow for the *Attractor vs Producer* project led by **Global Reef**, investigating whether newly deployed shipwreck artificial reefs in the Gulf of Thailand function primarily as **fish attractors** or **fish producers**.

This wrapper pins and links two complementary analysis repositories as git submodules:

- **AR-producer**: tests production mechanisms (recruitment, size structure, life-stage signals)  
- **AR-attractor**: tests attraction mechanisms (redistribution, diversity, assemblage structure)

The wrapper exists to provide a **single, citable, reproducible Zenodo release** that captures the exact versions of both analytical components used for inference.

---

## 📁 Repository structure 

```
AR-producer-attractor-release/
├── AR-producer/        # git submodule (production-focused analyses)
├── AR-attractor/       # git submodule (attraction-focused analyses)
├── README.md           # this file
├── CITATION.cff        # citation metadata for Zenodo
└── LICENSE
``` 

Each submodule is pinned to a specific commit or tag at the time of release.

---

## Scientific context

Artificial reefs can increase local fish abundance through two non-exclusive mechanisms:

1. **Attraction** – concentration or redistribution of existing fish from surrounding natural reefs  
2. **Production** – generation of new biomass via recruitment, growth, or long-term persistence  

This project explicitly separates and evaluates these mechanisms using repeated underwater fish surveys conducted around shipwreck deployments near **Koh Tao, Thailand**, under the Global Reef research programme.

---

## Submodule overview

---

### AR-attractor  
**Focus:** attraction signals  

- Timed Swim surveys for fish abundance
- Abundance and diversity patterns  
- Functional group responses  
- Paired wreck–reef comparisons  
- Multivariate ordination (NMDS, Bray–Curtis)  

Repository: https://github.com/global-reef/AR-attractor

---

### AR-producer  
**Focus:** production signals  

- Size-structured abundance models  
- Juvenile vs adult (life-stage) responses  
- Functional group and species-level GLMMs  
- Tests for recruitment and biomass generation  

Repository: https://github.com/global-reef/AR-producer

---

## Reproducing the analyses

### Clone the wrapper repository (including submodules)

```
git clone --recurse-submodules https://github.com/global-reef/AR-producer-attractor-release.git
cd AR-producer-attractor-release

```

---

## ✨ Run analyses
Each submodule is a self-contained R project and should be run independently.

### AR-producer
Open AR-producer/AR_Producer.Rproj in RStudio
Run 00_RUN.R to assemble cleaned datasets
Execute scripts 01_* through 07_* sequentially
Figures, tables, and model outputs are written to the outputs/ directory

### AR-attractor
Open AR-attractor/AR_Attractor.Rproj in RStudio
Run 01.CLEAN.R to assemble cleaned datasets
Execute scripts 02.* through 06.* sequentially
Figures, tables, and model outputs are written to the outputs/ directory
Refer to the individual README files within each submodule for detailed dependencies and script descriptions.


Notes
-----

- Survey data are collected by Global Reef researchers based in Koh Tao, Thailand.
- Fieldwork and data processing are ongoing; results may be updated as more surveys are completed.
- This project contributes to understanding the ecological role shipwrecks 

License
-------

This project is private and not licensed for redistribution. For collaboration inquiries, please contact scarlett@global-reef.com.

**Affiliation:** [Global Reef](https://global-reef.com), Koh Tao, Thailand  



