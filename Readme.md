## Network secruity project for Phising data
# 🛡️ Network Security – Phishing Detection using Machine Learning

An end-to-end Machine Learning project for detecting phishing websites and malicious network activity using network-related features.

The project demonstrates a production-style ML workflow including data ingestion, validation, transformation, model training, experiment tracking, prediction, and deployment.

---

## 🚀 Project Overview

Phishing websites are designed to imitate legitimate websites and trick users into providing sensitive information such as passwords, banking details, or personal data.

This project builds a Machine Learning system that analyzes network and website-related features and predicts whether the activity is **legitimate or phishing**.

The goal is not only to train a model but also to implement a reusable **end-to-end MLOps pipeline**.

---

## ✨ Key Features

- End-to-end Machine Learning pipeline
- Automated data ingestion
- Data validation and schema checking
- Feature transformation and preprocessing
- Machine Learning model training
- Model evaluation and selection
- Experiment tracking
- MongoDB-based data storage
- Prediction pipeline
- Web application for predictions
- Docker support
- Modular Python project structure
- Exception handling and application logging

---

## 🏗️ Project Architecture

```text
Raw Network Data
       │
       ▼
   MongoDB
       │
       ▼
Data Ingestion
       │
       ▼
Data Validation
       │
       ▼
Data Transformation
       │
       ▼
 Model Training
       │
       ▼
Model Evaluation
       │
       ▼
 Trained Model
       │
       ▼
Prediction Pipeline
       │
       ▼
 Web Application
```

---

## 🧠 Machine Learning Pipeline

### 1. Data Ingestion

Data is collected from the configured data source and converted into a format suitable for the training pipeline.

The ingestion component separates the data into training and testing datasets.

### 2. Data Validation

The validation stage checks:

- Required columns
- Dataset schema
- Missing values
- Data types
- Feature consistency
- Data quality

This ensures that invalid data does not enter the training pipeline.

### 3. Data Transformation

The data is cleaned and transformed before training.

Typical preprocessing includes:

- Missing-value handling
- Feature transformation
- Numerical preprocessing
- Feature preparation for Machine Learning algorithms

### 4. Model Training

Multiple Machine Learning algorithms can be evaluated to determine the best performing model.

The selected model is trained using the transformed training dataset.

### 5. Model Evaluation

The trained model is evaluated using classification metrics such as:

- Accuracy
- Precision
- Recall
- F1 Score

The best model is selected for prediction.

### 6. Prediction Pipeline

New network data can be passed through the prediction pipeline.

The pipeline automatically:

```text
Input Data
   ↓
Preprocessing
   ↓
Feature Transformation
   ↓
ML Model
   ↓
Prediction
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation |
| NumPy | Numerical processing |
| Scikit-learn | Machine Learning |
| MongoDB | Data storage |
| PyMongo | MongoDB integration |
| MLflow | Experiment tracking |
| Docker | Containerization |
| FastAPI / Flask | Application/API layer |
| GitHub | Version control |
| GitHub Actions | CI/CD automation |

---

## 📁 Project Structure

```text
networksecurity/
│
├── networksecurity/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_validation.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   │
│   ├── pipeline/
│   │   ├── training_pipeline.py
│   │   └── batch_prediction.py
│   │
│   ├── entity/
│   ├── utils/
│   ├── logging/
│   ├── exception/
│   └── constant/
│
├── data_schema/
├── templates/
├── final_model/
├── prediction_output/
│
├── app.py
├── main.py
├── requirements.txt
├── setup.py
├── Dockerfile
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/chait009/networksecurity.git
cd networksecurity
```

### 2. Create a Virtual Environment

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

Linux/macOS:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

If the application connects to MongoDB or external services, configure the required environment variables.

Example:

```text
MONGODB_URL=your_mongodb_connection_string
```

Do not commit credentials or `.env` files containing secrets to GitHub.

---

## 🏋️ Run the Training Pipeline

Run:

```bash
python main.py
```

The pipeline performs:

```text
Data Ingestion
      ↓
Data Validation
      ↓
Data Transformation
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Model Saved
```

---

## 🔮 Run the Application

Start the application using:

```bash
python app.py
```

Depending on the configured web framework, open the local application URL shown in the terminal.

For example:

```text
http://localhost:8000
```

---

## 🐳 Docker

Build the Docker image:

```bash
docker build -t network-security .
```

Run the container:

```bash
docker run -p 8000:8000 network-security
```

---

## 📊 Model Workflow

```text
Network Features
       │
       ▼
Data Preprocessing
       │
       ▼
Feature Engineering
       │
       ▼
Machine Learning Model
       │
       ▼
┌────────────────────┐
│ Legitimate Traffic │
│         OR         │
│ Phishing Activity  │
└────────────────────┘
```

---

## 📈 MLOps Concepts Demonstrated

This project demonstrates several practical MLOps concepts:

- Modular ML pipelines
- Reusable Python components
- Training and inference separation
- Experiment tracking
- Model artifact management
- Data validation
- Environment-based configuration
- Containerization
- CI/CD readiness
- Production-style logging
- Custom exception handling

---

## 🎯 Why This Project Matters

Building an ML model is only one part of deploying Machine Learning systems.

This project demonstrates how an ML solution can be structured as a maintainable application where:

- Data can continuously enter the system
- Data quality is validated automatically
- Features are transformed consistently
- Models can be retrained
- Experiments can be tracked
- Predictions can be served through an application

This makes the project representative of a **real-world Machine Learning engineering workflow** rather than just a standalone notebook.

---

## 🔮 Future Improvements

Potential improvements include:

- Real-time network traffic classification
- Advanced phishing URL analysis
- SHAP-based model explainability
- Model monitoring
- Data drift detection
- Automated model retraining
- Kubernetes deployment
- Cloud deployment
- REST API endpoint for real-time predictions
- Centralized monitoring and logging
- Dashboard for security analytics

---

## 👨‍💻 Author

**Chait**

AI / Machine Learning Engineer

GitHub: `chait009`

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐.
