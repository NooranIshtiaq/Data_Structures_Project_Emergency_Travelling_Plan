## Data Structures Emergency Traveling Plan

A graph-based shortest-path emergency travel planner implemented in C++
using adjacency lists, BFS, a custom queue, and linked lists — with no STL containers.

---

## About

This project models a city-to-city emergency travel system using a directed graph.
Given N cities connected sequentially, plus optional "aerial routes" between any two
cities, it computes the minimum travel time (in days) from city 1 to city N using
Breadth-First Search (BFS).

- Normal road travel between adjacent cities: **4 hours**
- Aerial route between any two cities: **24 hours**
- BFS finds the optimal route across all possible combinations

Built as a FAST-NUCES Data Structures course project by **Umaima Hashmi (22i-1984)**
and **Nooran Ishtiaq (22i-2010)**.

---

## Data Structures Used

| Structure | Implementation |
|---|---|
| Singly Linked List | Custom `node` + `linkedlist` classes |
| Queue | Linked-list-based, no STL |
| Graph | Adjacency list using linked lists |
| BFS | Custom queue-driven traversal |

---

### Linked List

A linked list is implemented with a `node` class containing:

- `data`: an integer value.
- `aerial_root`: a boolean indicating if the node has an aerial root.
- `next`: a pointer to the next node.

The `linkedlist` class initializes the head of the list.

### Queue

A queue is implemented using the linked list nodes. It has:

- `enqueue()`: Adds an element to the rear of the queue.
- `dequeue()`: Removes an element from the front of the queue.
- `Front()`: Returns the value at the front of the queue.
- `isEmpty()`: Checks if the queue is empty.

### Graph (Adjacency List Implementation)

A graph is represented using an adjacency list where each vertex points to its adjacent vertices. The `graph` class includes:

- `add_edge()`: Adds a directed edge between two cities.
- `add_adjacent_edges()`: Adds edges between consecutive cities.
- `add_aerial_root()`: Adds an aerial root between two cities.
- `print_aerial_roots()`: Prints cities connected by aerial roots.
- `print_graph()`: Prints the entire graph.

### Breadth-First Traversal

The breadth-first traversal algorithm finds the shortest path in terms of days between cities. Key points:

- Normal travel time between cities is 4 hours.
- Aerial travel time is 24 hours.
- The algorithm uses a queue to traverse the graph and calculates the shortest distance in days.

### Main Function

The main function handles user input for multiple test cases, constructs the graph, adds edges and aerial roots, and calculates the shortest travel time in days.
