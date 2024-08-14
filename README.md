# Problem Statement

Identify machines with potential failure based on data extracted from sensors during the manufacturing process.

## Requirements

The necessary packages and their respective versions are listed in the `requirements.txt` file.

## Data Files

- `desafio_manutencao_preditiva_teste.csv`
- `desafio_manutencao_preditiva_treino.csv`

## Data Analysis

The Profile Report used in the Exploratory Data Analysis (EDA) has been saved as `report_baseTreino.html`. You can download it from the Git repository and open it in a web browser.

## Model Evaluation

For each test run, the model generates a CSV file with evaluation metrics for each category. The file is named in the format `method_treatment.csv`.

The final model from `modelo_lighthouse.ipynb` (tab: `SVM with SMOTE oversampling and class weight FINAL`) saves an output file named `predicted.csv`, which contains two columns: `rowNumber` and `predictedValues`.

After running the `Importações` tab in the `modelo_lighthouse.ipynb` file, you can execute each tab for adjustment attempts of the training set (such as Oversampling or Undersampling) separately.

Since the nature of the problem involves failure detection, it is more important that the model does not miss identifying potential failures, even if the precision is not ideal, rather than incorrectly indicating that a machine about to fail will not fail. Therefore, the chosen metric for model comparison is Recall.

The `predicted.csv` file with predictions for the `desafio_manutencao_preditiva_teste.csv` dataset is located in the `output` folder.

## Quick Start

Follow these steps to run the project:

1. **Clone the Repository**

   ```bash
   git clone https://github.com/euconstante/ml-prediction.git
   cd ml-prediction.git
   ```

2. **Create and Activate a Virtual Environment**

   ```bash
   python3 -m venv myenv
   source myenv/bin/activate
   ```

3. **Install Required Packages**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run Data Analysis**

   - Open and execute the `report_baseTreino.html` for the Exploratory Data Analysis.

5. **Train and Evaluate Models**

   - Open the `modelo_lighthouse.ipynb` notebook.
   - Run the `Importações` tab to import necessary libraries and data.
   - Execute the other tabs for training and evaluation, including any adjustment attempts like Oversampling or Undersampling.

6. **View Results**

   - The `predicted.csv` file containing the predictions will be saved in the `output` folder.
