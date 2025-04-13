# ✈️ Flight Delay Prediction using Vertex AI & TensorFlow

This project uses Google's Vertex AI Workbench and TensorFlow to build and deploy a machine learning model that predicts whether a flight will arrive on time.

## 🚀 Key Features
- Data preprocessing with **BigQuery**
- **Wide & Deep** Neural Network architecture in TensorFlow
- **Model deployment** to Vertex AI Endpoints
- **Explainable AI (XAI)** integration using Sampled Shapley
- Model visualizations with `matplotlib`

## 📊 Dataset
BigQuery tables from `dsongcp` public dataset.

Features used:
- `dep_delay`, `taxi_out`, `distance`, `dep_hour`, `is_weekday`
- Airport coordinates, `carrier`, `origin`, `dest`

Target:
- `ontime`: Whether arrival delay is < 15 minutes

## 🧠 Model Architecture
- Combines:
  - Deep (DenseFeatures + Hidden Layers)
  - Wide (Crossed + Bucketized Categorical Features)
- Final Sigmoid Layer for Binary Classification

Model Diagram

<img width="817" alt="Screenshot 2025-04-12 at 3 20 48 PM" src="https://github.com/user-attachments/assets/690850db-86d0-4996-82ac-4e25c3e646c5" />

Training Results

<img width="840" alt="Screenshot 2025-04-12 at 3 21 03 PM" src="https://github.com/user-attachments/assets/a10fd3ec-d4e1-4f3c-88dd-5d4f018938f5" />



## 🧪 Deployment
Model is exported and deployed to Vertex AI using:
- TensorFlow Serving Docker image
- RESTful endpoint
- Scalable, serverless deployment with auto-replicas

## 💡 Explainable AI
- **Vertex AI Explainable AI** used to inspect feature contributions
- Configured using `explanation-metadata.json`

## 📦 Tools & Stack
- TensorFlow 2.x
- Vertex AI (WorkBench, Endpoints, Explainability)
- Google Cloud Storage
- BigQuery SQL
- Python 3.10

## 📂 Folder Structure
- `model/`: diagrams, metadata
- `notebooks/`: Jupyter notebook for development
- `scripts/`: bash scripts for deployment
- `data/`: example input JSON
- `requirements.txt`: for dependency installation

## 🤖 Try it Yourself
1. Open a Vertex AI Workbench instance
2. Run the notebook in `notebooks/`
3. Deploy model and test using `example_input.json`

## 🙋‍♂️ Author
**Saugat Pyakuryal**  
[LinkedIn](https://linkedin.com/in/iamsaugaat) | [GitHub](https://github.com/iamsaugaat)
