<p align="center">
  <img src="your_project_logo.png" alt="Time Series Forecasting Pipeline" width="400"/>
</p>

<h1 align="center"> 📈 Automated Time Series Forecasting Pipeline 📈</h1>

<p align="center">
  <strong>A Python-based pipeline leveraging Greykite for robust time series forecasting.</strong>
</p>

<p align="center">
  <a href="https://github.com/your-username/your-repo">
    <img src="https://img.shields.io/github/license/its-amann/Automated-Time-Series-Forcasting.svg" alt="License">
  </a>
  <a href="https://github.com/your-username/your-repo/issues">
    <img src="https://img.shields.io/github/issues/its-amann/Automated-Time-Series-Forcasting.svg" alt="Issues">
  </a>
  <a href="https://github.com/your-username/your-repo/stargazers">
    <img src="https://img.shields.io/github/stars/its-amann/Automated-Time-Series-Forcasting.svg" alt="Stars">
  </a>
</p>

---

## 🚀 Overview

Welcome to the **Automated Time Series Forecasting Pipeline**, a sophisticated and **highly adaptable** application designed to simplify and automate the process of time series forecasting. This pipeline utilizes the power of the Greykite library, providing you with a robust and accurate forecasting solution for diverse datasets. Whether you are analyzing energy consumption, sales data, or any other time-dependent variable, this pipeline will provide you the tools necessary to make precise predictions.

✨ **Key Highlights:**
- **Automated Model Selection:** Leverages Greykite's advanced algorithms to automatically select the best-performing model for your data.
- **User-Friendly Interface:** Utilizes clear prompts to obtain the necessary parameters to create the best model for your specific data
- **Robust and Accurate Forecasting:** Incorporates multiple growth terms, seasonal components, event modeling, changepoint detection, and autoregression.
- **Customizable Regressors:** Easily add and process external regressors to enhance forecast accuracy.
- **Comprehensive Evaluation:** Includes thorough cross-validation to ensure the reliability of the forecasts.
- **Seamless Data Integration:** Supports various data frequencies, including daily, hourly, or any time series data
- **Easy to use:** Once the code is correctly configurated, just uploading your data, running the model and it will provide you with your forecast in a CSV file

<p align="center">
  <img src="system_architecture.png" alt="System Architecture" width="600"/>
</p>

<h3 align="center">
    The diagram above shows the general workflow of the forecasting pipeline.
    The user provides the data and its parameters through the command line interface,
    the Greykite library processes the data using several techniques,
    and the forecast is outputted in a CSV file, also with its respective plots.
    
</h3>

---

## 🛠 Features

- **Automated Data Loading:** Loads historical time series data with user-defined time series and date variable.
- **Future Data Integration:** Seamlessly integrates future data for forecasting.
- **Dynamic Parameter Input:** Allows the user to enter parameters like the time series, the date column, country code, regressors, and forecasting horizon
-   **Frequency Detection:** Automatic data frequency detection and use for proper model implementation
-   **Automatic Data Cleaning**: Removes non-alphanumeric characters from the time series and regressor columns.
-   **Dynamic Regressor Handling:** Validates, incorporates, and auto-lags relevant regressor columns into the model.
-   **Model Component Specification:** Configures the model components including growth terms, seasonality, events, changepoints, autoregression, and custom fit algorithms.
-   **Cross-Validation Setup:** Implements a robust cross-validation strategy to evaluate model performance and stability.
-   **Forecast Output:** Generates a CSV file with the forecast that can easily be integrated into other programs.
-   **Backtesting Plots:** Produces visualizations of the backtesting results for validation and analysis.
-   **Tabular Results:** Summarizes cross-validation metrics using tabulate, providing easy readability

---

## 📸 Screenshots

<p align="center">
  <img src="data_preview.png" alt="Data Loading and Preview" width="600"/>
</p>

<h2 align="center">
    Data Loading and Preview
</h2>

<p align="center">
  <img src="parameter_inputs.png" alt="User-Defined Parameter Inputs" width="600"/>
</p>

<h2 align="center">
    User-Defined Parameter Inputs
</h2>

<p align="center">
  <img src="forecast_output.png" alt="Forecast Output in a CSV File" width="600"/>
</p>
    
<h2 align="center">
    Forecast Output in a CSV File
</h2>

<p align="center">
  <img src="backtesting_plots.png" alt="Backtesting Plots" width="600"/>
</p>

<h2 align="center">
   Backtesting Plots
</h2>

<p align="center">
  <img src="tabular_results.png" alt="Cross-Validation Results" width="600"/>
</p>

<h2 align="center">
   Cross-Validation Results
</h2>

---

## 🔧 Installation

### Prerequisites

