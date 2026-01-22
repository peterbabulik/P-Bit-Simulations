# P-Bit-Simulations

**Exploring probabilistic computing: Solving NP-hard optimization and pattern restoration using energy landscape minimization.**

## 🧠 Overview

Traditional computing relies on deterministic bits (0 or 1). This repository explores the concept of **Probabilistic Bits (P-bits)**—stochastic units that fluctuate between states to find the most "stable" (lowest energy) configuration of a system. 

By treating mathematical problems as physical systems, we can use energy-based models to solve complex optimization problems and simulate associative memory. This project implements two core experiments using **Simulated Annealing** and **Hopfield Networks**.

---

## 🚀 Experiments

### 1. The Perfect Split (Number Partitioning)
**The Problem:** Given a set of random integers, how do you split them into two piles so that the difference between their sums is as close to zero as possible? This is a version of the *Number Partitioning Problem*, which is NP-hard.

**The Solution:**
*   **Method:** Simulated Annealing (Metropolis-Hastings Algorithm).
*   **Mechanism:** The system starts at a high "temperature," allowing the P-bits to flip randomly. As the system cools, it settles into a global energy minimum—the most balanced state possible.
*   **Visual:** The included plotter tracks the "energy" (difference between piles) as it converges toward zero.

### 2. Associative Memory (Hopfield Network)
**The Problem:** How can a system "remember" a pattern and recover it even if the input is corrupted by heavy noise?

**The Solution:**
*   **Method:** Hebbian Learning ("Neurons that fire together, wire together").
*   **Mechanism:** We sculpt an energy landscape where the "saved memory" sits at the bottom of a deep valley. 
*   **Process:** 
    1.  **Train:** Store a 20x20 visual pattern.
    2.  **Corrupt:** Inject 30% random noise into the pattern.
    3.  **Restore:** Use the P-bit swarm to perform asynchronous updates, letting the system "fall" back into the stored memory state.

---

## 🛠️ Key Algorithms
*   **Metropolis-Hastings:** A Markov Chain Monte Carlo (MCMC) method used to accept or reject state changes based on thermodynamic probability.
*   **Energy Landscapes:** Defining a cost function where the optimal solution is mathematically equivalent to the lowest physical energy.
*   **Asynchronous State Updates:** Updating individual neurons/bits one at a time to ensure convergence and prevent system oscillations.

---

## 📦 Installation & Usage

### Prerequisites
You will need Python 3.x and the following libraries:
```bash
pip install numpy matplotlib seaborn
```

### Running the Simulations
Simply clone the repo and run the main script:
```bash
git clone https://github.com/peterbabulik/P-Bit-Simulations
cd P-Bit-Simulations
python p_bit_main.py
```

---

## 📊 Visualizations
The code generates two primary plots:
1.  **Energy Decay Curve:** Shows the optimization process of the Number Partitioning experiment.
2.  **Pattern Restoration Grid:** A side-by-side comparison of the Original Memory, the Corrupted Input, and the Final Restored State.

---

## 📜 License
This project is open-source and available under the MIT License.

---
*Developed to explore the intersection of Statistical Mechanics and Computer Science.*
