# MTL-TSFLO: LLM-Driven Territorial Spatial Function Layout Optimization

**A Territorial Spatial Optimization Method Integrating Large Language Models with Multisource Geospatial Data-Trained Multilayer Perceptron and Transformer Models**

---

  

## Overview

  

This repository provides the implementation of the **LLM-driven Territorial Spatial Function Layout Optimization (MTL-TSFLO)** framework.

  

Unlike conventional optimization methods that require manually designed transition matrices and handcrafted mathematical models, MTL-TSFLO automatically converts planning requirements expressed in natural language into optimization objectives and constraints through Large Language Models (LLMs), and subsequently generates an optimized territorial spatial function layout.

  

To simplify reproduction and demonstration, this repository provides the optimization module only.

  

The Spatial Distribution Suitability (SDS) and Spatial Expansion Suitability (SES) used by the optimization model are provided as input data and are assumed to have been generated beforehand.

  

---


## Workflow

  

The workflow implemented in this repository is:

  

```
Natural-language planning requirements

                │

                ▼

      LLM semantic understanding

                │

                ▼

Automatic construction of optimization

 objectives and constraints

                │

                ▼

Optimization solver

                │

                ▼

Optimized territorial spatial function map

```

  

The SDS and SES maps are treated as known inputs rather than being generated within this repository.

---

  

## Repository Structure

  

```
.

├── data/

│   ├── MLP_Scores_5Bands/

│   ├── Trans_Scores_5Bands/

│   ├── func_shuangliu/

│   ├── yj_shuangliu/

│   ├── st_shuangliu/

│   ├── cz_shuangliu/

│   └── Demo/

│

├── prompts/

│

├── optimization/

│

├── outputs/

│

├── requirements.txt

│

└── README.md

```

  

---

## Input Data

  

The optimization model requires the following raster inputs.

  

| Input               | Description |

|-------              |-------------|

| MLP_Scores_5Bands   | Spatial Distribution Suitability |

| Trans_Scores_5Bands | Spatial Expansion Suitability |

|func_shuangliu       | Existing territorial spatial function map |

| yj_shuangliu        | Permanent Basic Farmland |

| st_shuangliu        | Ecological Protection Redline |

| cz_shuangliu        | Urban Development Boundary |

  

All rasters should have identical projection, extent, resolution, and raster dimensions.

  

---

  

## Output

  

The optimization produces:

- Optimized territorial spatial function map

- Optimization statistics

- Constraint satisfaction report




---

## Installation

  

Python 3.11 is recommended.

  

Install dependencies by

  

```bash
pip install -r requirements.txt

```

  ![[Pasted image 20260715215158.png]]

---

  

## Running the Demo

  

Run

  

```bash
python demo3.ipynb

```

  

The optimized layout will be generated

  

---

  

## Notes

  

This repository demonstrates only the LLM-driven optimization component of the proposed framework.

  

The MLP_Scores_5Bands and Trans_Scores_5Bands maps are provided as input data for demonstration purposes and are not generated within this repository.

  

The complete datasets used in the manuscript are not included.

  

---

## License

  

MIT License

  

---
