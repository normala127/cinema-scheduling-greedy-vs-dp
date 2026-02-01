# Optimizing Cinema Scheduling  
### Greedy vs Dynamic Programming Algorithms

This project focuses on **optimizing movie cinema scheduling** to maximize revenue under realistic operational constraints.  
Two algorithmic approaches are implemented and compared:

- **Greedy Scheduling Algorithm**
- **Dynamic Programming (Knapsack-based) Algorithm**

The project was developed as part of the **CS207 – Algorithms and Data Structures** course at the **International University of Sarajevo**.

---

## Problem Description

Cinemas operate under strict constraints such as:
- Limited daily operating hours
- Fixed screen availability
- Movie durations
- Cleaning and buffer times
- Revenue maximization goals

The objective is to **schedule movies across multiple screens and days** in a way that:
- Maximizes total revenue
- Respects all time and operational constraints
- Ensures feasible and efficient schedules

---

## ⚙️ Algorithms Implemented

### 1️Greedy Scheduling Algorithm
- Selects movies based on a heuristic (e.g. revenue-to-duration ratio)
- Prioritizes locally optimal choices
- Fast and efficient
- Does **not guarantee global optimality**

**Advantages**
- Low computational cost
- Easy to implement
- Suitable for large datasets

**Limitations**
- Can miss better global solutions

---

### 2️Dynamic Programming Algorithm (Knapsack-based)
- Models the scheduling problem as a **knapsack optimization**
- Considers all feasible combinations within time limits
- Guarantees **optimal revenue**

**Advantages**
- Produces optimal solutions
- Handles constraints rigorously

**Limitations**
- Higher time and space complexity
- Less scalable for very large inputs

---

## Implementation Details

### Data Structures
- Movie objects storing:
  - Duration
  - Revenue
  - Screening constraints
- Schedules represented as structured lists per screen and day

### Constraint Handling
- Daily cinema operating limit
- Non-overlapping screenings
- Movie duration and buffer times
- Multi-day scheduling support

### Helper Functions
- Revenue calculation
- Schedule validation
- Time feasibility checks

---

## Theoretical Analysis

### Time Complexity
| Algorithm | Time Complexity |
|---------|----------------|
| Greedy | O(n log n) |
| Dynamic Programming | O(n × T) |

*(where n is number of movies, T is available time)*

### Space Complexity
| Algorithm | Space Complexity |
|---------|----------------|
| Greedy | O(n) |
| Dynamic Programming | O(n × T) |

---

## Empirical Evaluation

Both algorithms were tested on the same datasets to compare:
- Total revenue
- Runtime performance
- Scalability
- Practical feasibility

**Results**
- Greedy performs well for large inputs with minimal runtime
- Dynamic Programming achieves higher revenue when optimality is required
- Trade-off between speed and solution quality is clearly observed

---

## Practical Comparison

| Aspect | Greedy | Dynamic Programming |
|------|--------|--------------------|
| Speed | Fast | Slower |
| Optimality | Not guaranteed | Guaranteed |
| Scalability | High | Moderate |
| Use Case | Real-time scheduling | Revenue-critical planning |

---

### Requirements
- Python 3.x

- Author

Asja Bašović
International University of Sarajevo
Spring 2025

License

This project is developed for educational purposes.
