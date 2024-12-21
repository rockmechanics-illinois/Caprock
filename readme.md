# **Breakthrough Pressure Prediction**

This repository contains datasets, scripts, and machine learning workflows for analyzing and predicting breakthrough pressure based on rock properties. The repository is structured to facilitate exploratory data analysis, machine learning experiments, and physics-informed modeling to improve predictions of breakthrough pressure.

---

### **Directory Structure**

#### **1. Datasets**
This folder contains raw data files used for model training and validation:
- `direct1.csv`: Dataset containing direct measurements of rock properties and breakthrough pressure.
- `direct2.csv`: Additional dataset of direct measurements.
- `indirect1.csv`: Dataset including indirectly estimated rock properties for breakthrough pressure analysis.
- `indirect2.csv`: Another dataset with indirect property estimations.

#### **2. Output Plots**
This folder stores visualizations and performance plots generated during the modeling process:
- Comparative performance metrics of different models.
- Residual plots, predicted vs. actual breakthrough pressure, and feature importance graphs.

#### **3. Notebooks**
This repository includes the following Jupyter notebooks for different stages of analysis:
- **Bayesian Methods.ipynb**: Bayesian analysis of breakthrough pressure predictions, including uncertainty quantification.
- **Breakthrough Pressure Prediction.ipynb**: Comprehensive workflow for preprocessing, model training, and evaluation.
- **Exploratory Data Analysis.ipynb**: Initial analysis and visualization of rock property datasets to identify trends and relationships.
- **Oversampling Methods Final.ipynb**: Techniques for handling class imbalance using oversampling methods to improve prediction accuracy.
- **Physics Informed Neural Network.ipynb**: Implementation of neural networks grounded in physics-based loss functions to enhance predictive capability.
- **Simple Linear Regression.ipynb**: Baseline regression analysis for breakthrough pressure prediction.
- **XGBoost.ipynb**: Gradient boosting machine learning experiments for accurate pressure predictions.

---

### **Getting Started**

#### **Prerequisites**
Ensure you have the following software and libraries installed:
- Python 3.8+
- Jupyter Notebook
- Required Python libraries (listed in `requirements.txt`)

#### **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Breakthrough-Pressure.git
   ```
2. Navigate to the repository directory:
   ```bash
   cd Breakthrough-Pressure
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

### **Workflow Overview**

1. **Exploratory Data Analysis**:
    - The **Exploratory Data Analysis.ipynb** notebook focuses on loading and exploring datasets (`direct1.csv`, `direct2.csv`, `indirect1.csv`, and `indirect2.csv`) to analyze breakthrough pressure predictions. It utilizes libraries like `pandas`, `numpy`, `matplotlib`, and `seaborn` for data manipulation and visualization, along with tools like `sklearn` and `xgboost` for potential machine learning tasks. The notebook previews the datasets, processes column names for consistency, and sets up the groundwork for visualizations and model-building experiments, integrating machine learning and deep learning frameworks like PyTorch.
      - Python Notebook to run: `Exploratory Data Analysis.ipynb`
      - Imports from: Datasets/

2. **Data Preprocessing, Model Training and Evaluation**:

    - The notebooks implement a complete pipeline for breakthrough pressure prediction. Preprocessing includes handling missing values, scaling features, renaming columns (e.g., `Pore radius [nm]` to `Pore diameter [nm]`), and removing outliers using Z-scores. Polynomial feature expansion and log transformation are applied where beneficial. Models trained include Bayesian Ridge Regression, Gradient Boosting Regression (GBR), and a Physics-Informed Neural Network (PINN) with domain-specific loss functions. Oversampling techniques are applied to the indirect datasets to balance the data and tested on direct datasets to assess generalizability. Evaluation metrics like MSE, MAE, and \(R^2\) are used, along with visualizations such as residual plots and predicted vs. actual values. Bayesian methods further quantify uncertainty in predictions. This approach ensures robust and interpretable model performance.
      - Python Notebook to run: `XGBoost.ipynb`, `Physics Informed Neural Network.ipynb`, `Simple Linear Regression.ipynb`, `Bayesian Methods.ipynb`, `Oversampling Methods Final.ipynb`
      - Imports from: Datasets/


3. **Visualization**:
   - Plots in the `Output Plots` to analyze model performance and compare results.

---

### **Results**
The repository provides:
- Predictive models for breakthrough pressure based on direct and indirect measurements.
- Comparative analysis of traditional and advanced machine learning techniques.
- Physics-informed modeling to incorporate domain knowledge.
- Bayesian workflows to evaluate uncertainty bounds.
