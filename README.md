# Effective Time Series Forecasting Supported by Causal Discovery

## Project Overview
This project explores the integration of causal discovery methods into time series forecasting models, with a specific application to stock market data. By leveraging causal inference algorithms such as **VAR-LiNGAM** and **PCMCI**, we aim to enhance feature selection and improve predictive accuracy. Combining these methods with advanced forecasting models like **LSTM**, the project demonstrates how causality can improve robustness and interpretability in financial forecasting.

---

## Key Objectives
1. **Feature Selection**: Use causal discovery methods to identify the most relevant features and eliminate spurious correlations.
2. **Causal Integration**: Incorporate causal information into forecasting models to improve accuracy and robustness.
3. **Stock Market Application**: Demonstrate the effectiveness of this approach using real-world financial datasets.

---

## Methodology
### Causal Discovery Methods
- **VAR-LiNGAM**:
  - Combines Vector AutoRegression (VAR) and Linear Non-Gaussian Acyclic Model (LiNGAM).
  - Identifies temporal and contemporaneous causal relationships in financial data.
  - Features selected: `High_Apple`, `Close_Apple`, `High_Google`, `Low_Google`, `High_Microsoft`.

- **PCMCI**:
  - Detects lagged and contemporaneous causal relationships using Partial Correlation and Conditional Independence tests.
  - Features selected: `Low_Apple`, `Open_Microsoft`, `Open_Amazon`, `High_Amazon`, `Low_Microsoft`.

### Forecasting Models
- **Random Forest**: Used as a baseline model for its robustness with non-linear relationships.
- **LSTM (Long Short-Term Memory)**: Applied for its ability to capture temporal dependencies and sequential patterns.

---

## Results
### Feature Selection Impact
- **VAR-LiNGAM**: Reduced the feature set from 20 to 5, eliminating spurious correlations and improving robustness.
- **PCMCI**: Achieved a similar reduction in features while maintaining predictive relevance.

### Model Performance
- **With VAR-LiNGAM**:
  - **RMSE**: 3.77 USD (Close_Google prediction).
  - Outperformed models without causality by 82% in terms of RMSE.
- **Without VAR-LiNGAM**:
  - **RMSE**: 22 USD.
  - Demonstrated the drawbacks of correlation-based feature selection.

- **PCMCI**:
  - Demonstrated similar improvements in accuracy, with consistent reductions in MAE and RMSE for both univariate and multivariate datasets.

---

## Dataset
- **Source**: Yahoo Finance.
- **Time Period**: January 1, 2010 - December 31, 2023.
- **Variables**: `Open`, `High`, `Low`, `Close`, `Volume`.
- **Target**: `Close_Google` (Google's daily closing price).
- **Prediction Horizon**: 1 month.

---

## Experimental Environment
- **Programming Language**: Python.
- **Libraries**:
  - Causal Discovery: `tigramite` (PCMCI), custom implementations for VAR-LiNGAM.
  - Machine Learning: `scikit-learn`, `TensorFlow`, `Keras`.
  - Data Processing: `pandas`, `numpy`.

---

## Conclusion
Integrating causal inference into financial forecasting:
- Improves predictive accuracy and robustness.
- Reduces the risk of overfitting and spurious correlations.
- Enhances interpretability through causal relationships.

The study highlights the potential of causal discovery methods like VAR-LiNGAM and PCMCI to transform traditional time series forecasting approaches.

---

## Future Work
1. Explore other causal inference methods (e.g., Granger causality).
2. Optimize computational efficiency for high-dimensional datasets.
3. Extend the methodology to other domains such as healthcare or climate modeling.

---

## Authors
- **Naël Briand**
- **Quentin De La Chaise**

---

## Citation
If you use this repository, please cite our report:

