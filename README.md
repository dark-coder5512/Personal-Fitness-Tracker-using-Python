# Personal Fitness Tracker

## 1. Objective
The primary objective of this project is to develop an accessible, user-friendly web application that leverages machine learning to accurately estimate the number of calories burned during physical activity. By utilizing physiological data and exercise metrics, the tool aims to assist users in tracking their fitness progress and managing their energy expenditure effectively.

## 2. Problem Statement
Accurately tracking calories burned during exercise is a key component of fitness management and weight loss. However, precise measurement often requires expensive wearable technology or complex laboratory equipment. Many individuals rely on generic estimates that do not account for personal physiological differences, leading to inaccurate tracking and suboptimal fitness planning. There is a need for a cost-effective, software-based solution that can provide personalized calorie estimation based on easily measurable parameters.

## 3. Solution
This project implements a Machine Learning solution using the **Random Forest Regressor** algorithm. The model is trained on a comprehensive dataset containing exercise and physiological data (including Age, Gender, Height, Weight, Duration of exercise, Heart Rate, and Body Temperature).

The solution is deployed as an interactive web application using **Streamlit**, allowing users to input their parameters via a simple interface and receive instant predictions.

## 4. Project Functionality
The Personal Fitness Tracker performs the following functions:

### A. User Input Interface
The application provides a sidebar for users to input specific parameters:
- **Age**: User's age in years.
- **BMI (Body Mass Index)**: Calculated or estimated body mass index.
- **Duration**: Length of the exercise session in minutes.
- **Heart Rate**: Average heart rate during the session.
- **Body Temperature**: Body temperature in Celsius.
- **Gender**: Male or Female.

### B. Calorie Prediction
Upon receiving the input, the pre-trained Random Forest model processes the data to predict the total kilocalories burned. This prediction is displayed prominently on the main dashboard.

### C. Comparative Analysis
The application provides context to the user's data by comparing it with the underlying dataset:
- **Similar Results**: Displays a sample of records from the dataset that have similar calorie burn values.
- **Statistical Benchmarking**: Informs the user how their metrics (Age, Duration, Heart Rate, Body Temp) compare to the population average (e.g., "You have a higher heart rate than 75% of other people").

## 5. Technical Stack
- **Language**: Python
- **Frontend/Framework**: Streamlit
- **Data Manipulation**: Pandas, NumPy
- **Machine Learning**: Scikit-learn (Random Forest Regressor)
- **Visualization**: Matplotlib, Seaborn

## 6. Future Enhancements (Roadmap)
To further strengthen the project, the following updates are proposed:
- **Performance Optimization**: Implementing `@st.cache_resource` to load data and train the model only once, significantly speeding up interaction.
- **Advanced Visualizations**: Adding correlation heatmaps and feature importance charts to show users which factors contribute most to their calorie burn.
- **Health Insights**: Automatically categorizing BMI (e.g., "Healthy Weight", "Overweight") and Heart Rate Zones (e.g., "Fat Burn", "Cardio").
- **Data Persistence**: Adding functionality to save prediction history to a local file to track progress over time.
