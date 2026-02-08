#  AI Academic Course Recommender (GNN)

An intelligent recommendation engine built for **PSUT** students that uses **Knowledge Graphs** and **Graph Neural Networks (GNN)** to suggest valid next-semester study plans.

## The Problem
Standard recommenders often suggest courses that are either too easy, too hard, or mathematically impossible to register for due to missing prerequisites.

## The Solution
This project treats the university curriculum as a **Knowledge Graph**.
- **Nodes**: Students, Courses, and Topics.
- **Edges**: Prerequisites, Topics Covered, and Enrollment History.

### Key Features:
* **Heterogeneous GNN**: Uses `SAGEConv` (GraphSAGE) to learn relationships between student history and course topics.
* **Strict Prerequisite Filter**: A recursive logic layer ensures a course is only recommended if **all** prerequisites are met in the student's history.
* **Cohort-Aware Leveling**: Dynamically calculates academic standing (Year 1–4) to prevent suggesting remedial courses to seniors.
* **Cosine Similarity Ranking**: Fixes "NaN" score issues by normalizing node embeddings for stable, logical ranking.

## Tech Stack
- **Python** (Pandas, NumPy)
- **PyTorch & PyTorch Geometric** (Graph Neural Networks)
- **Knowledge Graph Representation**

##  Results
The system successfully identifies  electives (like AI/ML) for 3any year students who have completed their past level core requirements.
