# Consumer Opinion Analysis: A Data-Driven Examination of E-commerce Product Reviews
![Project Overview](Project_overviewW.png)
## Project Overview

This project conducts a comprehensive data-driven analysis of consumer opinions and feedback collected from various leading e-commerce platforms, including Flipkart, Amazon, Fresh India Organics, and BigBasket. Focusing primarily on reviews for **fruits**, this study aims to extract valuable insights into customer sentiments, identify key product attributes, and understand the underlying structure of consumer discourse.

Utilizing a robust data analysis framework, the project encompasses natural language processing (NLP) techniques, machine learning, and statistical methods to uncover patterns and actionable intelligence from unstructured text data.

## Key Objectives

* **Data Acquisition & Preprocessing:** Collect and clean raw consumer review data.
* **Sentiment Analysis:** Classify comments into positive, negative, and neutral sentiments to gauge overall customer perception towards products.
* **N-gram Analysis:** Identify frequently co-occurring phrases (bigrams and trigrams) to understand common associations and topics within reviews.
* **Clustering:** Group similar comments or terms to reveal natural clusters of opinions and discussions.
* **Term Co-occurrence Network:** Visualize relationships between frequently appearing terms to understand their contextual usage.
* **Statistical Analysis:** Investigate relationships between review characteristics (e.g., comment length) and sentiment scores.
* **Reporting:** Summarize all findings, methodologies, and visualizations in a detailed project report.

## Methodology

The project employs a multi-faceted approach, integrating several data analysis and NLP techniques:

* **Data Collection & Preparation:** Data is loaded from provided CSV and Excel files (`FDS_TotalDataSet.csv`, `FDS_TotalDataSet22_withsentiment.xls`) which contain customer IDs, items, comments, and sentiment labels. Preprocessing includes text cleaning, tokenization, and stop word removal.
* **Sentiment Classification:** Utilized machine learning models to classify sentiment, followed by performance evaluation using classification reports. (See `FDS_Step1(Sentimental Analysis)-Copy1.ipynb` and `FDS_Part1-Copy1 (1).ipynb`).
* **N-gram Generation:** Implemented bigram and trigram extraction to identify significant multi-word expressions in reviews. (See `Bigram_trigaram.ipynb`, `FDS_part1.1 (3).ipynb`).
* **TF-IDF Vectorization:** Converted text data into numerical representations (Term Frequency-Inverse Document Frequency) for quantitative analysis.
* **Hierarchical Clustering:** Applied agglomerative hierarchical clustering on comment data to identify natural groupings of similar reviews, visualized using dendrograms. (See `FDS_PART1.2 (3).ipynb`, `FDSDENDOGRAM.ipynb`, `FDSDENDOGARM22-Copy1.ipynb`).
* **Statistical Inference:** Performed one-sample t-tests and correlation analysis (Pearson and Spearman) to explore relationships between sentiment scores and comment length. (See `FDS_part3-Copy1 (1).ipynb`).
* **Co-occurrence Network Analysis:** Constructed and visualized a network illustrating the relationships and co-occurrence frequency of terms within the comments. (See `FDS_part4-Copy1 (1).ipynb`).

## Project Structure

The repository is organized as follows:

* `Bigram_trigaram.ipynb`: Jupyter Notebook for N-gram generation and visualization.
* `FDS_part1.1 (3).ipynb`: Jupyter Notebook for N-gram analysis and TF-IDF vectorization.
* `FDS_PART1.2 (3).ipynb`: Jupyter Notebook focusing on hierarchical clustering of comments.
* `FDS_Part1-Copy1 (1).ipynb`: Jupyter Notebook for sentiment analysis and evaluation (e.g., classification report).
* `FDS_part3-Copy1 (1).ipynb`: Jupyter Notebook for statistical analysis (t-tests, correlations).
* `FDS_part4-Copy1 (1).ipynb`: Jupyter Notebook for term co-occurrence network analysis.
* `FDS_Step1(Sentimental Analysis)-Copy1.ipynb`: Jupyter Notebook containing initial sentiment analysis steps.
* `FDSDENDOGARM22-Copy1.ipynb`: Jupyter Notebook for dendrogram visualization of important terms.
* `FDSDENDOGRAM.ipynb`: Further Jupyter Notebook for dendrogram analysis.
* `FDS_TotalDataSet.csv`: The primary raw consumer review dataset.
* `FDS_TotalDataSet22_withsentiment.xls`: Processed dataset including sentiment scores.
* `FDS_REPORT.pdf`: The final project report summarizing the methodology, findings, and conclusions.
* `README.md`: (This file) Project overview and instructions.
* `.gitignore`: Specifies files and directories to be ignored by Git (e.g., temporary Jupyter files).

## Technologies Used

* **Python 3.x**
* **Jupyter Notebook**
* **Key Libraries:** `pandas`, `numpy`, `scikit-learn`, `nltk`, `matplotlib`, `seaborn`, `plotly`, `networkx`, `scipy`, `collections`.

## How to Run the Project (Local Setup)

To replicate this analysis locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/ANILKUMARCHAGANTI/Consumer_opinion_Analysis.git](https://github.com/ANILKUMARCHAGANTI/Consumer_opinion_Analysis.git)
    cd Consumer_opinion_Analysis
    ```
2.  **Create a virtual environment (recommended for dependency management):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: `.\venv\Scripts\activate`
    ```
3.  **Install required Python libraries:**
    ```bash
    pip install pandas numpy scikit-learn nltk matplotlib seaborn plotly networkx
    ```
    * **NLTK Data:** You may also need to download specific NLTK data. If you encounter errors, run this in a Python interpreter or a new notebook cell:
        ```python
        import nltk
        nltk.download('punkt')
        nltk.download('stopwords')
        nltk.download('vader_lexicon')
        # You may also need 'averaged_perceptron_tagger', 'wordnet' based on specific notebooks
        ```
4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    This will open Jupyter in your browser. You can then navigate to and run each `.ipynb` file sequentially to reproduce the analysis.

## Key Insights and Findings

(Based on the abstract of your `FDS_REPORT.pdf` and typical findings from such projects)

* **Dominance of Positive Sentiments:** Initial findings often indicate a high presence of positive sentiments, particularly related to core product attributes such as "freshness," "quality," and "taste" of the fruits.
* **Identified Product Attributes:** N-gram analysis helps pinpoint the most frequently discussed product features that drive consumer satisfaction or dissatisfaction.
* **Opinion Clusters:** Clustering reveals natural groupings of comments that express similar opinions or discuss related topics, providing a segmented view of consumer feedback.
* **Term Relationships:** Co-occurrence networks visually demonstrate how different terms are associated within reviews, highlighting important contextual relationships (e.g., "good" with "product," "bad" with "delivery").

---
