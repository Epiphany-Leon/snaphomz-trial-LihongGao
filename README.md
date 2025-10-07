# Snaphomz Trial – Lihong Gao

This project serves as a technical trial assignment for **the Data Science & AI/LLM Integration Intern role at Snaphomz**. The goal is to demonstrate end-to-end capabilities across data preparation, predictive modeling, and LLM feature integration using only local, open-source tools.


## 1. Results
* **Key EDA Insight**: A significant price disparity exists between markets, with California's average price per square foot being substantially higher than Texas's.
* **Model Performance**: A baseline `LinearRegression` model achieved an R-squared of **53.86%** and a Mean Absolute Error of **$114.42 per sqft**, demonstrating the predictive power of basic property features.
* **LLM Feature**: Successfully implemented a local semantic search (RAG) system capable of finding relevant properties from unstructured `remarks` based on natural language queries.


## 2. Setup & Usage

* **Python Version**: 3.12+
* **Key Libraries**: Pandas, Scikit-learn, Sentence-Transformers
* **Environment Setup**:
    ```bash
    # Clone the repository
    git clone [Your Repository URL]
    cd snaphomz-trial-LihongGao

    # Create and activate a virtual environment
    conda create --name snaphomz-trial python=3.12 -y
    conda activate snaphomz-trial

    # Install dependencies
    uv pip install -r requirements.txt
    ```
* **How to Run**:
    ```bash
    # Launch Jupyter Lab and open the notebook
    jupyter lab notebooks/trial.ipynb
    ```
    Once open, run all cells from top to bottom to reproduce the analysis.


## 3. Decisions & Rationale

* **Predictive Model**: A `LinearRegression` model was chosen to predict `price_per_sqft`. This aligns with the "quick baseline" requirement, offering high interpretability and efficiency.
* **LLM Feature**: A Retrieval-Augmented Generation (RAG) approach was used for the Q&A feature. This robustly grounds answers in the provided data, demonstrating an ability to build a search system that avoids factual invention (hallucination).
* **Assumptions & Trade-offs**:
    * **Assumption**: The provided `listings_sample.csv` is representative of the broader market for the purpose of this trial.
    * **Trade-off**: Chose a simple, interpretable baseline model over a more complex, high-performance model to adhere to the "quick baseline" spirit of the assignment.


## 4. Known Limitations
* The analysis is based on a small sample dataset, so the insights may not be generalizable.
* The predictive model is a simple baseline; its accuracy could be significantly improved with more advanced algorithms and feature engineering.
* The RAG system performs semantic retrieval but does not have a generative component to synthesize natural language answers.


## 5. Time Spent
* **Approximate Hours**: 5-6 hours