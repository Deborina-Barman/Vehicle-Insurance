# 🚗 Vehicle Insurance Prediction - End-to-End MLOps Pipeline

This project is an end-to-end **MLOps pipeline** for predicting vehicle insurance policy purchase likelihood. It includes everything from data ingestion to deployment using tools like **MongoDB**, **DVC**, **AWS S3**, **EC2**, **Docker**, **GitHub Actions**, and more.

---

## 📌 Features

- Modular code with proper architecture
- MongoDB integration for data ingestion
- DVC-based pipeline management and versioning
- Data validation and transformation
- Model training, evaluation, and pusher components
- AWS S3 for model registry
- CI/CD pipeline using GitHub Actions + Docker + AWS ECR + EC2
- Web app deployment via FastAPI on EC2

---

## 🛠 Tech Stack

| Layer            | Tools Used                                |
|------------------|--------------------------------------------|
| Data Storage     | MongoDB Atlas                              |
| Pipeline Mgmt    | DVC                                        |
| Cloud Storage    | AWS S3, EC2                                |
| App Deployment   | Docker, GitHub Actions, EC2 (Self-Hosted) |
| Model Registry   | S3 Buckets                                 |
| Web App          | FastAPI, Jinja2 Templates                  |

---

## 🗂️ Project Structure

```
├── src
│   ├── components
│   ├── data_access
│   ├── configuration
│   ├── entity
│   ├── pipeline
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
├── notebook
│   ├── mongoDB_demo.ipynb
│   └── eda_feature_engineering.ipynb
├── static/
├── templates/
├── dvc.yaml
├── params.yaml
├── Dockerfile
├── requirements.txt
├── setup.py
├── pyproject.toml
└── app.py
```

---

## 🔄 Pipeline Workflow

1. **Data Ingestion** from MongoDB Atlas
2. **Data Validation** using schema definitions
3. **Data Transformation** into ML-ready format
4. **Model Training** using scikit-learn (or any ML model)
5. **Model Evaluation** against thresholds
6. **Model Pushing** to AWS S3 bucket
7. **CI/CD Integration** to automate Docker builds and deploy to EC2

---

## 🚀 Deployment Instructions

### ✅ Setup MongoDB Atlas
- Create a cluster and user
- Allow IP access (0.0.0.0/0)
- Copy the Python connection string and export it as `MONGODB_URL`

### ✅ Setup Virtual Environment
```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
pip install -r requirements.txt
```

### ✅ DVC Pipeline Setup
```bash
dvc init
dvc repro
```

### ✅ AWS Setup
- IAM User (Admin Access)
- AWS S3 Bucket: `my-model-mlopsproj`
- EC2 Instance + ECR repo for deployment
- Setup environment variables:
```bash
export AWS_ACCESS_KEY_ID="<your_key_id>"
export AWS_SECRET_ACCESS_KEY="<your_secret_key>"
```

### ✅ Docker + EC2 Deployment
- Build Docker image
- Push to ECR
- SSH into EC2 and run Docker container

---

## 🌐 App Access
- After deployment: `http://<your-ec2-ip>:5080`
- Includes `/predict` and `/train` endpoints

---

## 📽️ Demo

👉 Coming soon...

Or add:
```markdown
🔗 [Live Demo](http://<ec2-public-ip>:5080)
```

---

## 📈 Future Improvements
- Add model monitoring with Prometheus
- Improve model training pipeline with MLflow tracking
- Deploy using Kubernetes for scalability

---

## 🤝 Contributions
Open to contributions. Raise an issue or open a PR.

---

## 🙌 Acknowledgements
Inspired by real-world MLOps workflows and course-style projects.

---

## 📧 Contact
**Deborina Barman**  
Email: deborina.24mas10045@vitbhopal.ac.in  
LinkedIn: [deborinabarman](https://www.linkedin.com/in/deborinabarman/)

---

> "From Data to Deployment — One Project, All MLOps!"

