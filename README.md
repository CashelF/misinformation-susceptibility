# Reddit Community Alignment and Misinformation Susceptibility

This notebook explores the analysis of community alignment and misinformation susceptibility in Reddit communities. It includes the steps to fetch subreddit submissions and comments, process them, and apply machine learning models to assess misinformation susceptibility based on news source credibility.

## Requirements

This notebook uses the following libraries:

- **torch**: For checking the availability of CUDA for GPU acceleration.
- **pandas**: For data manipulation.
- **networkx**: For creating and analyzing networks.
- **sentence-transformers**: For generating sentence embeddings.

## Notebook Overview

### 1. **Data Collection**
   - The notebook includes code to fetch Reddit data (submissions and comments) from various subreddits.
   - The data is used to analyze sentiment-based relationships among communities.

### 2. **Community Alignment Network**
   - A **community alignment network** is created to model sentiment-based relationships between Reddit subreddits.
   - Sentiment alignment is computed for each user's interaction with a subreddit using sentence embeddings and cosine similarity.

### 3. **Misinformation Susceptibility**
   - The notebook also computes **misinformation susceptibility scores** for each subreddit based on their links to credible or non-credible sources.

### 4. **Network Analysis**
   - The **credibility network** is constructed to model relationships between different news sources, assessing their credibility based on consistency and conflict in their coverage.

# Susceptibility to Misinformation Graph

This notebook explores the construction of a susceptibility to misinformation graph based on Reddit data and news source credibility. The goal is to analyze and visualize the relationship between subreddits and their susceptibility to misinformation, leveraging a community alignment network and credibility data from various news sources.

## Requirements

This notebook requires the following Python libraries:

- **pandas**: For data manipulation.
- **glob**: For loading files dynamically.
- **matplotlib**: For visualizing data (if used for plotting).

## Notebook Overview

### 1. **Data Collection**
   - The notebook loads data from multiple CSV files dynamically. These include:
     - Submissions and comments for various subreddits.
     - News source credibility data to assess the reliability of sources.

### 2. **Merging Data**
   - After collecting the data, it merges Reddit submissions with external news source credibility information. This helps assess the alignment between subreddit discussions and news source credibility.

### 3. **Building the Graph**
   - The notebook constructs a community alignment graph, which models relationships between Reddit subreddits based on shared users and sentiment.
   - The graph is used to calculate the misinformation susceptibility of each subreddit.

### 4. **Visualization**
   - The final graph can be visualized to see how different subreddits are aligned with news sources and each other in terms of their susceptibility to misinformation.
