# F1 Race Pace Prediction Project

## Overview
This project focuses on predicting race pace for each Formula 1 driver based on practice and qualifying data. The goal is to provide a forecast of each driver's performance during the race, with continuous model updates as new race weekends unfold.

## Project Structure and Workflow
1. **Data Sources**: 
   - The model uses data from **practice sessions (FP1, FP2, FP3)** and **qualifying sessions**. 
   - Data is sourced using the `fastf1` Python library, which provides detailed information about each session.
   - The dataset spans **2022 through 2024** and is updated after each race weekend.

2. **Model Training**:
   - The model is trained on **practice and qualifying data**, with the **race data** serving as the target variable.
   - After each weekend, new data is incorporated, and the model is retrained, ensuring that it remains up-to-date and reflects the latest trends in driver and team performance.

3. **Prediction and Reporting**:
   - After the qualifying session each weekend, the model generates race pace predictions.
   - The predictions are presented alongside a **qualitative description** of the weekend, accounting for variables not captured by raw data, such as penalties or changes to grid positions.
   - After the race, **post-race analysis** is conducted, including a comparison between predicted and actual results, visualized through plots, and an **error calculation** to assess prediction accuracy.

4. **Code Execution**:
   - **Data collection and preprocessing** are handled locally. This includes cleaning and structuring race data for model input.
   - The **model training and prediction** computations are performed in Google Colab, leveraging cloud resources for faster processing.

## Tools and Libraries
- **Python**
- **fastf1** for data extraction from F1 sessions
- **Keras** and **TensorFlow** for building and training the machine learning model
- **Matplotlib** and **Seaborn** for data visualization
- **Colab** for cloud-based model training and predictions

## Data Description
- The project uses a comprehensive dataset for each F1 race weekend, including:
  - **Practice session lap times**
  - **Qualifying session lap times**
  - **Race results** (target variable)
  - Data is continually updated after each weekend.

## Usage
To run this project locally, you will need to:
1. Clone the repository.
2. Install the necessary Python libraries by running:

    ```bash
    pip install -r requirements.txt
    ```

3. Run the data collection script to gather data from the latest F1 weekend:

    ```bash
    python collect_data.py
    ```

4. Use the Colab notebook to train the model and generate predictions.

## Reporting and Visualization
- After every race, a **visual report** will be generated, showing the model's predictions vs actual race results.
- The report includes:
  - Plots of predicted vs actual lap times for each driver.
  - An error analysis showing the model's prediction accuracy.

