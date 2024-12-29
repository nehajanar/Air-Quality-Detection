# AI4ALL Final Project: Hybrid LSTM-Embedding Neural Network for AQI Prediction

This project focuses on predicting the Air Quality Index (AQI) by integrating temporal and categorical data using a hybrid deep learning approach. The model combines **LSTM layers** to process sequential data (e.g., pollutant levels over time) and **embedding layers** to handle categorical features (e.g., state, county, and city). By leveraging this multi-input architecture, the model provides accurate AQI predictions based on historical pollutant levels and meteorological data.

## Skills Applied

- Time-series analysis with LSTM
- Categorical data representation with embedding layers
- Data preprocessing, feature engineering, and scaling
- Deep learning model design and optimization
- Visualization of trends and results

## Program Context

Developed as part of AI4ALL, this project showcases the application of cutting-edge AI techniques to address critical environmental challenges, specifically air quality forecasting.

## Problem Statement

Air pollution significantly impacts public health, the environment, and the economy. Accurate AQI forecasting is essential for enabling informed decisions, mitigating health risks, and guiding policymaking.

### Relevance

- Provides a predictive tool to monitor air quality in real-time.
- Supports public health efforts by forecasting poor air quality days.
- Assists policymakers in designing effective interventions for air pollution control.

## Key Results

1. Processed and merged data from multiple sources into a unified dataset with over 40,000 observations.
2. Built and trained a hybrid LSTM-Embedding Neural Network:
   - Combines temporal patterns and categorical location features for robust AQI prediction.
3. Model Performance:
   - **Mean Absolute Error (MAE):** 8.172
   - **Mean Squared Error (MSE):** 11.675

---

## Methodologies

### 1. Data Collection and Preprocessing

- Downloaded 10 separate feature attribute CSV files from **AQS Data Mart**.
- Merged multiple datasets, condensing 10 features into 3 categories:
  - **Criteria Gases**: Ozone, SO2, CO, NO2
  - **Particulates**: Fine particles (PM2.5), Coarse particles (PM10)
  - **Meteorological Features**: Wind, Temperature, Barometric Pressure, Relative Humidity, and Dewpoint
- Connected with output feature AQI values to create a complete dataframe.

### 2. Feature Engineering

- Scaled features using `MinMaxScaler`.
- Created time-series input sequences with a 30-day rolling window for temporal data.

### 3. Model Architecture

- **Temporal Input**:
  - Stacked LSTM layers to capture sequential patterns in AQI and pollutant data.
- **Categorical Input**:
  - Embedding layers to represent state, county, and city as dense vectors.
- **Fusion**:
  - Combined temporal and categorical features through concatenation.
- **Dense Layers**:
  - Fully connected layers refine features for AQI prediction.

### 4. Training

- Trained the hybrid model using TensorFlow and Keras.

### 5. Evaluation

- Evaluated the model on a separate test dataset.
- Visualized actual vs. predicted AQI values for validation.

## Data Sources

- [AQS Data Mart (EPA)](http://aqs.epa.gov/aqsweb/airdata/download_files.html#AQI): Comprehensive pollutant and meteorological data for air quality monitoring.

## Technologies Used

- **Programming Languages:** Python
- **Deep Learning Frameworks:** TensorFlow and Keras
- **Data Processing**: Pandas, NumPy, scikit-learn
- **Visualization:** matplotlib, seaborn, folium
- **Geospatial Analysis:** folium (interactive maps)

## Authors

*This project was completed in collaboration with:*
- **Uyen Nguyen** ([nguyen_u1@denison.edu](mailto:nguyen_u1@denison.edu))
- **Neha Janardhan** ([njanardhan@umass.edu](mailto:njanardhan@umass.edu))
- **Nurbu Lama** ([laman1@montclair.edu](mailto::laman1@montclair.edu))
- **Ignacio Ruiz** ([iruiz047@fiu.edu](mailto::iruiz047@fiu.edu))

