# Bulldozer Price Regression Model

A machine learning project that predicts the sale price of bulldozers using Random Forest Regression. This model analyzes historical auction data to forecast equipment prices based on various features including equipment specifications, usage patterns, and temporal factors.

## 📋 Project Overview

This project implements a complete machine learning pipeline for predicting bulldozer auction prices using scikit-learn. The model processes both numerical and categorical features, handles missing data, and achieves robust predictions through ensemble learning with Random Forest.

## 🎯 Features

- **Comprehensive Data Preprocessing Pipeline**
  - Automatic handling of missing values using median imputation for numerical features
  - Ordinal encoding for categorical features with unknown value handling
  - Date parsing and feature engineering from sale dates

- **Feature Engineering**
  - Extraction of temporal features: year, month, day, day of week, day of year
  - Automatically separates numerical and categorical features

- **Model Architecture**
  - Random Forest Regressor with optimized hyperparameters
  - 90 estimators for robust predictions
  - Parallel processing enabled for faster training

- **Evaluation Metrics**
  - Mean Absolute Error (MAE)
  - Root Mean Squared Log Error (RMSLE)
  - R² Score
  - Comprehensive training and validation metrics

- **Feature Importance Analysis**
  - Identification of most influential features
  - Visualization of top contributing factors

## 🛠️ Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **matplotlib** - Data visualization
- **scikit-learn** - Machine learning pipeline and models
  - RandomForestRegressor
  - Pipeline
  - ColumnTransformer
  - SimpleImputer
  - OrdinalEncoder

## 📁 Project Structure

```
bulldozer_price_regression/
│
├── bluebook_bulldozer_price_regression.ipynb  # Main Jupyter notebook
├── Train.csv                                   # Training dataset
├── Valid.csv                                   # Validation dataset
├── ValidSolution.csv                          # Validation ground truth
├── README.md                                   # Project documentation
└── anaconda_projects/                         # Additional project files
```

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.x installed along with the following packages:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

### Installation

1. Clone the repository:
```bash
git clone git@github.com:memoer30/Bulldozer-Price-Regression.git
cd bulldozer_price_regression
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```
*(Note: Create a requirements.txt file if needed)*

3. Launch Jupyter Notebook:
```bash
jupyter notebook bluebook_bulldozer_price_regression.ipynb
```

## 📊 Dataset

The project uses bulldozer auction data with the following structure:

- **Train.csv**: Historical training data with sale prices
- **Valid.csv**: Validation dataset for model evaluation
- **ValidSolution.csv**: Ground truth prices for validation set

### Key Features:
- **YearMade**: Manufacturing year of the equipment
- **saledate**: Date of the auction sale
- **Equipment specifications**: Various categorical features describing the bulldozer
- **SalePrice**: Target variable (price at auction)

## 🔄 Pipeline Workflow

1. **Data Loading**: Import training and validation datasets with proper date parsing
2. **Feature Engineering**: Extract temporal features from sale dates
3. **Preprocessing**: 
   - Numerical features: Median imputation
   - Categorical features: Convert to strings → Ordinal encoding
4. **Model Training**: Random Forest Regressor with optimized parameters
5. **Evaluation**: Calculate MAE, RMSLE, and R² scores
6. **Analysis**: Feature importance visualization

## 📈 Model Performance

The model evaluates performance using multiple metrics:

- **Mean Absolute Error (MAE)**: Measures average prediction error
- **Root Mean Squared Log Error (RMSLE)**: Penalizes large errors, suitable for price prediction
- **R² Score**: Indicates proportion of variance explained by the model

*Run the notebook to see actual performance metrics*

## 🎨 Visualizations

The notebook includes:
- Feature importance bar chart showing top 20 most influential features
- Data exploration outputs

## 🔑 Key Findings

Feature importance analysis reveals:
- **YearMade**: Most significant predictor of bulldozer price
- **saleYear**: Temporal Market conditions impact pricing
- **Equipment characteristics**: Various technical specifications contribute to value

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

Created by [Your Name]

## 🙏 Acknowledgments

- Dataset sourced from historical bulldozer auction data
- Built with scikit-learn's robust machine learning tools

---

*For questions or feedback, please open an issue in the repository.*
