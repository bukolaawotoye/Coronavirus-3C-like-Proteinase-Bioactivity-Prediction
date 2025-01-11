# Coronavirus-3C-like-Proteinase-Bioactivity-Prediction
# Drug Discovery Project

## Overview
This project focuses on the exploration of bioactivity data for drug discovery, specifically targeting the 3C-like protease (3CLpro) of coronaviruses. The aim is to identify potential inhibitors using computational techniques. The pipeline includes data retrieval, preprocessing, exploratory data analysis, feature extraction, and machine learning modeling.

## Features
- **Data Retrieval**: Bioactivity data was obtained from the ChEMBL database, targeting the 3C-like protease with IC50 values.
- **Data Preprocessing**: 
  - Filtering and handling missing values.
  - Classification of bioactivity classes (active, inactive, intermediate).
  - Creation of a clean dataset with key features: `molecule_chembl_id`, `canonical_smiles`, `bioactivity_class`, and `standard_value`.
- **Exploratory Data Analysis**:
  - Calculation of Lipinski descriptors to assess drug-likeness.
  - Conversion of IC50 values to pIC50 values.
  - Statistical analysis (Mann-Whitney U Test) to compare active and inactive compounds based on molecular properties.
- **Feature Engineering**:
  - Calculation of molecular fingerprint descriptors using PaDEL.
  - Removal of low-variance features to enhance model performance.
- **Machine Learning Modeling**:
  - Built a Random Forest Regressor to predict pIC50 values.
  - Evaluated the model with a scatter plot of actual vs. predicted values.
  - Used LazyPredict to benchmark different machine learning models.

## Requirements
The following libraries and tools are required to run the project:
- **Python**
- **Libraries**: 
  - `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `lazypredict`
  - `PaDEL-Descriptor` for molecular descriptor calculations

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/drug-discovery.git
   ```
2. Navigate to the project directory:
   ```bash
   cd drug-discovery
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. **Data Retrieval**:
   - Download the dataset from ChEMBL.
2. **Run Preprocessing**:
   ```bash
   python preprocess.py
   ```
3. **Run Analysis and Modeling**:
   ```bash
   python analysis_and_modeling.py
   ```
4. **View Results**:
   - Results, including plots and model performance metrics, will be saved in the `results/` directory.

## Results
- Random Forest Regressor achieved an R² score of **0.546**.
- LazyPredict results identified other competitive models with varying accuracy and computation time.
- Visualized active vs. inactive compounds through statistical tests and molecular property plots.

## Future Work
- Explore other machine learning models and hyperparameter tuning.
- Expand dataset with additional bioactivity data.
- Integrate deep learning approaches for more accurate predictions.

## Contributing
Contributions are welcome! Feel free to submit issues or pull requests.

## License
This project is licensed under the MIT License.

## Acknowledgments
- **ChEMBL Database** for providing the bioactivity data.
- **PaDEL-Descriptor** for molecular descriptor calculations.

## Contact
For any questions or suggestions, please reach out at [bukawotoye@gmail.com](mailto:your-email@example.com).
