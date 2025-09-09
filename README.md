ThreatTorch: Intrusion Detection WebApp

ThreatTorch is an Intrusion Detection System (IDS) project developed during my third year of college.
The project demonstrates how machine learning can be applied to detect malicious network activity in large-scale datasets.

The work includes:

Performing Exploratory Data Analysis (EDA) to understand traffic behavior.

Training and evaluating multiple machine learning models.

Saving the trained models as .pkl files for reuse.

- The GUI is functional for prediction but not fully responsive, so I don’t plan to deploy it in production.
- A short demo video may be added later to show the prediction process in action.

Motivation

With the increasing frequency and sophistication of cyberattacks, traditional security methods are not always enough. Intrusion Detection Systems (IDS) help detect and prevent malicious activities.

The motivation behind ThreatTorch was to:

Learn how data science and ML techniques can be used for cybersecurity.

Perform realistic analysis of IDS datasets.

Compare multiple classification models to identify the most effective one.

Build a working prototype of an IDS webapp for demonstration purposes.

Tech Stack

Languages & Libraries:

Python: Data preprocessing, EDA, modeling.

Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn.

Pickle: For storing and reusing trained models.

Frontend (WebApp):

HTML, CSS, JavaScript (for the GUI).

Project Workflow
1) Dataset & Preprocessing

Loaded the IDS dataset into a pandas DataFrame.

Cleaned missing or inconsistent values.

Applied feature encoding and scaling where required.

Handled class imbalance (more benign traffic vs. fewer attacks).

2️) Exploratory Data Analysis (EDA)

EDA was a crucial step in understanding network traffic patterns:

Class distribution: Visualized Attack vs. Benign traffic counts to highlight dataset imbalance.

Protocol analysis: Examined distributions across major protocols (TCP, UDP, ICMP, IGMP). Found which protocols were more prone to attacks.

Correlation heatmap: Analyzed relationships between numeric features to avoid multicollinearity.

Attack categories: Visualized attack types (DoS, Probe, R2L, U2R, etc.) and their proportions.

Port-based trends: Checked distributions of Source Ports and Destination Ports grouped by categories to see which ports were more frequently targeted.

Traffic size distributions: Studied IN_BYTES and OUT_BYTES with histograms and log transforms to reveal hidden skewness.

This step provided insights that guided feature engineering and model selection.

3️) Modeling

Multiple machine learning models were trained and compared:

Logistic Regression: As a baseline classifier.

Random Forest: For ensemble-based classification.

XGBoost: For high-performance gradient boosting.

Other models: Experimented with additional classifiers for comparison.

Evaluation metrics:

Accuracy

Precision

Recall

F1-score

The results helped identify which models performed best on intrusion detection tasks.

-Models were saved as .pkl files for reuse.
-Some large .pkl files are excluded from GitHub due to the 100 MB file size limit.

4️)WebApp Integration

Built a basic webapp GUI with HTML, CSS, and JavaScript.

Connected the trained ML model backend (via .pkl) to allow predictions on user inputs.

The GUI simulates a user entering traffic features and receiving an “Attack” or “Benign” prediction.

Current limitation: UI is static and not fully responsive (best viewed on desktop).
