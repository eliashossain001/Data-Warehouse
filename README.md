# E-commerce Data Analysis
Author: Elias Hossain (Graduate Student) <br>
Department of Electrical & Computer Engineering (ECE) <br>
North South University, Dhaka <br>

# Purpose of the Notebook
This project is focused on performing data analysis on an e-commerce dataset using Python and PostgreSQL. The dataset includes information about transactions, customers, items, time, and stores. 
The purpose of the notebook is to showcase how to execute OLAP queries using SQL and Python, and how to load the results into pandas dataframes. Additionally, the notebook would demonstrate how to visualize the data using matplotlib. Specifically, the notebook would focus on answering the given questions 
about the ecomdb warehouse using simple and complex CUBE queries, and present the results in a clear and organized manner. However, this notebook is created as a part of the assignment of the CSE512-Distributed Database Management System (DBMS)

# Instructions for Running the Notebook

To run this notebook, make sure you have Python 3 installed on your system along with the necessary packages such as NumPy, Pandas, Scikit-learn, and Matplotlib. You can install these packages using the following command:

```
pip install numpy pandas scikit-learn matplotlib
```
Once the required packages are installed, you can open the notebook in Jupyter Notebook or JupyterLab and run each cell in sequence to execute the code and see the results. You can clone this repository by following the command:

```
git clone https://github.com/eliashossain001/Data-Warehouse.git

```
# Project Setup
1. Install Python 3.8 or higher
2. Install PostgreSQL
3. Clone this repository
4. Create a virtual environment: python -m venv env
5. Activate the virtual environment: source env/bin/activate
6. Install the required packages: pip install -r requirements.txt
7. Create a PostgreSQL database and configure the database connection
8. Load the dataset into the database using PostgreSQL queries


# Dataset
The dataset used in this project is located in the data folder and consists of the following tables:

* fact_table: contains information about transactions such as payment key, customer key, time key, item key, store key, quantity, unit, unit price, and total price.
* trans_dim: contains information about transactions such as payment key, transaction type, and bank name.
* item_dim: contains information about items such as item key, item name, description, unit price, manufacturer country, supplier, and unit.
* customer_dim: contains information about customers such as customer key, name, contact number, and national ID.
* time_dim: contains information about time such as time key, date, hour, day, week, month, quarter, and year.
* store_dim: contains information about stores such as store key, division, district, and upazila.

# Data Analysis
The OLAP_Analytics file contains functions to perform various types of data analysis on the dataset. These include:

* Sales by Payment Type: a bar chart that shows the breakdown of sales by payment type over a specified range of time.
* Sales by Item: a pie chart that shows the breakdown of sales by item over a specified range of time.
* Sales by Customer: a bar chart that shows the breakdown of sales by customer over a specified range of time.
* Sales by Time: a line chart that shows the trend in sales over a specified range of time.
* Sales by Store: a bar chart that shows the breakdown of sales by store over a specified range of time.


# Sales Forecasting
The sales_forecasting notebook contains the predictive modeling for this project. It uses the pandas, numpy, matplotlib, statsmodels, and sklearn libraries.

# ARIMA Model
The ARIMA model is used to forecast the one year sales (breakdown monthly) for each item. The ARIMA class from the statsmodels.tsa.arima_model module is used to fit the model to the data and generate forecasts.

# Linear Regression Model
The linear regression model is used to forecast the sales of the stores for the next 30 days. The LinearRegression class from the sklearn.linear_model module is used to fit the model to the data and generate forecasts.

# Results
The forecasts generated by the ARIMA and linear regression models are stored in separate tables in the ecom_schema schema of the PostgreSQL database.

# ARIMA Model Results
The arima_forecasts table contains the one year sales forecasts (breakdown monthly) for each item.

# Linear Regression Model Results
The lr_forecasts table contains the sales forecasts for each store for the next 30 days.

# Usage
To run the sales_forecasting.py script, you'll need to have the following software installed:

1. Python 3.x
2. PostgreSQL

# Acknowledgements:

I would like to express my sincere gratitude to Dr. Abu Sayed Md. Latiful Hoque, the course instructor of CSE512 at North South University, for assigning this project and providing valuable guidance throughout the project. I am also thankful to the eSystems Research and Development Lab, Dept. of CSE, Bangladesh University of Engineering & Technology (BUET), led by Dr. Abu Sayed Md. Latiful Hoque for their innovative and impactful research contributions in the field of Health and Education.

I would also like to extend my appreciation to Md Jahedul Islam, a research assistant in the lab, for providing me with project setup guidance and continuous support throughout the project.

