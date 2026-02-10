# Data Generation Using Simulation for Machine Learning  
## Predicting CartPole Stability Using OpenAI Gym

---

## Project Overview
This project demonstrates how **simulation-based data generation** can be used to create datasets for **machine learning** tasks.  
A physics-based simulator is used to generate synthetic data, which is then used to train and evaluate multiple **supervised regression models**.

The goal is to learn how well different ML models can predict system behavior from simulated environments.

---

## Problem Statement
Predict the **stability duration** of a CartPole system based on its **initial physical state**.

- Given the initial state of the CartPole system, predict how long the pole remains balanced.
- Stability duration is measured using the **total episode reward**, which corresponds to the number of time steps before failure.

---

## Simulator Used
- **OpenAI Gym – CartPole-v1**

---

## Dataset Description

### Input Features
Each data point consists of the initial state returned by the simulator:
- Cart position  
- Cart velocity  
- Pole angle  
- Pole angular velocity  

### Target Variable
- **Episode reward** (proxy for stability duration)

### Dataset Size
- **1000 simulation episodes**

---

## Machine Learning Task
The generated dataset is used to train and evaluate multiple **regression models** under identical conditions.

### Models Evaluated
- Linear Regression  
- Ridge Regression  
- K-Nearest Neighbors (KNN)  
- Decision Tree Regressor  
- Random Forest Regressor  
- Gradient Boosting Regressor  

---

## Evaluation Metrics
Model performance is evaluated using:
- Mean Absolute Error (MAE)  
- Root Mean Squared Error (RMSE)  
- R² Score  

These metrics measure prediction accuracy and how well each model explains variance in stability duration.

---

## Key Results & Observations
- **Nonlinear models** (KNN and tree-based ensembles) significantly outperform linear models.
- Linear regression performs poorly due to the **highly nonlinear and chaotic dynamics** of the CartPole system.
- **KNN achieved the best overall performance**, indicating strong local nonlinear relationships in simulation-generated data.
- The results highlight the importance of **model selection** when learning from simulator-based datasets.

---

## Author
**Ishan Bhat**  
**Roll No:** 102313022


