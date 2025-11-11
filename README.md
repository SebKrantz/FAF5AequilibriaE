# FAF5 Network Analysis with AequilibraE

This project demonstrates comprehensive transportation network analysis using the FAF5 (Freight Analysis Framework 5) network data and the AequilibraE transportation modeling framework.

## Overview

The FAF5 network is a comprehensive freight transportation network covering the United States, containing detailed highway network data including links, nodes, and various transportation attributes. This project provides tools and workflows to:

1. Load FAF5 network data from Geodatabase format
2. Create an AequilibraE project and import the network
3. Calculate shortest travel times/costs between origin-destination (OD) pairs
4. Compute shortest paths between OD pairs with detailed path information
5. Generate route choice sets between OD pairs using BFS-LE algorithm
6. Perform traffic assignment using path-sized logit method

## Interactive Maps

The analysis generates interactive maps visualizing the network analysis results:

### Shortest Paths Map
[View Shortest Paths Map](https://html-preview.github.io/?url=https://github.com/CPCS-IAU/FAF5/blob/master/shortest_paths_map.html)

### Route Choice Sets Map
[View Route Choice Sets Map](https://html-preview.github.io/?url=https://github.com/CPCS-IAU/FAF5/blob/master/route_choice_sets_map.html)

## Features

- **Network Loading**: Import FAF5 network from Geodatabase format (487,394 links and 974,788 nodes)
- **Path Computation**: Calculate shortest paths between OD pairs with detailed link-by-link information
- **Route Choice Analysis**: Generate route choice sets using Breadth-First Search with Link Elimination (BFS-LE) algorithm
- **Traffic Assignment**: Perform static traffic assignment using path-sized logit route choice model
- **Visualization**: Generate interactive Folium maps for exploring network paths and route choices

## Installation

### Prerequisites

- Python 3.9 or higher
- GDAL/GEOS libraries (required for GeoPandas)

### Setup

1. Clone the repository:
```bash
git clone https://github.com/CPCS-IAU/FAF5.git
cd FAF5
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

The project requires:
- `numpy>=1.20.0`
- `pandas>=1.3.0`
- `aequilibrae>=1.0.0`
- `geopandas>=0.12.0`
- `fiona>=1.9.0`
- `shapely>=2.0.0`
- `jupyter>=1.0.0`
- `ipykernel>=6.0.0`

## Usage

The main analysis is performed in the Jupyter notebook `FAF5_AequilibraE_Analysis.ipynb`. Open the notebook and run the cells sequentially to:

1. Load the FAF5 network data
2. Create and configure the AequilibraE project
3. Perform network analysis operations
4. Generate visualization maps

### Network Data

The FAF5 network data should be located in:
```
Networks/Geodatabase Format/FAF5Network.gdb
```

The network data dictionary is available in `Networks/FAF5 Network Data Dictionary.pdf`.

## Project Structure

```
FAF5/
├── FAF5_AequilibraE_Analysis.ipynb   # Main analysis notebook
├── requirements.txt                  # Python dependencies
├── Networks/                         # FAF5 network data
│   ├── Geodatabase Format/
├── shortest_paths_map.html          # Interactive shortest paths map
├── route_choice_sets_map.html       # Interactive route choice sets map
└── README.md                        # This file
```

## Analysis Workflow

1. **Network Loading**: Import FAF5 links and nodes from Geodatabase
2. **Project Creation**: Initialize AequilibraE project and import network
3. **Graph Preparation**: Build network graph with travel time/cost attributes
4. **Path Computation**: Calculate shortest paths for selected OD pairs
5. **Route Choice Sets**: Generate alternative routes using BFS-LE algorithm
6. **Traffic Assignment**: Assign traffic flows using path-sized logit model
7. **Visualization**: Create interactive maps showing paths and assignments

## References

- [AequilibraE Documentation](https://aequilibrae.com/)
- FAF5 Network Data Dictionary (included in `Networks/` directory)

## License

[Add your license information here]

## Contributing

[Add contribution guidelines if applicable]

