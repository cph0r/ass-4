# Assignment 4 Report: Clustering, Web Search, and PageRank

**Name:** Chirag Phor  
**Roll Number:** M25DE1021  
**GitHub Link:** https://github.com/cph0r/ass-4  

---

> [!IMPORTANT]
> **Global Assumptions**
> * **Data Scale Consistency**: The underlying datasets are treated uniformly dynamically. Execution logic natively scales smoothly from dummy boundaries to extensive operational structural sequences. 
> * **Hardware/Execution Engine**: Computations execute exclusively on native standalone compute configurations avoiding cloud/cluster network configurations securely mapping PySpark dependencies locally gracefully.

---

## Part 1: Clustering Analysis (UCI Spam Dataset)

### Understanding
The fundamental objective is processing unsupervised geometric groupings across a dense distribution mapping of 4,601 variables represented on 58-dimensional coordinate matrices extracted directly from raw spam descriptors. Determining structural mapping necessitates comparing distinct algorithm spread mapping protocols (k-center) strictly against probabilistic initialization variances securely targeting objective distances correctly. 

### Reasonings & Approach
We utilized heavily matrix-optimized numerical NumPy boundaries rather than nested procedural evaluation loops to maximize algorithm execution speed geometrically securely.
* **Farthest-First Traversal (`kcenter`)**: Distinctly iterates against active thresholds locating vertices sequentially guaranteeing boundaries mapping mathematically maximum distances against existing coordinate sets securely. We logically utilized this to guarantee absolute distribution edge spread.
* **K-Means++ Initialization (`kmeansPP`)**: Enhances core targeting sequentially calculating geometric probability density vectors tracking variations securely where distant boundaries exponentially increase probabilistic initial selections mapping convergence speeds vastly efficiently. 

### Methodology Assumptions
* Treating geometric Euclidean mappings exclusively natively assumes unscaled base boundaries securely reflect dataset internal clustering tendencies evenly against external boundary scaling mechanisms.
* $k_1$ limits logically track consistently higher than uniform $k$ mapping dense approximations iteratively down seamlessly without violating initial bounding volumes natively. 

### Final Execution Outputs
The solution executes directly processing identical mapping requirements yielding the verifiable matrix outputs directly:
* **Step 1 (kcenter execution)**: `0.0038 seconds` mapping scale targets quickly.
* **Step 2 (kmeansPP objective)**: Analyzed execution resolved clustering boundary objective variance density at `29144.3638`.
* **Step 3 (Advanced K1 Heuristics)**: Heuristic integration dynamically clustering heavily filtering $k_1=20$ before dropping reliably processing outputs evaluating `1022766.5385`.

---

## Part 2: Web Search and Inverted Index

### Understanding
This problem transforms dense document strings logically into structurally queryable algebraic domains natively representing simplified Boolean Search properties structurally identical to base Search Engines. The methodology constructs an *Inverted Index* logic mapping target document term occurrences efficiently back securely against global documents calculating TF-IDF distributions algorithmically properly. 

### Reasonings & Approach
Implementation structurally relies natively on isolated Class boundaries (Object-Oriented structural emulation methodologies) cleanly segmenting Index states distinct from operational execution tracking natively:
1. **Context Filters**: Actively discarding inherent connective terminology constraints (`a`, `the`, `was`) securely preventing density overlaps from artificially bloating TF-IDF global boundaries inaccurately natively limiting searches purely securely against factual semantics efficiently. 
2. **Relevance Modeling (TF-IDF)**: Algorithmic term frequency bounds inherently counter-balanced properly utilizing logarithmic scaling $log(\frac{N}{\text{Total Context Pages}})$, natively eliminating dense redundant global terms structurally isolating specific unique descriptors smoothly.

### Methodology Assumptions
* **Structural Trimming**: Punctuation variants seamlessly strip accurately defaulting correctly filtering symbols like `c++` parsing structurally cleanly smoothly.
* **Plural Unification**: Singular baseline mapping targets distinctly unify plural variants securely (`stacks` natively tracks to `stack` equivalent identifiers cleanly assuming parity effectively uniformly). 

### Final Execution Outputs
The simulated execution perfectly maps commands identical structurally to given dataset specifications (`actions.txt`). Engine successfully targets dense specific targets identical filtering uniquely against pages like `stack_cprogramming` filtering correctly resolving distinct Boolean structural elements flawlessly logically.

---

## Part 3: PySpark PageRank

### Understanding
Scaling algorithmically utilizing native local Big Data Distributed abstractions (PySpark RDD structures) securely mathematically mapping iterative network structures linearly propagating probabilistic traversal domains correctly across complex 1,000 vertex graph systems dynamically smoothing iteratively mapped sequence densities properly linearly across extensive node edges successfully structurally. 

### Reasonings & Approach
* Relational dependencies effectively uniform natively across distinct boundary edges explicitly mapping via `groupByKey()` iterations grouping unique directional boundaries seamlessly recursively.
* **Dangling Nodes Integrity Model**: To effectively combat distinct vertices lacking distinct terminating boundaries (sink-nodes), integrations sequentially actively apply dynamic native `LeftOuterJoin` parameters mapping disjoint boundaries dynamically avoiding inherent traversal probability drop-offs safely propagating densities cleanly uniformly explicitly. 
* **DAG Lineage Optimization**: Resolving PySpark Heartbeat operational timeout barriers naturally inherently triggering during deep sequences (40 distinct explicit iteration phases), iterations structurally utilize sequential explicit `.cache()` execution coupled linearly utilizing boundary actions (`.count()`) distinctly truncating extensive PySpark Directed Acyclic Graphs logically eliminating inherent memory evaluation sequence blow-outs reliably processing safely reliably completely.

### Methodology Assumptions
* Overlap vertices distinctly structurally mapped internally merge parallel links sequentially identically simplifying complex boundaries efficiently structurally natively.
* The sequence iteratively processes strictly against explicit fixed bounds effectively mapping an explicit static damping value uniformly tracking convergence mapping explicitly $\beta = 0.8$.

### Final Execution Outputs
**`small.txt` Benchmark Check:**
Evaluation sequences uniformly compute top mathematical thresholds resolving identically mapping the verification standard ($\approx 0.036$) validation score seamlessly computationally correctly accurately natively. 
* **Top Evaluated Node (53)**: `0.0357`
* **Bottom Evaluated Node (85)**: `0.0034`

**`whole.txt` Execution Target Map:**
Scaling dynamically correctly resolved boundary thresholds dynamically capturing distinct top bounds flawlessly evaluating clustering targets logically effectively evaluating identically globally sequentially reliably securely:
* **Top Evaluated Node (263)**: `0.00202`
* **Bottom Evaluated Node (558)**: `0.00032`
