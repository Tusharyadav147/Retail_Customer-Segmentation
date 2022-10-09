## Project Title 
* Retail Customer Segmentation

## Problem Statment
* This project  is about a Superstore which caters to a vast variety of customers. Superstore’s manager has noticed that there are diminishing returns from the existing marketing strategies. Sales from the last 2 quarters have hit a plateau which has started to concern the store manager. 
* Store’s usual marketing campaigns includes unmonitored and untargeted approach which in the last quarter incurred some losses due to which the store manager started to look for areas of improvement. He found that the mass effectiveness of mass campaigns is very low as the cost is too high. The store already has an analytics team which has been collecting household level data from customers in the loyalty program.

## Datasets: Following csv files
* Transactio.csv
* Product.csv
* Promotions.csv
* Demogrpahics.csv
* Coupons.csv
* Coupon_redemption.csv
* Campaign.csv
* Campaign_description.csv

## What are the required python packages?
* Pandas
* Numpy
* Matplotlib
* Seaborn

## 


## Where to download the data?
* Dataset can be downloaded [here](https://exchangelabsgmu-my.sharepoint.com/:f:/g/personal/jyang43_masonlive_gmu_edu/En-TZLF4UVBAqyCtiyQOYM0BU3leFL4TSCJd18xoIXovGA?e=b3LTcq). 

**Note**: Please contact the author Jingchao Yang (jyang43@gmu.edu) for direct access if link expires.
* Place the dataset in the data folder before running the code

**Note**: All data has been preprocessed to csv format, raw data can be accessed from [weather underground](https://www.wunderground.com/) and [GeoTab](https://data.geotab.com/weather/temperature). Toolset for preprocessing raw data can be accessed upon request.

## How to get the results?
### Category of models
* [multistep_lstm](multistep_lstm) indludes python files for LSTM model building and training
* [multistep_others](multistep_others) includes comparison model ARIMA and XGBoost

### 1. LSTM model:
To run our LSTM model, go to the [directory](multistep_lstm) and use the command:

`python run_auto.py`

LSTM was also developed to support transfer learning with command <br>
`python run_auto.py --transLearn`

**Note**: Model training can take much longer time without GPU support. LA Dataset already includes trained models and ready for transfer learning, user can delete the content inside the LA/output to retrain.

Model output will be stored in the data/output folder.

### 2. Other models
Creat result folder under [multistep_others](multistep_others) for model output. ARIMA and XGBoost are for model comparison and were not developed for transfer learning.

#### 2.1 ARIMA
To run our ARIMA model, go to [multistep_others](multistep_others) and use the command <br>
```python auto_arima_run.py```

**Note**: ARIMA does not support any parallelization and can take a long time to finish. To help with the process, a Fast Mode has set to True as default [here](https://github.com/stccenter/IoT-based-Temperature-Prediction/blob/main/multistep_others/auto_arima_run.py#L19), and will only produce a result on randomly selected 3 stations. Change to False to test on the full dataset.

#### 2.2 XGBoost
To run our XGBoost model, go to [multistep_others](multistep_others) and use the command <br>
```python xgboost_run.py```

## Useful links
* Check out the slides [AAG 2021 Presentation](AAG_2021_IoTbased_Fine-scale_Urban_Temperature_Forecasting_Jingchao.pdf) for more project details.
* [Tutorial](https://stackabuse.com/time-series-prediction-using-lstm-with-pytorch-in-python/) for LSTM using pytorch
* [Tutorial](https://www.kaggle.com/sumi25/understand-arima-and-tune-p-d-q) for ARIMA
* [Tutorial](https://www.kaggle.com/furiousx7/xgboost-time-series) for XGBoost

## Author
Jingchao Yang <br>
Email: jyang43@gmu.edu
## Validated by
Anusha Srirenganathan <br>
Email: asrireng@gmu.edu

## Tutorial video <br/>
[<img src="https://github.com/stccenter/IoT-based-Temperature-Prediction/blob/main/data/view/thumbnail.jpg" width="60%">](https://youtu.be/HIrH0976zrY)


