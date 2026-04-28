# Fraud Detection System (Full-Stack ML Application)

## Overview

This project presents a full-stack fraud detection system designed to evaluate financial transactions in real time using a machine learning model.

It demonstrates how ML models can be integrated into backend services and exposed through a user-facing interface. The system processes input through a backend layer and forwards it to an ML service for prediction.


## Core Features

- Machine learning–based fraud detection  
- Real-time prediction through API integration  
- Probability-based classification of transaction risk  
- Decision layer with outcomes: Approve, Review, Block  
- Structured separation between frontend, backend, and ML components  


## Architecture

Frontend (React) → Backend (Spring Boot) → ML Service (FastAPI) → Prediction Engine → Response


## Workflow

1. The user provides transaction input through the UI  
2. The frontend sends the request to the backend service  
3. The backend formats the input and calls the ML API  
4. The ML model processes the data and returns a probability score  
5. The system applies decision thresholds:
   - Approve  
   - Review  
   - Block  
6. The result is sent back and displayed  


## Technologies Used

- React (Frontend)  
- Spring Boot (Backend)  
- FastAPI (ML API)  
- Scikit-learn, NumPy (Machine Learning)  


## Directory Structure

fraud-detection-system/
│
├── ml-api/
├── backend/
├── fraud-ui/
└── README.md


## Running the Project

### Clone the repository

git clone <repository-url>  
cd fraud-detection-system  


### Start ML service

cd ml-api  
pip install -r requirements.txt  
uvicorn app:app --reload  

Runs on: http://127.0.0.1:8000  


### Start backend server

Run the Spring Boot application  

Runs on: http://localhost:8080  


### Start frontend

cd fraud-ui  
npm install  
npm start  

Runs on: http://localhost:3000  


## Sample Execution

Input:  
Transaction Amount: 5000  

Output:  
Decision: Block  
Fraud Probability: 80.80%  


## Team Contribution

**Md Asad Anwer**

Designed and validated a machine learning model for fraud detection with feature engineering and evaluation

Built and tested FastAPI endpoints for real-time inference and prediction workflows

Implemented decision-layer logic based on fraud probability for practical system outcomes

Developed backend services using Spring Boot to handle client requests and coordinate ML predictions

Ensured reliable frontend-backend communication through proper request handling and JSON mapping

Developed React UI for transaction input and fraud result visualization

Optimized system performance and contributed to debugging across the full stack

**Ritika Srivastava**

Built and trained a fraud detection model with preprocessing, feature scaling, and class imbalance handling

Developed ML inference API using FastAPI to serve real-time predictions

Implemented probability-based fraud scoring and threshold-driven decision logic (Approve / Review / Block)

Integrated ML service with Spring Boot backend for seamless API orchestration

Transformed frontend inputs into model-compatible feature vectors and handled cross-service communication

Contributed to React frontend by integrating APIs and displaying real-time prediction results

Performed debugging and testing to ensure smooth end-to-end system functionality


## Additional Notes

The features used in the model are anonymized. In practical systems, such features are derived automatically from transaction patterns and user behavior.


## Future Scope

- Add persistent storage for transactions  
- Introduce user-level analysis  
- Deploy the system for public access  
- Enhance model accuracy with advanced techniques  
