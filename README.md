# Learn to Build an End-to-End Machine Learning Pipeline - Part 3

The aim of Part 3 is to develop an end-to-end machine learning pipeline by implementing model monitoring, CI/CD practices, and Amazon SageMaker Pipelines for improved reliability and efficiency in logistics operations.

## Overview
The project addresses a critical challenge faced by the logistics industry. Delayed truck shipments not only result in increased operational costs but also impact customer satisfaction. Timely delivery of goods is essential to meet customer expectations and maintain the competitiveness of logistics companies. By accurately predicting truck delays, logistics companies can:
- Improve operational efficiency by allocating resources more effectively
- Enhance customer satisfaction by providing more reliable delivery schedules
- Optimize route planning to reduce delays caused by traffic or adverse weather conditions
- Reduce costs associated with delayed shipments, such as penalties or compensation to customers

## Data
The project involves the following data tables:

- City Weather: Weather data for various cities
- Routes: Information about truck routes, including origin, destination, distance, and travel time
- Drivers: Details about truck drivers, including names and experience
- Routes Weather: Weather conditions specific to each route
- Trucks: Information about the trucks used in logistics operations
- Traffic: Traffic-related data
- Truck Schedule: Schedules and timing information for trucks

_Data is not included in this repository._

## Approach
- Setting up Streaming Data Generation: ○ Define functions or scripts to generate streaming data mimicking real-world scenarios ○ Ensure data is representative and diverse to capture various conditions and events
- Lambda Function Creation for Streaming Data:

○   Write Lambda function code to handle incoming streaming data ○   Configure necessary permissions and triggers for Lambda execution ○   Develop Lambda function logic to process and transform streaming data ○   Integrate Lambda functions into the pipeline architecture for seamless data flow
- Docker Image Creation with Python 3.10: ○ Build a Docker image containing the required Python environment and dependencies
- Streaming Data Integration and Pipeline Monitoring: ○ Implement mechanisms for monitoring pipeline, performance, and data quality
- Data Drift and Model Drift Calculation: ○ Implement algorithms to calculate data drift and model drift based on historical and real-time data ○ Monitor deviations in data and model performance for proactive intervention
- Model Retraining and Evaluation: ○ Develop processes for retraining models based on detected drift and updated data
- Scenario-based Runs and Testing: ○ Perform scenario-based runs to simulate different operational conditions and scenarios
- Scheduling SageMaker Pipeline Execution
- Configure scheduling mechanisms to automate the execution of SageMaker pipelines at predefined intervals
- Notification System Setup and Implementation: ○ Configure notification systems to provide alerts and updates on pipeline status and events ○ Integrate notification systems into the pipeline architecture for effective communication and monitoring
- Resource Cleanup Post-execution: ○ Ensure efficient resource management and cost optimization by removing unused or unnecessary resources
- Conclusion: ○ Summarize key findings, insights, and outcomes from the monitoring approach

Code Folder Overview:

Once you unzip the code.zip file, you can find the following folders:

## Tech stack
➔ Language: Python 3.10 ➔ Libraries: NumPy, Pandas, Evidently AI ➔ Data: Hopsworks Feature Store ➔ Experiment Tracking: Weights and Biases ➔ Model Building: Scikit-learn, XGBoost ➔ Cloud Platform: AWS Sagemaker, Amazon SageMaker, AWS Lambda, AWS SNS, AWS CodePipeline, AWS CodeCommit, AWS CodeBuild

## How to run
```bash
pip install -r Code+Folder/Training_Codes/requirements.txt
python Code+Folder/Training_Codes/app.py
python Code+Folder/Training_Codes/engine.py
```
Notebooks: [`sagemaker-pipelines-project.ipynb`](Code+Folder/StreamingData_Sagemaker_Pipeline/sagemaker-pipelines-project.ipynb), [`Truck-Delay-Classification_Part_2.ipynb`](Code+Folder/Training_Codes/notebooks/Truck-Delay-Classification_Part_2.ipynb), [`Truck_Delay_Classification_Part_1.ipynb`](Code+Folder/Training_Codes/notebooks/Truck_Delay_Classification_Part_1.ipynb), [`sample-monitoring_pipeline.ipynb`](Code+Folder/Training_Codes/sample-monitoring_pipeline.ipynb)

## Project structure
```
.gitignore
Code+Folder/
  Lambda_function_streaming_data/
    lambda_streaming_data_gen.py
  Python3.10_docker/
    Dockerfile
  README.md
  StreamingData_Sagemaker_Pipeline/
    calculate_data_drift.py
    calculate_model_drift.py
    feature_engg_finalmerge_hopsworks.py
    fetch_streaming_dump_to_hopsworks.py
    is_first_day_of_week.py
    model_drift_not_detected.py
    model_retraining.py
    not_first_day_of_week.py
    pipeline.py
    previous_data_updation.py
    sagemaker-pipelines-project.ipynb
    test.py
  Training_Codes/
    app.py
    config.yaml
    engine.py
    ml_pipeline/
    notebooks/
    requirements.txt
    sample-monitoring_pipeline.ipynb
  sagemaker_pipeline_notifications_cdk/
    python/
```

## Credits
Based on a ProjectPro guided project.
