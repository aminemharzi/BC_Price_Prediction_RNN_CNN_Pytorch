# Time Series Regression with PyTorch

This project implements a time series regression model using PyTorch to predict values from historical data. The dataset contains cryptocurrency price information (e.g., Bitcoin) and the goal is to predict future values based on historical features.

## Project Structure

- **Dataset**: A CSV file (`gemini_BTCUSD_2020_1min.csv`) containing cryptocurrency price data.
- **Notebook**: A single Jupyter Notebook (`time_series_regression.ipynb`) that contains all the code for preprocessing, model training, evaluation, and visualization.

---

## Requirements

The following Python libraries are required:

```bash
numpy
pandas
matplotlib
torch
scikit-learn
jupyter
```

You can install the dependencies using:
```bash
pip install numpy pandas matplotlib torch scikit-learn jupyter
```

---

## Files and Directories

- **`data/`**: Contains the dataset file `gemini_BTCUSD_2020_1min.csv`.
- **`time_series_regression.ipynb`**: The main Jupyter Notebook containing all the project code.
- **`README.md`**: Project documentation (this file).

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. Ensure that the dataset (`gemini_BTCUSD_2020_1min.csv`) is located in the `data/` directory.

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

4. Open the `time_series_regression.ipynb` notebook.

5. Run the cells sequentially to:
   - Preprocess the data using `MinMaxScaler`.
   - Train the model (RNN or CNN).
   - Evaluate the model on validation and test sets.
   - Plot training, validation, and test losses.

---

## Model Architectures

### Recurrent Neural Network (RNN)
- Two GRU layers.
- Final dense layer for output prediction.

### Convolutional Neural Network (CNN)
- Two `Conv1d` layers for feature extraction.
- GRU layers for sequential learning.
- Final dense layer for prediction.

---

## Data Preprocessing

1. Load the dataset using Pandas.
2. Drop unnecessary columns.
3. Normalize the data using `MinMaxScaler`.
4. Use sliding windows to create sequences for training, validation, and testing.

---

## Training

- Optimizer: Adam
- Loss Function: Mean Squared Error (MSE)
- Metrics: MAE, RMSE, R², MAPE
- Epochs: 10 (configurable)
- Steps per epoch: 40

---

## Evaluation Metrics

- **Mean Squared Error (MSE)**: Penalizes large errors heavily.
- **Mean Absolute Error (MAE)**: Average absolute error between predictions and targets.
- **Root Mean Squared Error (RMSE)**: Square root of MSE, in the same unit as the target variable.
- **R² (R-Squared)**: Measures how well the model explains the variance in the target variable.
- **Mean Absolute Percentage Error (MAPE)**: Error as a percentage of the true value.

---

## Results

- Training, validation, and test loss are printed during training.
- Loss curves are plotted at the end of training for visualization.

---

## Future Improvements

- Incorporate advanced architectures like LSTMs or Transformers.
- Experiment with hyperparameter tuning.
- Use additional features (e.g., trading volume) for better predictions.
- Extend the model to predict multiple time steps ahead.

---

## License

This project is licensed under the MIT License. Feel free to use and modify the code.

---

