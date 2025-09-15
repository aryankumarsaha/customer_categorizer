# Customer Personality Segmentation
## Problem statement
In this data science project, we will build a machine learning system which will be able predict the personality of the customer using machine learning algorithms. This project will be very usefull for malls, various stores and companies which are product based. Based on customer's personal details and purchase details, we can cluster them and we can predict the customer's cluster number using classification techniques.
## Solution Proposed
Now the question is how to dynamically predict the cluster of the customer ?. One of the approaches which we can use of machine learning approach, where we can cluster the customer based on the details we have and predict the cluster type based on the domain knowledge and leverage previous customer data to predict the cluster.
## Tech Stack Used
1. Python
2. FastAPI
3. Machine learning algorithms
4. Docker
5. MongoDB
## How to run
Before you run this project make sure you have MongoDB Atlas account and you have the shipping dataset into it.
Step 1. Create a conda environment.
```
conda create --prefix venv python=3.7 -y
```
```
conda activate venv/
```
Step 2. Install the requirements
```
pip install -r requirements.txt
```
Step 3. Export the environment variable
```bash
export AWS_ACCESS_KEY_ID=<AWS_ACCESS_KEY_ID>
export AWS_SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>
export AWS_DEFAULT_REGION=<AWS_DEFAULT_REGION>
export MONGODB_URL= <MONGODB_URL>
```
Step 4. Run the application server
```
python app.py
```
Step 5. Train application
```bash
http://localhost:5000/train
```
Step 6. Prediction application
```bash
http://localhost:5000/predict
```

## `src` is the main package folder which contains

**Components** : Contains all components of Machine Learning Project
- Data Ingestion
- Data Validation
- Data Transformation
- Data Clustering
- Model Trainer
- Model Evaluation
- Model Pusher
**Custom Logger and Exceptions** are used in the Project for better debugging purposes.
## Conclusion
- This Project can be used in real-life by Users.



