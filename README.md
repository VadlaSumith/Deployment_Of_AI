# Group E: Customer Feedback Sentiment Analysis

## Project Overview

This project is part of the Retail Industry Project module, where the objective is to develop an AI system that analyzes customer feedback (such as reviews and comments) to determine sentiment (positive, negative, neutral). The system aims to provide insights into customer satisfaction and identify areas for improvement in products and services. By leveraging Natural Language Processing (NLP) and machine learning models, the project delivers actionable insights to enhance the retail experience.
Setup Instructions

## 1. Prerequisites
**Python** (version 3.8 or later)

2. Setup Environment
Clone the repository:
bash
Copy code
git clone https://github.com/GroupE/Sentiment-Analysis.git
Create a virtual environment and install dependencies:
bash
Copy code
python -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
pip install -r requirements.txt
Set up the MySQL database:
Create the database schema using the provided SQL file in the Data folder.
Configure your database credentials in config.py.
3. Running the Project
Data Preprocessing: Run the preprocessing script to clean and prepare the dataset:
bash
Copy code
python source/data_preprocessing.py
Model Development: Train the sentiment analysis model:
bash
Copy code
python source/model_training.py
Deployment: Use Ansible playbooks located in the Deployment folder to automate deployment.
Usage Guide

Running Scripts
Data Preprocessing: Processes raw customer reviews from the dataset, including cleaning, sentiment labeling, and transformation.
Command:
bash
Copy code
python source/data_preprocessing.py
Input: Raw dataset (amazon_uk_shoes_reviews.csv) stored in the Data folder.
Output: Cleaned and labeled dataset (cleaned_reviews.csv).
Model Training: Builds and trains models like Naive Bayes and LSTM for sentiment analysis.
Command:
bash
Copy code
python source/model_training.py
Input: Processed dataset from the previous step.
Output: Trained models stored in the Models folder.
Deployment: Use Ansible scripts to deploy models and set up environments.
Command:
bash
Copy code
ansible-playbook -i hosts.ini deploy.yml
Notes for Contributors
All contributions should follow the branching model (main, development, and feature branches) as specified in the GitHub repository.
Ensure test cases are written for each new feature using PyTest, and add them to the Tests folder.
Update the README.md and documentation files with any new changes or setup requirements.
Folder Structure Explanation

Documentation:
Contains planning and design documents, including:
Requirements document detailing the goals and objectives of the sentiment analysis project.
Design specifications explaining the architecture, model choices, and processing pipeline.
Project plan with milestones and timelines visualized using Gantt charts.
Data:
Holds both raw and processed datasets:
amazon_uk_shoes_reviews.csv: The original dataset used for customer feedback analysis.
cleaned_reviews.csv: The cleaned and labeled dataset used for model training.
Source:
Contains implementation scripts:
data_preprocessing.py: Script for cleaning and labeling the dataset.
model_training.py: Script for building and training the sentiment analysis model.
Other helper scripts for visualization, evaluation, and deployment.
Deployment:
Ansible playbooks and Jenkins configuration files for setting up and managing the testing, staging, and production environments.
README:
This file provides a comprehensive guide on the project, including setup instructions, usage guides, and explanations of the folder structure.
