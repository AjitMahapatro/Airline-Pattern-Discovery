# ✈️ Operational Pattern Discovery System

### 📌 Project Overview
This project applies **Unsupervised Learning** to large-scale aviation datasets to move beyond basic reporting. Instead of just seeing *that* a delay happened, this system discovers the hidden "If-Then" patterns (Association Rules) that explain **why** they happen across complex variables like Carrier, Origin, and Destination.

### ⚙️ Technical Approach
* **Algorithm:** Association Rule Mining via **FP-Growth** (Frequent Pattern Growth).
* **Core Metrics:** Evaluated results based on **Support, Confidence, and Lift** to ensure statistical significance.
* **Data Processing:** Cleaned and transformed raw flight logs into transactional formats using **Pandas**.
* **Visual Logic:** Utilized **Graph Theory (NetworkX)** to visualize how specific airports act as "bottleneck nodes" in delay propagation.

### 🔍 Key Discovery & Reasoning Logic
The model isolated specific **Carrier-Route combinations** that exhibited a **90% probability** of disruption. 
* **Insight:** Discovered that certain airlines operating out of specific hubs (e.g., Charlotte or Dallas) had a "Lift" value > 5.0, meaning the delay was 5x more likely to occur than the average baseline.

### 🛠 Tech Stack
* **Language:** Python
* **Libraries:** MLxtend (FP-Growth), Pandas, NumPy, NetworkX, Matplotlib
* **Data Source:** Airline On-Time Performance Data (Transactional Logs)

---
**Note:** The raw dataset is over 25MB and is excluded from this repository for performance; however, all logic and pattern discovery scripts are fully documented in the `.ipynb` file.
