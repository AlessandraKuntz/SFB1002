# SFB1002 Publication Analysis

**Charting Collaboration and Impact: A Data Analysis of SFB1002's Research Output**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org)
[![NetworkX](https://img.shields.io/badge/NetworkX-Network%20Analysis-red)](https://networkx.org)

A comprehensive analysis of collaborative research publication data from the SFB1002 research consortium, implemented as a Jupyter notebook for research data management and strategic insight generation.

## 📋 Overview

This project analyzes 550+ publication records from SFB1002 (2014-2024) to understand collaboration patterns, productivity trends, and research impact. The analysis demonstrates research data management best practices while generating actionable insights for academic collaboration enhancement.

**Analysis Results:**
- ✅ 498 publications analyzed (2014-2024)
- 🏢 37 working groups identified  
- 👥 2,359 unique authors catalogued
- 🤝 45.4% collaboration rate
- 📊 60+ visualizations and reports generated

## 🚀 Quick Start

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn plotly networkx openpyxl
```

### Usage
1. **Clone or download** this repository
2. **Prepare your data**: Place your Excel file in the same directory as the notebook
3. **Update file path**: In the notebook, change:
   ```python
   file_path = "2025-07-01_excel_export.xlsx"  # Change to your filename
   ```
4. **Run the notebook**: Execute all cells in `DS_M5_SFB1002_Kuntz.ipynb`
5. **View results**: Check the generated `SFB1002_Analysis` folder on your Desktop

## 📊 Data Requirements

Your Excel file should contain these core columns:

| Column | Description | Example |
|--------|-------------|---------|
| `Working Groups` | Research group identifiers | "ag_group1, ag_group2" |
| `Publication Year` | Year of publication | 2020 |
| `Authors` | Author names (comma-separated) | "Smith J, Doe A, Johnson B" |
| `Journal` | Publication venue | "Nature Medicine" |
| `Open Access` | Access status | "Yes" or "No" |
| `Publication Type` | Type of publication | "Journal Article" |
| `DOI` | Digital Object Identifier | "10.1038/..." |
| `Subproject` | Subproject codes | "A01, B02" |

**Note:** The notebook handles missing data gracefully and includes data cleaning protocols.

## 📁 Generated Outputs

The analysis creates a comprehensive folder structure on your Desktop:

```
~/Desktop/SFB1002_Analysis/
├── 01_cleaned_data/              # 5 processed datasets
│   ├── main_dataset.csv          # Core publication data (498 rows)
│   ├── individual_groups.csv     # Group-separated records (984 rows)
│   ├── collaboration_dataset.csv # Multi-group publications (226 rows)
│   ├── author_dataset.csv        # Author-level records (5,011 rows)
│   └── external_resources.csv    # Additional metadata
├── 02_visualizations/            # Charts and graphs
│   ├── static/                   # PNG publication-ready charts
│   ├── interactive/              # HTML interactive dashboards
│   └── networks/                 # Collaboration network diagrams
├── 03_reports/                   # Executive summaries
│   └── executive_summary.html    # Main strategic report
├── 04_statistics/                # Statistical summaries
├── 05_temporal_analysis/         # Time-based trends
├── 06_collaboration_metrics/     # Network analysis results
├── 07_productivity_analysis/     # Performance metrics
├── 08_impact_analysis/           # Publication impact assessment
└── 09_strategic_insights/        # Strategic recommendations
```

## 🎯 Key Features

### Data Processing & Quality
- **Automated cleaning** with error handling and validation
- **Multi-perspective datasets** for different analytical needs
- **Standardized formats** ensuring data consistency
- **Missing data handling** with appropriate defaults

### Analysis Capabilities
- **Collaboration Networks** using NetworkX for partnership mapping
- **Temporal Trends** showing evolution of research output
- **Productivity Metrics** for individual and group performance
- **Impact Assessment** of publication quality and visibility

### Visualizations
- **Static Charts** (15+) - Publication-ready PNG files
- **Interactive Dashboards** - Plotly-based HTML visualizations
- **Network Diagrams** - Collaboration mapping with centrality metrics
- **Executive Reports** - Comprehensive HTML summaries

## 📈 Example Insights Generated

The analysis provides insights such as:

- **Collaboration Patterns**: Which groups collaborate most frequently
- **Productivity Trends**: Publication output over time by group
- **Network Analysis**: Key connector groups and collaboration hubs
- **Strategic Opportunities**: Underutilized collaboration potential
- **Impact Metrics**: Open access rates and journal diversity
- **Author Networks**: Prolific researchers and influence patterns

## 🔧 Customization

### Modifying Analysis Parameters

```python
# Change time period filter
df = df[(df['Publication_Year'] >= 2015) & (df['Publication_Year'] <= 2023)]

# Adjust collaboration threshold
prolific_authors = author_counts[author_counts >= 5].index  # Change from 3 to 5

# Modify network layout
pos = nx.spring_layout(G, k=5, iterations=100)  # Adjust layout parameters
```

### Adding Custom Analysis

The notebook is modular - you can add custom analysis functions:

```python
def custom_analysis(self):
    """Add your custom analysis here"""
    # Your analysis code
    pass

# Add to the main analysis pipeline
analyzer.custom_analysis()
```

## 🛠️ Technical Details

### Main Components
- **`SFB1002Analyzer` class** - Core analysis engine
- **Data cleaning methods** - Systematic data preparation
- **Network analysis functions** - Collaboration mapping
- **Visualization generators** - Chart and report creation
- **Strategic insight derivation** - Recommendation algorithms

### Dependencies
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
import plotly.graph_objects as go
import networkx as nx
from collections import Counter, defaultdict
```

### Performance
- **Runtime**: ~5-10 minutes for complete analysis
- **Memory**: Requires ~500MB RAM for full dataset
- **Output size**: ~50MB of generated files

## 🎓 Educational Context

This project demonstrates research data management (RDM) principles:

- **FAIR Data Principles**: Findable, Accessible, Interoperable, Reusable outputs
- **Data Stewardship**: Quality assurance and documentation protocols  
- **Reproducible Research**: Clear methodology and reusable code
- **Strategic Intelligence**: Data-driven insights for decision making

## 🤝 Contributing

To adapt this analysis for your own data:

1. **Modify data requirements** in the cleaning section
2. **Adjust analysis parameters** for your research context
3. **Customize visualizations** for your specific needs
4. **Extend strategic insights** based on your objectives

## 📄 File Structure

```
sfb1002-analysis/
├── DS_M5_SFB1002_Kuntz.ipynb    # Main analysis notebook
├── README.md                     # This file
├── requirements.txt              # Python dependencies
└── sample_data/                  # Example data structure (optional)
```

## 🚨 Troubleshooting

**Common Issues:**

1. **"File not found"** - Ensure your Excel file is in the same directory as the notebook
2. **Missing dependencies** - Run `pip install -r requirements.txt`
3. **Memory errors** - For very large datasets, consider filtering data before analysis
4. **Visualization errors** - Ensure you have the latest versions of plotly and matplotlib

**Getting Help:**
- Check the error messages in the notebook output
- Verify your data format matches the expected structure
- Ensure all required columns are present in your Excel file

## 📧 Contact

**Project**: SFB1002 Publication Analysis  
**Created**: July 2025  
**Purpose**: Research Data Management Certificate Project  

For questions about implementation or methodology, please refer to the notebook documentation and comments.

---