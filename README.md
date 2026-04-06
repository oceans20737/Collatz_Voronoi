[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19441005.svg)](https://doi.org/10.5281/zenodo.19441005)
# Collatz Stained Glass
**Application of Voronoi Tessellation in a Binary Logarithmic Spiral Space**

**Author**: Hiroshi Harada  
**Date**: April 6, 2026  

---

## Overview
This study proposes a novel mathematical visualization framework that reveals the structural order underlying the Collatz conjecture (the 3n+1 problem), an unsolved problem in number theory, by combining a **binary logarithmic spiral space** with **Voronoi tessellation**.

By mapping natural numbers onto a binary geometric space and generating Voronoi cells, it illustrates how **the set of natural numbers forming the reverse Collatz tree (preimage tree) densely fills the logarithmic domain without gaps (Hausdorff dimension $D_H \approx 1.0$)**. This process is depicted as a “stained glass” window, with color variations corresponding to the number of evolutionary steps.

---

## Mathematical and Technical Approach

### 1. Mapping to the Binary Logarithmic Spiral Space
A natural number \(n\) is mapped to the following polar coordinates:

- $r = \log_2(n)$  
- $\theta = 2\pi(r \bmod 1)$

This mapping geometrically expresses **binary self-similarity, the parity-based periodicity of trajectories, and the uniqueness of the convergence direction toward “1”**.

---

### 2. Extracting the Perfect Packing Structure via Voronoi Tessellation
A total of \(N = 3000\) generator points are produced, and dummy points are placed along the outer boundary to close infinite cells. From this configuration, \(N = 1000\) Voronoi cells are extracted.

This stabilizes the geometric arrangement of natural numbers into a **closed tiling structure**, visually presenting a **dense packing pattern approaching Perfect Packing**.

---

### 3. Dynamic Coloring Based on Evolutionary Steps
Based on the Total Stopping Time, each cell is colored using the following three-phase gradient:

- **Cyan (Early stage)**: Powers-of-two sequences (the main trunk) that evolve rapidly.  
- **Yellow (Intermediate stage)**: Odd numbers reached via jump trajectories (e.g., 5, 13, 17), and odd numbers belonging to infinite series represented by \(4m+1\)  
  (e.g., 5-series = 21 → 85 → 341 → …, 13-series = 53 → 213 → 853 → …).  
- **Magenta (Late stage)**: Deep nodes (e.g., 27, 31, 41) that fill the remaining space after long trajectories.

---

### 4. Overlaying the Causal Tree
In the final frame, the causal structure of the reverse Collatz tree is overlaid onto the spiral space, visually demonstrating **where each natural number lands and how the even-multiple branches extend from those points**.

---

## Requirements
To run this program, the following Python libraries are required:

```bash
pip install numpy scipy matplotlib
```

---

## Usage
1. Run the script:
```bash
python collatz_stained_glass.py
```
2. During execution, the terminal will display progress (frame rendering status).  
3. Upon completion, an animated GIF file will be generated in the working directory, and a “completed image” with all cells colored will be displayed in a separate window.

---

## License
- **Research document / Concepts**: CC BY 4.0  
- **Python source code**: MIT License  
- Copyright (c) 2026 Hiroshi Harada

---
