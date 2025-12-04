# Tree Structure & Algorithms Analysis Project

## Project Overview
This project explores the implementation, performance analysis, and algorithmic applications of advanced tree structures. The work is divided into three core problems and one challenge problem, utilizing Python to benchmark search algorithms and solve complex graph labeling optimizations.

The project covers:

**1.** Search Performance: Comparing AVL Trees vs. Red-Black Trees.


**2.** Database Indexing: B-Tree implementation compared against linear lists and HashMaps.


**3.** Graph Labeling: Vertex k-labeling for Perfect Ternary Trees.

**4.** Optimization: Homogeneous Amalgamated Star graph labeling.

## Repository Structure

```
Assignment4_Application of Tree Structure & Algorithms in Different Fields of Sciences/
├── raw_data/                  
│   ├── frequent_words.txt     # Dataset for Problem 1
│   └── customer_data.csv      # Dataset for Problem 2
├── src/                       
│   ├── Assignment4_Problem1.ipynb  		  # Code for AVL and RB Tree Implementation 
│   ├── Assignment4_Problem2.ipynb  		  # Code for B-Tree Implementation
│   ├── Assignment4_Problem3.ipynb  		  # Code for Perfect Ternary Tree Labeling 
│   └── Assignment4_ChallengingProblem.ipynb  # Code for Star Graph Labeling 
├── results/  
│   └── output.csv    						  # Output of vertex labels and edge weights
└── Assignment4_ACT_FinalReport.pdf           # Detailed analysis and findings
└── README.md                 				  # Project overview and documentation

```

## Key Task & Findings

**1. AVL vs. Red-Black Tree Performance**

**Objective**: Store 1,000 frequent words and perform 100 random searches to compare the efficiency of strict balancing (AVL) vs. relaxed balancing (Red-Black) .

- **Hypothesis**: AVL trees offer faster search times due to strict balancing, while Red-Black trees perform better during insertion/deletion.

- **Results**:

  - **Search Efficiency**: AVL Trees were significantly faster for retrieval.

    - AVL Total Search Time: 0.3 ms.

    - Red-Black Total Search Time: 2,847.4 ms.

  - **Insertion Cost**: Red-Black trees were faster to build due to fewer required rotations.

    - AVL Insertion Time: 25.74 ms (746 rotations).

    - Red-Black Insertion Time: 5.57 ms (604 rotations)

**2. B-Tree Implementation**

**Objective**: Implement a B-Tree (minimum degree t=3) to store customer data and compare search comparisons against a standard List and a HashMap.

- **Results (100 Searches)**:

  -**List (Linear Scan)**: 4,814 comparisons (Avg: 48.14) - O(N).

    - **B-Tree**: 691 Comparisons (Avg: 6.91) - O(log N).

    - **HashMap**: 100 comparisons (Avg: 1) - O(1).

- **Conclusion**: Tree-based searching is far more efficient than unsorted lists, reducing comparisons by nearly an order of magnitude.

**3. Vertex k-labeling (Perfect Ternary Tree**

**Objective**: Implement an algorithm to assign vertex labels to a Perfect Ternary Tree ($T_{3,5}$) such that edge weights are unique and consecutive.

- **Graph Parameters**: $V = 364$, E = 363.

- **Methodology**: Used an implicit array structure and a Partitioned Edge-Weight Assignment strategy.

- **Verification**: 

  - **Theoretical Max Label (k)**: 182

  - **Algorithm Max Label**: 182

  - **Edge Weights**: All 363 edges had unique weights ranging from 2 to 364.

**4. Challenge: Homogeneous Amalgamated Star ($S_{m,n}$)**

**Objective**: Implement vertex k-labeling for a Star graph topology ($m$ arms, $n$ vertices per arm).

- **Star Case**: m = 12, n = 4 (V = 49).

- **Results**: Successfully achieved a perfect labeling with a max label of 25, matching the theoretical lower bound $\lceil V/2 \rceil$.

## Dataset Description

- **File**: [raw_data/1000 Frequent Words.txt](https://github.com/mosomo82/COMP_SCI_5501/blob/99818fd48448fe02eed8dfe07d148bd6f61ce8aa/Assignment/Assignment4_Application%20of%20Tree%20Structure%20%26%20Algorithms%20in%20Different%20Fields%20of%20Sciences/raw_data/1000%20Frequent%20Words.txt) ; [raw_data/customers-100.csv](https://github.com/mosomo82/COMP_SCI_5501/blob/main/Assignment/Assignment4_Application%20of%20Tree%20Structure%20%26%20Algorithms%20in%20Different%20Fields%20of%20Sciences/raw_data/customers-100.csv)
- **Source**: Provided by the project

## Technologies Used

- **Language**: Python.

- **Enviroment**: Google Colab.

- **Libraries**: math, collections, random, pandas.

## How to Run the Project

The code for this assignment is hosted on Google Colab. You can access the specific notebooks for each problem using the links below:

**1.** Problem 1 (AVL vs Red-Black):  in [src/Assignment4_Problem1.ipynb](https://github.com/mosomo82/COMP_SCI_5501/blob/main/Assignment/Assignment4_Application%20of%20Tree%20Structure%20%26%20Algorithms%20in%20Different%20Fields%20of%20Sciences/src/Assignment4_Problem1.ipynb) 

**2.** Problem 2 (B-Tree):  in [src/Assignment4_Problem2.ipynb](https://github.com/mosomo82/COMP_SCI_5501/blob/main/Assignment/Assignment4_Application%20of%20Tree%20Structure%20%26%20Algorithms%20in%20Different%20Fields%20of%20Sciences/src/Assignment4_Problem2.ipynb)

**3.** Problem 3 (Ternary Tree Labeling):  in [src/Assignment4_Problem3.ipynb](https://github.com/mosomo82/COMP_SCI_5501/blob/main/Assignment/Assignment4_Application%20of%20Tree%20Structure%20%26%20Algorithms%20in%20Different%20Fields%20of%20Sciences/src/Assignment4_Problem3.ipynb)

**4.** Challenge (Star Labeling): in [src/Assignment4_ChallengingProblem.ipynb](https://github.com/mosomo82/COMP_SCI_5501/blob/main/Assignment/Assignment4_Application%20of%20Tree%20Structure%20%26%20Algorithms%20in%20Different%20Fields%20of%20Sciences/src/Assignment4_ChallengingProblem.ipynb)

## Authors/Contributors:

- **Bhavya Harshitha Chennu**

- **Harris Hamid** 

- **Manan Koradiya** 

- **Amir Obsa**

- **Tony Nguyen**

## Acknowledgements

- **Course**: COMP-SCI 5501-0001: Advanced Computational Thinking.

- **Instructor**: Dr. Muhammad Asim

## References

[1].	Ahmad, A., Asim, M. A., Baca, M.and Hasni, R., 2018. Computing edge irregularity strength of complete m-ary trees using algorithmic approach. U.P.B. Sci. Bull., Series A, 80(3), pp.145–152.

[2].	Ahmad, A., Al-Mushayt, O., & Bača, M. (2014). "On edge irregularity strength of graphs." Applied Mathematics and Computation.

[3].	Muhammad Shahzad1, Muhammad Ahsan Asim2,*, Roslan Hasni3, and Ali Ahmad4. Computing Edge Irregularity Strength of Star and Banana Trees Using Algorithmic Approach. Published 30 June 2024.


