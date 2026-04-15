# Assignment 4: Clustering, Web Search, and PageRank

## Total Marks: 120

---

# Part 1: Clustering (40 Marks)

## Objective

Study and implement:

* Farthest First Traversal (k-center clustering)
* k-means++ algorithm

## Dataset

* UCI Spam Dataset
* 4601 data points
* 58-dimensional feature vectors
* Each point represents an email

---

## Functions to Implement

### 1. `readVectorsSeq(filename)`

* Input: text file with comma-separated features
* Output: list of vectors

---

### 2. `kcenter(P, k)`

* Implements **Farthest-First Traversal**
* Input: dataset `P`, integer `k`
* Output: `k` centers
* Time complexity: **O(|P| × k)**

---

### 3. `kmeansPP(P, k)`

* Implements **k-means++ initialization**
* Input: dataset `P`, integer `k`
* Output: `k` centers
* Time complexity: **O(|P| × k)**

---

### 4. `kmeansObj(P, C)`

* Computes:

  * Average squared distance of each point to nearest center
* Output:

  ```
  (1 / |P|) * Σ distance²(point, closest center)
  ```

---

## Main Program Flow

Input:

* Dataset `P`
* Integers `k` and `k1` where `k < k1`

Steps:

### Step 1

* Run `kcenter(P, k)`
* Print execution time

---

### Step 2

* Run `kmeansPP(P, k)` → centers `C`
* Compute `kmeansObj(P, C)`
* Print result

---

### Step 3

* Run `kcenter(P, k1)` → centers `X`
* Run `kmeansPP(X, k)` → centers `C`
* Compute `kmeansObj(P, C)`
* Print result

---

## Submission Requirements

* Code in **Jupyter Notebook**
* Push to **GitHub**
* Include GitHub link in report
* Submit report as:

```
<roll_number>_CSL7110_Assignment4.pdf
```

---

# Part 2: Web Search (40 Marks)

## Objective

Build a **Search Engine using Inverted Index + TF-IDF**

---

## Key Concepts

### Inverted Index

Maps:

```
word → list of (page, position)
```

---

### TF-IDF

#### Term Frequency (TF)

```
tf(w, p) = occurrences of w in p / total words in p
```

#### Inverse Document Frequency (IDF)

```
idf(w) = log(N / number of pages containing w)
```

#### Relevance

```
score = tf × idf
```

---

## Classes to Implement

### 1. `MySet`

* `addElement()`
* `union()`
* `intersection()`

---

### 2. `Position`

* Stores:

  * Page
  * Word index

---

### 3. `WordEntry`

* Stores positions of a word
* Methods:

  * `addPosition()`
  * `getTermFrequency()`

---

### 4. `PageIndex`

* Stores all word entries of a page

---

### 5. `PageEntry`

* Reads webpage file
* Builds index

---

### 6. `MyHashTable`

* Maps word → WordEntry

---

### 7. `InvertedPageIndex`

* Stores all pages
* Methods:

  * `addPage()`
  * `getPagesWhichContainWord()`

---

### 8. `SearchEngine`

* Handles queries
* Main method:

  * `performAction()`

---

## Supported Actions

### 1. Add Page

```
addPage x
```

---

### 2. Search Word

```
queryFindPagesWhichContainWord x
```

---

### 3. Word Positions

```
queryFindPositionsOfWordInAPage x y
```

---

## Preprocessing Rules

* Convert to lowercase
* Remove stop words:

  ```
  a, an, the, is, of, for, etc.
  ```
* Remove punctuation
* Treat singular & plural same:

  * stack = stacks
  * structure = structures

---

## Files Provided

* `webpages/`
* `actions.txt`
* `answers.txt`

---

# Part 3: PageRank on Spark (40 Marks)

## Dataset

* Graph with:

  * 1000 nodes
  * 8192 edges
* File: `whole.txt`
* Smaller test file: `small.txt`

---

## PageRank Formula

```
r = (1 - β)/n * A + β * M * r
```

Where:

* `β = 0.8`
* `A = vector of ones`
* `M = transition matrix`

---

## Algorithm

### Initialization

```
r₀ = 1/n
```

---

### Iteration (40 times)

```
r(i) = (1 - β)/n + β * M * r(i-1)
```

---

## Implementation Notes

* Use **Spark (RDDs)**
* Treat multiple edges as **single edge**
* Ensure all nodes have outgoing edges

---

## Output

### 1. Top 5 Nodes

* Highest PageRank scores

### 2. Bottom 5 Nodes

* Lowest PageRank scores

---

## Validation

* Run on `small.txt`
* Expected top score ≈ **0.036**

---

# General Instructions

* Code must be:

  * Clean
  * Commented
  * Executed

* No plagiarism (strict 🚨)

---

# Deliverables Checklist

* [ ] Jupyter Notebook
* [ ] GitHub Repo
* [ ] PDF Report
* [ ] Results + Analysis

