# Graph Anonymization for Privacy-Preserving Network Analysis

This project implements and evaluates two algorithms—**Dynamic Programming (DP)** and **Greedy_Swap**—for anonymizing graph data to protect privacy while preserving structural utility. The goal is to modify a graph's topology so that nodes are indistinguishable within groups (degree anonymization), making re-identification difficult, while maintaining key network properties.

## 🔍 Overview

The anonymization process ensures *k-degree anonymity*, where each node’s degree appears at least `k` times in the graph. Two methods are implemented:

- **Dynamic Programming**: Constructs an anonymized degree sequence and builds a new graph.
- **Greedy_Swap**: Iteratively rewires edges to increase structural similarity with the original graph while preserving the anonymized degrees.

The system supports various graph types: random, small-world, and scale-free networks.

## 📊 Evaluation Metrics

- **Anonymization Success**: Achieved when all nodes satisfy k-anonymity.
- **Edge Overlap Ratio**: Measures structural preservation (`|E_original ∩ E_anonymized| / |E_original|`).
- **Graphicality Check**: Uses the Erdős–Gallai theorem to ensure the anonymized degree sequence can form a valid graph.
- **Lemma 2 Validation**: Ensures the anonymized graph can be constructed from the original (supergraph condition).

## 🛠️ Implementation

Built using Python with:

- `networkx` for graph manipulation
- `numpy`, `pandas` for data handling
- `matplotlib` for visualization

Key features:

- Degree sequence anonymization via dynamic programming
- Edge-swapping optimization to maximize overlap
- Automated debugging and logging for algorithm transparency
- Fallback mechanisms if anonymization fails

## 🧪 Results

Both algorithms successfully achieve degree anonymization across different graph models. The Greedy_Swap method maximizes edge overlap, enhancing utility for downstream analysis.

## 📄 License

MIT License – Open for research, modification, and educational use.
