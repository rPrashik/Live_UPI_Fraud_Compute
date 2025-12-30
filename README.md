In the fast-evolving landscape of digital payments, UPI fraud has become a significant challenge. This project implements a high-velocity data pipeline and machine learning solution to detect and prevent fraudulent transactions in real-time. By integrating AWS S3 with Databricks, the system monitors live transaction streams, compares them against historical baselines, and triggers automated banking recommendations.

🛠️ Technology Stack & Tools Applied
1. Cloud Storage & Data Lake (AWS S3)
•	Role: Served as the primary landing zone for both static and streaming data.
•	Knowledge Applied: Managed "Variety" and "Volume" by segregating Historical Baseline Data (2024) from Live Transaction Streams (2025). This allows for temporal comparison and "Fraud Migration" analysis.

2. Unified Analytics Platform (Databricks)
•	Role: The core computational environment for Data Engineering and Data Science.
•	Knowledge Applied: Leveraged Databricks for collaborative development and seamless integration between Spark SQL and Python environments.

3. Distributed Computing (PySpark & Structured Streaming)
•	Role: High-speed ingestion and processing engine.
•	Knowledge Applied: * Implemented Schema Enforcement to ensure data integrity across thousands of small CSV files.
o	Utilized Spark’s distributed architecture to aggregate and transform millions of records with minimal latency, solving the "Velocity" problem of Big Data.

4. Advanced Analysis (Spark SQL)
•	Role: Optimized querying engine for complex analytical tasks.
•	Knowledge Applied: Created SQL views to calculate real-time fraud ratios and identify geographic "Hotspots" (States with high fraud-to-transaction ratios).

5. Machine Learning (Scikit-Learn & Random Forest)
•	Role: Predictive intelligence layer.
•	Knowledge Applied: * Target Encoding (Risk Mapping): Instead of standard Label Encoding, I mapped states to their actual fraud probability. This provides the model with intuitive geographic risk context.
o	Probabilistic Classification: The model outputs a risk score (0-1), allowing the bank to move beyond binary "Yes/No" logic to nuanced "Risk-Based Authentication."

📊 Core Features & Insights
•	Real-Time Risk Heatmaps: Interactive visualizations showing which Indian states are currently under the highest threat.
•	Temporal Danger Zones: Analysis of transaction timestamps to identify specific "High-Alert" hours (e.g., late-night spikes).
•	Automated Action Logic:
    Low Risk: Instant Approval.
    Medium Risk: Trigger Step-up Authentication (Biometric/OTP).
    High Risk: Automated Block & Account Freeze.

🧠 Knowledge Applied: The Big Data "3 Vs"
•	Volume: Handled millions of historical records from the 2024 dataset.
•	Velocity: Processed thousands of live incoming CSV files simultaneously using Spark's parallel processing.
•	Variety: Managed diverse transaction features including Merchant Categories, Device Types, and Network Types to build a 360-degree user profile.

🚀 How to Run
1.	Configure AWS S3: Ensure your S3 buckets are accessible from your Databricks cluster.
2.	Import Notebook: Upload the .ipynb file to your Databricks workspace.
3.	Run Pipeline: Execute the cells sequentially to build the SQL views, train the model, and generate real-time recommendations.

Contact & Portfolio
•	Developed by: Prashik Ramteke
•	Focus: Big Data | Data Engineering | Machine Learning
