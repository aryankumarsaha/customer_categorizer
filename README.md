Customer Personality Segmentation
Problem Statement
This project aims to build a machine learning system that predicts customer personality segments. It’s useful for malls, stores, and product-based companies. By analyzing customers' personal and purchase data, we can group them into clusters and predict their segment using classification techniques.

Proposed Solution
To predict customer clusters dynamically, we use machine learning. First, we cluster customers based on existing data and domain knowledge. Then, we train models to predict which cluster a new customer belongs to, leveraging historical customer data.

Tech Stack Used
Python

FastAPI

Machine Learning algorithms

Docker

MongoDB

How to Run
Make sure you have a MongoDB Atlas account and have uploaded the shipping dataset.

Create and activate a conda environment:

bash
conda create --prefix venv python=3.7 -y  
conda activate venv/
Install dependencies:

bash
pip install -r requirements.txt
Set environment variables:

bash
export AWS_ACCESS_KEY_ID=<your_aws_access_key>  
export AWS_SECRET_ACCESS_KEY=<your_aws_secret_key>  
export AWS_DEFAULT_REGION=<your_aws_region>  
export MONGODB_URL=<your_mongodb_connection_string>
Run the app server:

bash
python app.py
Start training on: http://localhost:5000/train

Make predictions on: http://localhost:5000/predict

Run Locally with Docker
Make sure Dockerfile is in the project directory.

Build Docker image:

bash
docker build --build-arg AWS_ACCESS_KEY_ID=<aws_key> --build-arg AWS_SECRET_ACCESS_KEY=<aws_secret> --build-arg AWS_DEFAULT_REGION=<region> --build-arg MONGODB_URL=<mongo_url> .
Run Docker image:

bash
docker run -d -p 5000:5000 <image_name>
Project Architecture
(Include your architecture diagrams here as images)

Models Used
K-Means clustering for grouping customers

Logistic Regression for predicting customer segment

Hyperparameter tuning with GridSearchCV for optimal model performance

Project Structure
The main folder src contains:

Data Ingestion

Data Validation

Data Transformation

Data Clustering

Model Training

Model Evaluation

Model Deployment

Custom logging and exception handling are implemented for easier debugging.

Conclusion
This project can be leveraged by businesses to improve customer targeting based on predicted personality segments.

This version is more conversational, clear, and easy to follow while retaining all essential details and instructions.
