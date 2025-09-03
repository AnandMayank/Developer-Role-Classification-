# Create README.md file content
# Developer Role Classification Project

## Project Description
This project aims to classify the role of a software developer (Backend, Frontend, Fullstack, QA) based on their commit history data. The analysis involves data preprocessing, exploratory data analysis, feature engineering, model training, and evaluation.

## Repository Structure
This repository is organized into the following notebooks and files:

-   `Notebooks/preprocessing.ipynb`: Contains reproducible code for loading the raw data and performing all necessary preprocessing steps to create a model-ready dataset.
-   `Notebooks/eda.ipynb`: Includes visual and written observations from the exploratory data analysis, revealing dataset properties and potential risk factors.
-   `Notebooks/modelling.ipynb`: Presents the model selection process, including at least one baseline model and one improved model experiment, along with the training/validation protocol, hyperparameter notes, and logged results.
-   `final_dataset.csv`: The dataset used for this project.
-   `Final_report.pdf`: A detailed report on the project results.
-   `task.pdf`: The project task description.
-   `guidelines (1).pdf`: Additional guidelines.
-   `Annotated_examples_test.txt`:  Annotated examples — ten commits from different roles annotated in   plain language explaining
-   `README.MD`: This file, explaining the project and how to reproduce the results.

## Prerequisites
Before running the notebooks, ensure you have the following installed:
- Python 3.7 or higher
- Required libraries: pandas, numpy, scikit-learn, nltk, matplotlib, seaborn, xgboost

You can install the required libraries using pip:
```
pip install pandas numpy scikit-learn nltk matplotlib seaborn xgboost
```

Also, download NLTK data if not already done:
```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
```

## Reproducing Results End-to-End
To reproduce the results of this project, follow these steps:

1.  **Clone the repository:**
   ```
   git clone https://github.com/AnandMayank/Developer-Role-Classification-.git
   cd Developer-Role-Classification-
   ```

2.  **Install dependencies:**
   Follow the prerequisites section above to install the required libraries.

3.  **Run the notebooks in order:**
   - Open `Notebooks/preprocessing.ipynb` in Jupyter Notebook or JupyterLab and run all cells. This will load the data from `final_dataset.csv`, perform preprocessing (one-hot encoding, text processing with TF-IDF, scaling numerical features), and prepare the dataset for modeling.
   - Open `Notebooks/eda.ipynb` and run all cells. This performs exploratory data analysis, including visualizations of feature distributions and feature engineering (e.g., commit message length, interaction terms).
   - Open `Notebooks/modelling.ipynb` and run all cells. This includes model selection (baseline Logistic Regression, improved Random Forest and XGBoost), hyperparameter tuning, cross-validation, and final evaluation on the test set.

4.  **View results:**
   After running the notebooks, you can view the evaluation metrics, confusion matrix, and other outputs in the modelling notebook.

## Alternative Reproduction with Colab
For a more streamlined and cloud-based reproduction, you can use the provided Google Colab notebook:
- [Colab Link](https://colab.research.google.com/drive/18u8CA7yBda09jyUjHqI4V_pk5JxV_j8P?usp=sharing)
This Colab environment includes all necessary dependencies pre-installed and provides a proper reproducing flow with additional results and visualizations.
