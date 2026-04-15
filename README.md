# Assignment 4: Clustering, Web Search, and PageRank

**Name:** Chirag Phor  
**Roll Number:** M25DE1021  

## Overview
This repository contains the completion of Assignment 4, which spans three core topics in large-scale data algorithms:
1. **Part 1 - Clustering**: Implementations of Farthest First Traversal (k-center) and k-means++ probability-weighted initialization methods, measured against the UCI Spam dataset (`spambase.data`).
2. **Part 2 - Web Search**: An Object-Oriented simulation of an Inverted Index search engine built entirely from scratch in python. Includes robust stop-word filtering, boolean multi-query operations, and TF-IDF relevance scoring mimicking `queryFindPagesWhichContainWord` queries on the provided StackExchange dummy dataset.
3. **Part 3 - PageRank on Spark**: A network link-analysis script written with PySpark RDDs intended to track interconnected node probability masses modeling distributed internet traffic iteratively.

## Project Structure
- `solution.ipynb`: The main execution Jupyter Notebook containing all three implemented parts divided systematically.
- `Assignment 4- datasets/`: Contains the datasets required for clustering (UCI Spam base) and text webpages required for the Web Search inverted index evaluations. 
- (Note: Place `small.txt` and `whole.txt` into the root directory prior to executing the `PageRank` Spark cells as they are dynamically referenced.)

## Prerequisites
To run the Jupyter Notebook correctly, please ensure standard python data science libraries are installed alongside PySpark:
```bash
pip install numpy pyspark notebook
```

## Running the Notebook
Open the notebook via the terminal relative to the project root:
```bash
jupyter notebook solution.ipynb
```
Follow the linear execution trail. The cells will individually trigger:
- `Step 1 to 3` objective comparisons on the UCI Spam Matrix.
- A sequential simulated run mapping against `actions.txt` to print identical matching webpages.
- An iterative PageRank computation mapped out precisely over 40 iterations.

*(Note: PageRank outputs execution statements and retains the structure. Remove commenting blocks to operate directly when `small.txt` is present).*