- **Python 3.x** installed on your machine. [Download Python](https://www.python.org/downloads/)
- **Google Colab or Jupyter Notebook** (recommended).
- **pip** (Python package installer)

### Steps

1.  **Clone the Repository:**


`
git clone https://github.com/your-username/your-repo.git
cd your-repo
`

2.  **Install Greykite and other Libraries:**

   Open your Google Colab or Jupyter Notebook and install the following libraries

```bash
pip install greykite
pip install tabulate
```
3. **Upload your data:**

    Upload two CSV files into the current working directory, which will be the same folder where the notebook is placed:

    - One CSV file with the historical time series data and all the regressor columns
    - Another CSV file with the future regressor values and no time series values, since those will be generated by the model

4.  **Run the notebook:**
    -   Run the notebook cells sequentially
    -   The code will prompt you for different parameters for building the model, please fill them correctly based on your data
    -   The forecast will be saved in a file called "forecast_silverkite.csv"
    -   Plots of the backtesting process will be shown

---

## 💻 Usage

Upon running the notebook, you will be prompted with a series of questions. It is important to introduce the proper parameters to ensure a correct model building:

### User Inputs:
1.  **Time series variable:** Enter the name of the column in your dataset that contains the target time series you want to forecast.
2.  **Date Variable:** Enter the name of the column in your dataset that contains the date or time information. The format should be interpretable by pandas.
3.  **Country Code:** Enter the country code for holiday lookup (e.g., `US` for United States, `BE` for Belgium, etc.). This is used to include specific country holidays for the model
4.  **Regressor Columns:** Enter the names of the columns that contain regressors, separated by commas (e.g., `Temperature, Marketing, Promotions`). These must be numeric columns.
5.  **Forecasting Horizon:** Enter the number of future periods you want to forecast (e.g., 24 for hourly forecasting or 31 for daily forecasting)

### Steps:
1.  **Load your data:** Load the data in CSV format to the designated location on your Google Drive or Jupyter Notebook.
2.  **Set Parameters:**  Introduce the parameters requested by the code as per your data
3.  **Run the model:** The model will automatically run after the data has been loaded and its parameters introduced
4.  **Generate Forecast:** After the model finishes running, the forecast can be found in the "forecast\_silverkite.csv" file

---

## ⚙️ Codebase Overview

This project is organized into a single Python notebook. Here's an overview of the main sections:

### Library Imports
The notebook starts by importing essential libraries:
-   `pandas`: Data manipulation and analysis.
-   `numpy`: Numerical operations.
-   `matplotlib.pyplot`: Plotting and visualization.
-   `re`: Regular expression operations for text cleaning.
-   `plotly.offline`: Interactive plotting.
-   `greykite`: The main forecasting library.
-   `tabulate`: To print cross-validation results in a tabular format

### Data Loading and Processing
-   The code loads historical and future CSV files using `pd.read_csv()` and prints the head of the historical data.
-   It prompts the user to input necessary parameters through a command line interface.
-   It infers the time series frequency, identifies the training end date, and merges the historical data and future data
-   The date column is converted to datetime and is set as the index for proper frequency inference.
-   The time series and regressor columns are cleaned by removing non-alphanumeric characters, for better data processing.

### Greykite Configuration
-   **Metadata:** The code initializes the metadata parameters of the data, such as the time column, value column, and frequency
-   **Model Components:** Model components including growth terms, seasonality, events (holidays), changepoints, regressors, autoregression, and custom fit algorithms are configured using `ModelComponentsParam`
-   **Cross-Validation:** The code also configures cross-validation settings using `EvaluationMetricParam` and `EvaluationPeriodParam`
-   **Valid Regressors:** The code validates and incorporates numeric regressor columns, discarding any invalid ones, and informs the user of these steps.
-  **Model:** The Greykite model is built and trained according to the introduced parameters and with the data

### Model Training and Evaluation
-   The forecasting model is trained and the results are obtained using a `Forecaster` and `run_forecast_config` methods
-   Cross-validation results are summarized using `summarize_grid_search_results` and the results are formatted using `tabulate`
-   Backtesting plots are generated through the `plot` method
-   The final forecast is saved to a CSV file, using the `to_csv` method.

### Design Choices
-   **Automation:** The automation is prioritized through the use of the Greykite library, as well as the automation of data frequency detection
-   **User-Friendliness:** The user-friendly interface allows for the data and parameter introduction using a clear and simple command-line interface
-   **Robustness:** Robustness is ensured through automated data cleaning and data validation, as well as cross-validation and backtesting plots

---

## 🤝 Contributing

1. **Fork the Project**
2. **Create your Feature Branch:** `git checkout -b feature/AmazingFeature`
3. **Commit your Changes:** `git commit -m 'Add some AmazingFeature'`
4. **Push to the Branch:** `git push origin feature/AmazingFeature`
5. **Open a Pull Request**

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 💡 Acknowledgments

- This project uses the Greykite library, developed by the LinkedIn team.
-   The open-source community for providing all the necessary libraries for this project to work.
-   Special thanks to all the mentors and instructors for their guidance and support.

<p align="center">
  Made with ❤️ by Aman
</p>
```
