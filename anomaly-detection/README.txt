Anomaly Detection 

The purpose of this project is to explore how different machine learning models can be chained together to detect various malicious behavior. 


### DATA ###

Data set was source from https://registry.opendata.aws/cse-cic-ids2018 and more documentation can be found at https://www.unb.ca/cic/datasets/ids-2018.html

The data files are not on github as these .parquet files range in size form 50 MB to 100 MB. 

The flow data for each kind of attach (two days/files per attack) are in Apache Parquet format: https://parquet.apache.org


### METHOD ###

Initially a Jupyter Notebook was developed for one dataset, the Botnet data. After typical exploratory data anlysis steps, a range of models were tested. XGBoost (XGB) was identified as a clear winner in terms of performance. Most models performed above an F1 score of 99, yet XBG finished a fraction of the time of the other model. Working through this process can viewed in the anomaly_botnet notebook. 

The subsequent *_anomay notebooks would be more lean in terms of EDA and model testing. Once XGB was a identified as a winner in all data sets, hyper-paramter tuning was added to each notebook for that typs of attack. 

The judge notebooks trains the inference models that will give a best guess on if there is an attack or not. If the data is identified as benign then the data will not be used. If an attack is identified in the data  it will feed that into each of the models and whichever has the higher school, that attack will be chooses as the identified attack. 


### References ##

Everything in these notesbooks are my ideas, and not of my classes or of where I work. I did do the inital coding. However, in terms of efficiency I did ask an LLM to refactor and comment out my code as it saves a huge amount of time. 