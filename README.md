

---

# 1️⃣ BFS (Breadth First Search)

### 🔹 কী?

Graph traversal algorithm
👉 **Level by level** node visit করে

### 🔹 Data Structure

✅ **Queue**

### 🔹 Steps

1. Source node queue তে ঢুকাও
2. Mark visited
3. Queue থেকে বের করে তার unvisited neighbour গুলো queue তে ঢুকাও

### 🔹 Example Use

* Shortest path (unweighted graph)
* Level order traversal
* Connected components

### 🔹 Time Complexity

**O(V + E)**

---

# 2️⃣ DFS (Depth First Search)

### 🔹 কী?

Graph traversal algorithm
👉 **একদম গভীরে গিয়ে তারপর backtrack**

### 🔹 Data Structure

✅ **Recursion / Stack**

### 🔹 Steps

1. Node visit
2. Neighbour থাকলে recursive DFS call
3. শেষ হলে backtrack

### 🔹 Use Case

* Cycle detection
* Topological sort
* Articulation point

### 🔹 Time Complexity

**O(V + E)**

---

## 🆚 BFS vs DFS (Exam Table)

| BFS                        | DFS                |
| -------------------------- | ------------------ |
| Queue                      | Stack / Recursion  |
| Level-wise                 | Depth-wise         |
| Shortest path (unweighted) | Structure analysis |
| More memory                | Less memory        |

---

# 3️⃣ Spanning Tree

### 🔹 Definition

Connected graph-এর এমন subgraph
যেখানে:

* সব vertex আছে
* **No cycle**
* **Edges = V − 1**

### 🔹 কেন দরকার?

* Network design
* Cable / road planning

### 🔹 Note (Exam ⭐)

👉 Graph connected না হলে spanning tree সম্ভব না

---

# 4️⃣ Kruskal Algorithm (MST)

### 🔹 কী?

**Minimum Spanning Tree** বের করার algorithm
👉 **Edge-based**

### 🔹 Steps

1. সব edge weight অনুযায়ী sort
2. ছোট edge নাও
3. Cycle হলে বাদ
4. Union-Find ব্যবহার

### 🔹 Data Structure

* Disjoint Set (Union-Find)

### 🔹 Time Complexity

**O(E log E)**

### 🔹 Best For

* Sparse graph

---

# 5️⃣ Prim Algorithm (MST)

### 🔹 কী?

Minimum Spanning Tree
👉 **Node-based**

### 🔹 Steps

1. যেকোনো node থেকে শুরু
2. সবচেয়ে ছোট weight edge বেছে নাও
3. New node add
4. Repeat until V-1 edges

### 🔹 Data Structure

* Priority Queue (Min Heap)

### 🔹 Time Complexity

**O(E log V)**

### 🔹 Best For

* Dense graph

---

## 🆚 Kruskal vs Prim (Exam Favourite)

| Kruskal      | Prim           |
| ------------ | -------------- |
| Edge based   | Node based     |
| Sort edges   | Min heap       |
| Sparse graph | Dense graph    |
| Union-Find   | Priority Queue |

---

# 6️⃣ 0/1 Knapsack (Dynamic Programming)

### 🔹 Problem

একটা bag (capacity W)
👉 Item হয় নেবে (1) না নেবে (0)

### 🔹 DP State

```
dp[i][w] = max value using first i items and capacity w
```

### 🔹 Transition

```
if wt[i] <= w:
  dp[i][w] = max(
      value[i] + dp[i-1][w-wt[i]],
      dp[i-1][w]
  )
else:
  dp[i][w] = dp[i-1][w]
```

### 🔹 Time & Space

* Time: **O(nW)**
* Space: **O(nW)** (optimizable)

### 🔹 Difference

| 0/1 Knapsack | Fractional   |
| ------------ | ------------ |
| DP           | Greedy       |
| Item split ❌ | Item split ✅ |

---

## 🔥 Final Revision Sheet (1 glance)

| Topic         | DS             | Complexity |
| ------------- | -------------- | ---------- |
| BFS           | Queue          | O(V+E)     |
| DFS           | Stack          | O(V+E)     |
| Spanning Tree | —              | V−1 edges  |
| Kruskal       | Union-Find     | O(E log E) |
| Prim          | Priority Queue | O(E log V) |
| Knapsack      | DP             | O(nW)      |

---


