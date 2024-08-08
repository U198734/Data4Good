# Weather Data and Accident Prediction Project

## Project Overview

In this project, we utilize the **DWD Weather Data East Germany API** to access accurate and up-to-date meteorological data for eastern Germany. This API provides detailed weather information such as temperature, precipitation, wind speed, and more. Integrating this API enhances the accuracy and functionality of our applications or analyses related to weather in this region.

## Data Utilization

### Observations
From the dataset provided, we focus on variables from 2021, as it aligns with the dataset's time frame. Specifically, we have observed that only a few variables have values. Therefore, we use the most relevant ones for our study: **'sunshine'** and **'precipitation'**. The process for obtaining meaningful data is detailed in the code `Data4Good_1.ipynb`.

### Data Preparation
In `Datapreparation.ipynb`, we:
- Merged datasets
- Removed irrelevant variables
- Focused on a subset of the input data, specifically accidents near sensors in Berlin

## Deep Learning Model

### Model Development
We developed a Deep Learning model using a **Multilayer Perceptron (MLP)** to predict accident probabilities. The model uses the sigmoid activation function to yield values between 0 and 1. Key steps include:

- **Handling Dimensionality Issues**: Adjusted dimensions to ensure they do not affect the final values.
- **Training**: Performed forward and backpropagation, calculating the loss function using Binary Cross Entropy. PyTorch was utilized for efficient computation and automatic backpropagation.

### Analysis and Application
Once we have the predicted probabilities:
- **Python Script**: Created to associate accident probabilities with coordinates (latitude and longitude) in Berlin.
- **Heatmap Creation**: Developed an interactive graphical interface to visualize accident probabilities, allowing zooming and highlighting high-risk areas.

## Real-Time System Architecture

To ensure real-time usability, we designed a system architecture that:
- Periodically sends data for automatic execution
- Integrates three information sources: **Police**, **Sensors**, **Weather**
- Uses **Kafka Data Brokers** to manage data flow between Python scripts and the deep learning model
- Generates a heatmap of accident probabilities to improve safety and traffic management in Berlin

## Scalability
The system is designed to be scalable, capable of handling large volumes of data and adapting to various scales of application.

## Conclusion
This project demonstrates the potential of combining weather data and deep learning to enhance traffic safety through real-time prediction and visualization. We hope these resources and tools will be valuable for those interested in similar data mining and predictive analytics applications.

Happy exploring!

