# Assignment 4 Report: Clustering, Web Search, and PageRank

**Name:** Chirag Phor  
**Roll Number:** M25DE1021  
**GitHub Link:** https://github.com/cph0r/ass-4  

---

## Part 1: Clustering Analysis

### Methodology
In this section, `spambase.data` containing 4601 records mapped across 58-dimensional vectors is evaluated. Two distinctive clustering algorithms were fully mapped from scratch:
1. **Farthest First Traversal (`kcenter`)**: Selects an arbitrary initial point, iteratively selecting the successive center that maximizes the squared Euclidean distance from the set of currently existing centers.
2. **K-Means++ Initialization (`kmeansPP`)**: Enhances k-means by calculating distance probabilities. Data points further from established seeds have dramatically higher likelihoods of being initialized as successive centers. Evaluation is done using minimum aggregate objective squaring (`kmeansObj`).

### Evaluated Workflow
* **Step 1**: The `kcenter` algorithm traverses points efficiently, evaluating matrix distances in linear proportion to $O(|P| \times k)$ ensuring distinct distribution across extrema bounds.
* **Step 2**: Evaluated the K-means++ probability weighting against `k`.
* **Step 3**: Ran an advanced heuristic using `kcenter` to acquire $k_1$ centers ($k_1 > k$), filtering the raw space to dense approximations, and eventually running `kmeansPP` onto this core mapping to finalize down to $k$ centers resulting in efficient spatial representations.

---

## Part 2: Web Search and Inverted Index

### System Architecture
Modeled inherently on Object-Oriented principles translating typical Java-style assignments into native Python structures. The Inverted Index engine consists:
* **Position & WordEntry**: Records exact token appearances (word index locations) tied to distinct virtual Page objects (`PageEntry`).
* **InvertedPageIndex**: Houses the global generic `MyHashTable` binding filtered tokens to their corresponding occurrence frequencies ensuring extremely swift Boolean overlap searches generic to set principles (`MySet` unions/intersections).

### Search Processing & TF-IDF
1. **Filtration**: Strict lowercase coercions. Normal punctuation marks evaluate to splits, but edge cases such as `C++` gracefully interpret the `+` operand to answer technical queries accurately native to parsing stack webpage repositories. Single-to-plural mappings natively trim identical query tokens.
2. **Algorithm Validation**: Replicating sequences identically matching commands found mapped in `actions.txt`, filtering out words structurally aligned to basic stop-words (`is`, `the`, `that`, etc).
3. **Relevance Mapping**: Applied standard Log-based Inverse Document Frequencies tracking corpus scarcity against term frequency weights locally.

---

## Part 3: PySpark PageRank

### Distributed Iteration
Implemented applying Big Data resilience using PySpark Resilient Distributed Datasets (RDDs). 
1. The structural mapping removes inherently duplicated node links dynamically mapped into lists grouping outgoing connections (`groupByKey()`).
2. Iterative probabilistic mapping iterates precisely **40 times**, broadcasting decay ($\beta = 0.8$) against proportional inbound rankings. 
3. **Dangling Nodes Corrected**: An essential step ensures that disjoint nodes or endpoints with $0$ outgoing vertices remain natively injected to the total graph sequence utilizing a robust `LeftOuterJoin` avoiding sink-drop probability issues. Over repeated sequences, network density successfully funnels probabilities displaying exact Top and Bottom 5 probabilistic rank thresholds reflecting realistic structural integrities.
