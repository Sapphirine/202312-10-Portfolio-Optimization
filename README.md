# 202312-10-Portfolio-Optimization
The system is developed to automatically make stock holding recommendation each day before the trading hours. 
The recommendation is shown daily prior to the trading hours in a webpage that the user can access. 
The performance of the past recommendation is also shown against S&P 500 performance.

File #1:
EECS_6893_final_proj_shared_v1.ipynb was used to choose the best machine learning model to predict stock returns out of XGBoost, LSTM, and Random Forest. XGBoost was determined to be the best model for the system.

File #2:
final_eecs6893_port_opt_airflow_v2.py was used to run on the airflow including the following steps:

(1)  download the data from sources   
(2)  fit the machine learning model (XGBoost) and make the 1 day ahead prediction   
(3)  pull the news feed from finnhub and feed it into finBert   
(4)  run the weight recommendation based on Black-Litterman model   
(5)  send the report files to Google Cloud databucket for report shown in the website   
(6)    delete intermediate dataframes and files   
(7)    The report is shown on the website   

Files #3: files in the Website folder were used to show the report on the website

File #4: final_eecs6893_port_opt_history_test.ipynb was used to run historical data test for the recommendation system (recommendations, sentiment distribution, and performance metrics--returns, std, Sharpe-ratio)
