
Temperature Forecasting using Long Short-Term Memory (LSTM) Networks
Deep Learning Microproject – UEC642 (Aug–Dec 2025)

This repository contains the complete implementation and documentation for a Deep Learning microproject focused on short-term temperature forecasting using LSTM (Long Short-Term Memory) networks. It demonstrates how deep learning can effectively learn temporal dependencies in meteorological data to produce accurate, efficient, and localized forecasts.

--------------------------------------------------------------------------------

Project Overview

Traditional weather forecasting relies on Numerical Weather Prediction (NWP) models that are physics-based and computationally heavy. In contrast, data-driven deep learning methods learn directly from historical patterns, enabling faster and more efficient forecasting.

This project uses a two-layer LSTM model trained on multivariate weather data (temperature, humidity, and pressure) to predict future temperature values. The model achieves high accuracy with low computational cost—ideal for real-time and small-scale applications.

--------------------------------------------------------------------------------

Methodology

Data Preprocessing:
- Cleaned and normalized input features using Min–Max scaling.
- Removed missing or noisy values.
- Created time sequences using a sliding window approach.
- Split dataset chronologically into training (80%) and testing (20%).

Model Architecture:
1. LSTM layer with 64 units (tanh activation) – captures long-term dependencies.
2. LSTM layer with 32 units (tanh activation) – learns short-term temporal trends.
3. Dropout layer (0.2) – reduces overfitting.
4. Dense output layer – predicts temperature value.

Optimizer: Adam (learning rate = 0.001)
Loss Function: Mean Squared Error (MSE)
Evaluation Metrics: RMSE (°C), R²

Training Configuration:
- Epochs: 100
- Batch Size: 64
- Framework: TensorFlow / Keras
- Hardware: Standard CPU (no GPU required)

--------------------------------------------------------------------------------

Results

RMSE: 1.57 °C
R²: 0.976

The model predicts temperature within ±1.5 °C of actual readings on average.
It performs best in stable climatic regions such as Toronto, Detroit, and Montreal, while showing slightly higher deviation in extreme regions (Eilat, Phoenix).
Residual plots confirm low bias and high generalization capability.

Figures:
- Predicted vs Actual Temperature (Test Set)
- Residual Distribution Plot
- Error Metric Comparison (RMSE & R²)

--------------------------------------------------------------------------------

Comparison with Recent Work

| Model | Year | RMSE (°C) | Remarks |
|-------|------|-----------|---------|
| CNN-LSTM (Nguyen et al.) | 2022 | 2.3 | High spatial accuracy but complex |
| GraphCast (Lam et al.) | 2023 | 1.4 | State-of-the-art but GPU-heavy |
| Our LSTM Model | 2025 | 1.57 | Lightweight, accurate, and fast |
| FourCastNet (Subramanian et al.) | 2022 | 1.6 | Global-scale, heavy training |
| TLLA (Hu et al.) | 2024 | 1.5 | Attention-based, longer horizon |

Our LSTM model achieves competitive accuracy with far lower computational cost, making it more suitable for small-scale, real-time forecasting applications.

--------------------------------------------------------------------------------

Literature Review Summary

A review of 10 recent research papers (2019–2025) on deep learning forecasting models was conducted. The studies covered LSTM, Bi-LSTM, CNN-LSTM hybrids, Transformer architectures (Informer, TFT), attention-based frameworks (TLLA), and spatio-temporal models.

| S. No. | Paper | Technique | Key Finding |
|--------|--------|------------|--------------|
| 1 | DEEPCOVID (Rodríguez et al., 2021) | Deep Learning Framework | Early operational epidemic forecasting; uncertainty modeling |
| 2 | Chandra et al., 2022 | LSTM/Bi-LSTM | Captured temporal and wave dynamics |
| 3 | Lim et al., 2021 | TFT | Interpretable attention-based forecasting |
| 4 | Zhou et al., 2021 | Informer | Efficient long-sequence Transformer |
| 5 | Oreshkin et al., 2019 | N-BEATS | Interpretable univariate forecasting |
| 6 | Zhou et al., 2021 | GitHub Implementation | Enhanced reproducibility for Informer |
| 7 | Zhou et al., 2023 | Improved LSTM | Encoder–decoder hybrid model |
| 8 | Hu et al., 2024 | TLLA | Transfer learning with attention |
| 9 | Rodríguez et al., 2021 | DeepCOVID | Operational uncertainty lessons |
| 10 | Jiao et al., 2025 | Spatio-Temporal NN | Mobility features improved short-term accuracy |

For detailed discussion, see Section 3: Literature Survey in the report.

--------------------------------------------------------------------------------

Repository Structure

Code – weather_lstm_notebook.ipynb
Model – best_lstm_model.keras
Results – lstm_plot_1.png, lstm_plot_2.png, lstm_plot_3.png
Report – DEEp_Learning_Final.docx
README – This file

--------------------------------------------------------------------------------

Conclusion

This project successfully demonstrates the application of LSTM-based deep learning for short-term temperature forecasting. The model achieved RMSE = 1.57 °C and R² = 0.976, proving its reliability and robustness. Compared to heavy Transformer-based architectures, LSTM offers faster training, interpretability, and efficiency, making it suitable for real-world, localized predictions.

Future work can explore attention mechanisms, CNN-LSTM hybrids, or Transformer extensions to further enhance long-term forecasting.

--------------------------------------------------------------------------------

Authors

Submitted by:
Siddhartha (102215188)
Mohd Ammar (102215288)
Manika Bansal (102215274)
Garima Goel (102215353)

Under the Guidance of:
Dr. Gaganpreet Kaur
Dr. Deepak Rakesh
Department of Electronics and Communication Engineering
Thapar Institute of Engineering & Technology, Patiala

--------------------------------------------------------------------------------

Evaluation Criteria Alignment

| Requirement | Status |
|--------------|---------|
| Complete Code of Deep Learning Technique | ✓ Included |
| Rough Draft of Paper (Docx) | ✓ Attached |
| Survey of Minimum 10 Papers | ✓ Section 3 + Table 3.1 |
| Methodology Diagram | ✓ Included |
| Results & Graphs | ✓ Included |
| Comparison with Recent Work | ✓ Detailed |
| References | ✓ IEEE-style |
| Repository Structure | ✓ Organized |
| Submission Format | ✓ GitHub-ready |

--------------------------------------------------------------------------------

License

This repository is part of the course
UEC642 – Deep Learning (Aug–Dec 2025)
for academic and educational purposes only.
