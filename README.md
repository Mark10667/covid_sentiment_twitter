This thesis project built a practical and industry-level data pipeline from the very beginning of data sources to the analytical output at the end. Throughout this process, we experimented with several kinds of modern state-of-the-art technologies, including Kafka, Cloud, and Transformers in deep learning, to produce our final analytical results. 

<img width="678" alt="senior_thesis_pipeline" src="https://github.com/Mark10667/covid_sentiment_twitter/assets/33364324/022d313e-8280-4e02-8817-bb2ae3e3c77c">

Figure 1. Data Pipeline Structure 

We extracted tweets IDs about Covid from an IEEE Covid database [18]. Each day’s tweet IDs about Covid are saved into a CSV file. We used Kafka to read and filter data from csv files to the cloud. (This part can be done by a Kafka sink-connector. However, in our case, data is in separate CSV files instead of streaming through the pipeline. We can directly upload cleaned CSV files to the cloud)
On the cloud, we explicitly stored structured tweet data in BigQuery. In order for it to be stored in BigQuery, we need to store it in a cloud storage bucket first. 
After we’ve accumulated enough data, it’s time to do data analysis. In this project, we read BigQuery into a Pandas dataframe on a local Jupyter notebook to write complex code for analysis and visualization in Python. This entire part can certainly be done on the Cloud as well, which utilizes cloud computing power. 
