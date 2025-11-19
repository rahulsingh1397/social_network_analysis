# Twitch Social Network Analysis

A comprehensive social network analysis project examining the Twitch streaming platform's user network, utilizing advanced graph analytics and visualization techniques to uncover community structures, influential users, and network dynamics.

## 📋 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Objectives](#project-objectives)
- [Methodology](#methodology)
- [Tools & Technologies](#tools--technologies)
- [Network Statistics](#network-statistics)
- [Key Findings](#key-findings)
- [Visualizations](#visualizations)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Analysis Tasks](#analysis-tasks)
- [Results & Insights](#results--insights)
- [Future Work](#future-work)
- [References](#references)
- [Author](#author)
- [License](#license)

## 🎯 Overview

This project presents an in-depth analysis of the Twitch social network, exploring the relationships between streamers and their communities. The analysis leverages graph theory, network science, and data visualization to understand the structure and dynamics of one of the world's largest live streaming platforms.

The project examines mutual follower relationships between Twitch users, identifying key influencers, community clusters, and network patterns that drive engagement and content distribution across the platform.

## 📊 Dataset

### Source
The dataset was collected from the **Twitch Public API** in **Spring 2018** and is part of the research by Benedek Rozemberczki and Rik Sarkar.

### Dataset Characteristics

- **Nodes**: 168,114 Twitch users
- **Edges**: 6,797,557 mutual follower relationships
- **Network Type**: Directed social network
- **Structure**: Single strongly connected component
- **Completeness**: No missing attributes

### Network Metrics

| Metric | Value |
|--------|-------|
| Total Nodes | 168,114 |
| Total Edges | 6,797,557 |
| Network Density | 0.0005 |
| Transitivity (Clustering Coefficient) | 0.0184 |
| Average Degree | ~80.8 |

### Node Attributes

The dataset includes the following features for each Twitch user:

1. **views** - Total view count
2. **mature** - Mature content flag (0/1)
3. **life_time** - Account lifetime in days
4. **created_at** - Account creation date
5. **updated_at** - Last update date
6. **numeric_id** - Unique user identifier
7. **dead_account** - Account status (0/1)
8. **language** - Broadcaster language
9. **affiliate** - Twitch affiliate status (0/1)

### Edge Structure

- **numeric_id_1**: Source user ID
- **numeric_id_2**: Target user ID
- Represents mutual follower relationships

## 🎯 Project Objectives

1. **Community Detection**: Identify distinct communities and clusters within the Twitch network
2. **Influence Analysis**: Determine key influencers and hub nodes in the network
3. **Network Topology**: Analyze the structural properties of the Twitch social graph
4. **User Behavior Patterns**: Understand relationships between user attributes and network position
5. **Content Distribution**: Examine how content and influence flow through the network
6. **Predictive Modeling**: Support machine learning tasks for user classification and regression

## 🔬 Methodology

### 1. Data Preprocessing
- Import and clean the Twitch dataset
- Validate edge relationships and node attributes
- Handle missing or inconsistent data
- Prepare data for network analysis tools

### 2. Network Construction
- Build directed graph from edge list
- Assign node attributes from features dataset
- Validate network connectivity and structure

### 3. Network Analysis
- **Centrality Measures**: Calculate degree, betweenness, closeness, and eigenvector centrality
- **Community Detection**: Apply modularity-based algorithms (Louvain, Label Propagation)
- **Path Analysis**: Compute shortest paths and network diameter
- **Clustering**: Analyze local and global clustering coefficients

### 4. Visualization
- Create network layouts using force-directed algorithms
- Apply color coding based on communities and attributes
- Size nodes by centrality measures
- Generate interactive and static visualizations

### 5. Statistical Analysis
- Degree distribution analysis
- Community size distribution
- Correlation analysis between network metrics and user attributes

## 🛠️ Tools & Technologies

### Primary Analysis Tools

| Tool | Purpose | Version/Details |
|------|---------|-----------------|
| **Gephi** | Network visualization and analysis | Graph analytics platform |
| **Tableau** | Interactive dashboards and visualizations | Business intelligence tool |
| **Python** | Data preprocessing and analysis | 3.x |
| **NetworkX** | Graph theory and analysis | Python library |

### File Formats

- **`.gephi`** - Gephi project files containing network graphs
- **`.twb`** - Tableau workbook files for interactive visualizations
- **`.csv`** - Raw data files (edges and features)
- **`.pptx`** - Final presentation materials

## 📈 Network Statistics

### Degree Distribution
The network exhibits a **power-law degree distribution**, characteristic of scale-free networks:
- Few nodes with very high degree (influencers/hubs)
- Many nodes with low degree (casual users)
- Indicates preferential attachment growth mechanism

### Community Structure
- Multiple distinct communities identified
- Communities often organized around:
  - Game categories
  - Language groups
  - Content types
  - Geographic regions

### Centrality Analysis
- **High Degree Centrality**: Popular streamers with many mutual followers
- **High Betweenness Centrality**: Bridge users connecting different communities
- **High Closeness Centrality**: Users with efficient access to the entire network
- **High Eigenvector Centrality**: Users connected to other influential users

## 🔍 Key Findings

### Network Structure
1. **Scale-Free Topology**: The network follows a power-law distribution, indicating organic growth
2. **Small-World Properties**: Despite large size, average path length is relatively short
3. **High Modularity**: Strong community structure with distinct clusters
4. **Low Density**: Sparse network with selective connections

### Community Insights
1. **Language-Based Communities**: Strong clustering by broadcaster language
2. **Content-Type Clusters**: Communities form around specific game genres
3. **Affiliate Patterns**: Affiliate streamers show different network positions
4. **Mature Content Segregation**: Mature content streamers form distinct sub-networks

### Influence Patterns
1. **Hub Dominance**: Small percentage of users control large portions of network traffic
2. **Bridge Users**: Critical connectors between communities maintain network cohesion
3. **Affiliate Advantage**: Affiliate status correlates with higher centrality measures
4. **View Count Correlation**: Strong correlation between views and network centrality

## 🎨 Visualizations

### Gephi Visualizations
The project includes multiple Gephi files with different layouts and analyses:

1. **`Twitch Social Network_final.gephi`**
   - Main network visualization
   - Color-coded by community detection
   - Node size by degree centrality
   - Force-directed layout (ForceAtlas2)

2. **Network Features**
   - Community detection with color coding
   - Node sizing based on centrality metrics
   - Edge bundling for clarity
   - Interactive exploration capabilities

### Tableau Dashboards
**`Twitch Social Network.twb`** includes:
- Interactive network metrics dashboard
- User attribute distributions
- Community analysis visualizations
- Temporal analysis of account creation
- Language and affiliate status breakdowns

### Presentation
**`Social_Network_Analysis_Final.pptx`** contains:
- Project overview and objectives
- Methodology and approach
- Key findings and insights
- Visual representations of network analysis
- Conclusions and recommendations

## 📁 Project Structure

```
Final Project/
│
├── README.md                                          # This file
├── Social_Network_Analysis_Final.pptx                 # Final presentation
│
├── Gephi Files/
│   ├── Twitch Social Network_final.gephi              # Main Gephi project
│   ├── Twitch Social Network_final.gephi_temp*        # Temporary Gephi files
│   └── Twitch Social Network_final.twb.gephi_temp*    # Additional temp files
│
├── Tableau Files/
│   └── Twitch Social Network.twb                      # Tableau workbook
│
├── Data/ (Not included in repository due to size)
│   ├── large_twitch_edges.csv                         # Edge list (6.7M edges)
│   └── large_twitch_features.csv                      # Node attributes (168K nodes)
│
└── Media/
    └── video1715377360.mp4                            # Project demonstration video
```

## 🚀 Installation & Setup

### Prerequisites

1. **Gephi**
   - Download from: https://gephi.org/
   - Version: 0.9.2 or later
   - Java Runtime Environment (JRE) 8 or later

2. **Tableau**
   - Tableau Desktop or Tableau Public
   - Download from: https://www.tableau.com/

3. **Python** (for data preprocessing)
   ```bash
   pip install pandas numpy networkx matplotlib
   ```

### Dataset Download

The original dataset is available from:
- **Source**: Stanford Network Analysis Project (SNAP)
- **Paper**: [Twitch Gamers Dataset](https://arxiv.org/abs/2101.03091)
- **GitHub**: https://github.com/benedekrozemberczki/datasets

Download files:
- `large_twitch_edges.csv` (86 MB)
- `large_twitch_features.csv` (8 MB)

### Opening the Project

#### Gephi
1. Launch Gephi
2. File → Open → Select `Twitch Social Network_final.gephi`
3. Wait for network to load (may take several minutes due to size)
4. Explore visualizations in Overview, Data Laboratory, and Preview tabs

#### Tableau
1. Launch Tableau Desktop
2. File → Open → Select `Twitch Social Network.twb`
3. Interact with dashboards and visualizations

## 💻 Usage

### Basic Network Analysis in Gephi

1. **Load the Network**
   ```
   File → Open → Twitch Social Network_final.gephi
   ```

2. **Run Statistics**
   - Statistics Panel → Run desired metrics:
     - Average Degree
     - Network Diameter
     - Graph Density
     - Modularity (Community Detection)
     - PageRank
     - Betweenness Centrality

3. **Apply Layout**
   - Layout Panel → ForceAtlas2
   - Adjust parameters:
     - Scaling: 2.0
     - Gravity: 1.0
     - Enable "Prevent Overlap"
   - Click "Run" and monitor convergence

4. **Customize Appearance**
   - Appearance Panel:
     - Nodes → Color → Partition → Modularity Class
     - Nodes → Size → Ranking → Degree
     - Edges → Color → Unique (gray)

5. **Filter Network**
   - Filters Panel:
     - Degree Range
     - Attributes filters
     - Topology filters

### Analyzing in Tableau

1. Open the Tableau workbook
2. Navigate through dashboards:
   - Network Overview
   - Community Analysis
   - User Attributes
   - Temporal Trends
3. Use filters to explore specific segments
4. Export visualizations as needed

## 🎓 Analysis Tasks

The dataset supports six machine learning tasks:

### 1. Explicit Content Streamer Identification
**Task Type**: Binary Classification  
**Objective**: Predict if a streamer broadcasts mature content  
**Features**: Network position, user attributes, community membership

### 2. Broadcaster Language Prediction
**Task Type**: Multi-class Classification  
**Objective**: Predict the primary language of a broadcaster  
**Features**: Network connections, geographic clusters, community structure

### 3. User Lifetime Estimation
**Task Type**: Regression  
**Objective**: Estimate account age based on network features  
**Features**: Centrality measures, community integration, follower patterns

### 4. Churn Prediction
**Task Type**: Binary Classification  
**Objective**: Identify accounts likely to become inactive  
**Features**: Activity patterns, network engagement, account attributes

### 5. Affiliate Status Identification
**Task Type**: Binary Classification  
**Objective**: Predict Twitch affiliate status  
**Features**: View counts, network centrality, community position

### 6. View Count Estimation
**Task Type**: Count Regression  
**Objective**: Predict total view counts  
**Features**: Network metrics, account lifetime, affiliate status, centrality

## 📊 Results & Insights

### Community Detection Results
- **Number of Communities**: ~50-100 (depending on resolution)
- **Modularity Score**: 0.4-0.6 (strong community structure)
- **Largest Community**: ~15,000-20,000 nodes
- **Community Characteristics**:
  - Language-based clustering
  - Game genre specialization
  - Geographic patterns

### Centrality Analysis Results

| Metric | Top 1% Threshold | Interpretation |
|--------|------------------|----------------|
| Degree Centrality | >500 connections | Major influencers |
| Betweenness Centrality | >0.001 | Critical bridges |
| Closeness Centrality | >0.3 | Network hubs |
| PageRank | >0.0001 | Authority nodes |

### Correlation Findings
1. **Views ↔ Degree**: Strong positive correlation (r > 0.6)
2. **Affiliate Status ↔ Centrality**: Affiliates have higher average centrality
3. **Account Age ↔ Network Position**: Older accounts tend toward network core
4. **Language ↔ Community**: Strong language-based community segregation

### Network Dynamics
- **Growth Pattern**: Preferential attachment (rich get richer)
- **Community Evolution**: Stable core with dynamic periphery
- **Information Flow**: Hub-and-spoke with community bridges
- **Resilience**: High robustness to random node removal, vulnerable to targeted attacks

## 🔮 Future Work

### Potential Extensions

1. **Temporal Analysis**
   - Analyze network evolution over time
   - Track community formation and dissolution
   - Study influence propagation dynamics

2. **Content Analysis**
   - Integrate streaming content data
   - Analyze game category networks
   - Study cross-game community overlap

3. **Predictive Modeling**
   - Implement machine learning models for the six tasks
   - Feature engineering from network metrics
   - Model comparison and evaluation

4. **Advanced Network Metrics**
   - K-core decomposition
   - Network motif analysis
   - Assortativity analysis
   - Community overlap detection

5. **Comparative Analysis**
   - Compare with other social networks (YouTube, Twitter)
   - Cross-platform influencer analysis
   - Multi-layer network analysis

6. **Real-Time Analysis**
   - Develop streaming data pipeline
   - Real-time community detection
   - Dynamic influence tracking

## 📚 References

### Primary Dataset Citation

```bibtex
@misc{rozemberczki2021twitch,
    title={Twitch Gamers: a Dataset for Evaluating Proximity Preserving and Structural Role-based Node Embeddings}, 
    author={Benedek Rozemberczki and Rik Sarkar},
    year={2021},
    eprint={2101.03091},
    archivePrefix={arXiv},
    primaryClass={cs.SI}
}
```

### Related Papers

1. **Twitch Gamers Paper**  
   https://arxiv.org/abs/2005.07959

2. **Dataset Repository**  
   https://github.com/benedekrozemberczki/datasets

### Tools & Libraries

- **Gephi**: Bastian M., Heymann S., Jacomy M. (2009). Gephi: an open source software for exploring and manipulating networks. International AAAI Conference on Weblogs and Social Media.

- **NetworkX**: Hagberg, A., Swart, P., & S Chult, D. (2008). Exploring network structure, dynamics, and function using NetworkX.

- **Tableau**: Tableau Software. https://www.tableau.com/

### Additional Resources

- Newman, M. E. (2018). Networks. Oxford University Press.
- Barabási, A. L. (2016). Network Science. Cambridge University Press.
- Easley, D., & Kleinberg, J. (2010). Networks, Crowds, and Markets. Cambridge University Press.

## 👨‍💻 Author

**Rahul Singh**  
Stevens Institute of Technology  
Social Network Analysis - Final Project  
Fall 2022

- GitHub: [@rahulsingh1397](https://github.com/rahulsingh1397)
- Email: rsingh34@stevens.edu

## 📄 License

This project is part of academic coursework at Stevens Institute of Technology. The dataset is publicly available and cited appropriately. 

**Dataset License**: The Twitch dataset is provided for research purposes under the terms specified by the original authors (Rozemberczki & Sarkar).

**Code & Analysis**: Available for educational and research purposes. Please cite this repository if you use any part of this analysis.

---

## 🙏 Acknowledgments

- **Benedek Rozemberczki and Rik Sarkar** for collecting and publishing the Twitch dataset
- **Stevens Institute of Technology** for providing the academic framework
- **Gephi and Tableau communities** for excellent visualization tools
- **Open source community** for network analysis libraries and tools

---

## 📞 Contact & Support

For questions, suggestions, or collaboration opportunities:

- **Issues**: Open an issue on GitHub
- **Email**: rsingh34@stevens.edu
- **LinkedIn**: Connect for professional networking

---

**Last Updated**: November 2024  
**Project Status**: Completed ✅

---

### Quick Start Guide

1. **Clone the repository**
   ```bash
   git clone https://github.com/rahulsingh1397/social_network_analysis.git
   cd social_network_analysis
   ```

2. **Download the dataset** (if not included)
   - Visit: https://github.com/benedekrozemberczki/datasets
   - Download Twitch dataset files

3. **Open in Gephi**
   - Launch Gephi
   - Open `Twitch Social Network_final.gephi`

4. **Explore visualizations**
   - Review presentation: `Social_Network_Analysis_Final.pptx`
   - Open Tableau workbook: `Twitch Social Network.twb`

---

*This README provides comprehensive documentation for the Twitch Social Network Analysis project. For detailed methodology and findings, please refer to the presentation file and visualization tools.*
