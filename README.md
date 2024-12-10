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
