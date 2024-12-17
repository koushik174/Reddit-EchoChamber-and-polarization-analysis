# Reddit-EchoChamber-and-polarization-analysis


## Overview
This project analyzes Reddit discussions to detect echo chambers, track opinion polarization, and visualize information flow patterns. It uses natural language processing and network analysis to understand how opinions form and spread within communities.

## Project Structure
```
reddit-polarization/
├── data/
│   └── reddit_analyzed_data.csv
├── notebooks/
│   ├── 1_data_processing.ipynb
│   ├── 2_topic_modeling.ipynb
│   ├── 3_cascade_detection.ipynb
│   └── 4_visualization.ipynb
├── results/
│   ├── cascade_analysis_results.pkl
│   └── network_visualization.png
└── requirements.txt
```

## Key Findings

### 1. Network Analysis
- Identified 1069 active subreddits with 100,280 interactions
- Average of 337.29 connections per subreddit
- High interconnectivity suggests active cross-community discussion

### 2. Echo Chamber Detection
- Discovered 11 potential echo chambers
- Key isolated communities include:
  - r/Advice
  - r/AirForce
  - r/AllThingsTerran
  - r/Animals
  - r/AnimeWallpaper
- These communities show low topic diversity (topic_diversity = 1)

### 3. Topic Analysis
Most active topics by spread:
1. Topic 1: 262 subreddits, 518 posts
2. Topic 6: 256 subreddits, 752 posts
3. Topic 4: 236 subreddits, 651 posts
4. Topic 8: 233 subreddits, 543 posts
5. Topic 5: 231 subreddits, 446 posts

## Installation

```bash
pip install -r requirements.txt
```

## Usage
1. Data Processing:
```python
python step1_data_processing.py
```

2. Topic Modeling:
```python
python step2_topic_modeling.py
```

3. Cascade Detection:
```python
python step3_cascade_detection.py
```

4. Visualization:
```python
python step4_visualization.py
```

## Requirements
- Python 3.8+
- pandas
- numpy
- networkx
- scikit-learn
- transformers
- plotly
- matplotlib
- seaborn

## Conclusions
1. Community Structure:
   - Reddit shows a highly interconnected network of communities
   - Most subreddits participate in multiple topic discussions
   - Few true echo chambers exist, suggesting healthy cross-pollination of ideas

2. Topic Distribution:
   - Topics spread widely across different communities
   - Most popular topics reach 200+ subreddits
   - High engagement rates across diverse communities

3. Echo Chamber Characteristics:
   - Identified echo chambers show very specific topic focus
   - Low sentiment variation within echo chambers
   - Smaller communities more likely to form echo chambers

## Future Work
- Temporal analysis of opinion evolution
- User behavior tracking across communities
- Integration with other social media platforms
- Real-time echo chamber detection


## Acknowledgments
- Reddit API
- Hugging Face Datasets
- NetworkX community
