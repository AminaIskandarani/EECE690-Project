# Wind Turbine Fault Forecasting & Preventive Maintenance (EECE 690)

This repository contains our final project for EECE 690 - Introduction to Machine Learning at the American University of Beirut. The project is titled:

> **Fault Prediction and Preventive Maintenance for Wind Turbines Using Machine Learning**

It includes a Streamlit-based HMI dashboard, synthetic fault generation, Random Forest and MLP classifiers, cost-effectiveness evaluation, and full deployment support.
This paper explores the modeling of a machine learning-based framework for predictive maintenance in wind turbines with the aid of SCADA sensor data. The system leverages synthetic and historical fault data, dimensionality reduction,
and anomaly detection through Random Forest and Multi-Layer Perception. The solution aims to flag abnormal behavior early, reduce downtime, and enhance turbine reliability.

Project Structure

```bash
.
docker_complicated/
├── .dockerignore
├── docker-compose.yml
├── Dockerfile
├── full_complicated_model.py            # Main ML pipeline
├── failure_only_sensor_data_with_failure_info.csv
├── turbine_T01_data.csv
├── turbine_T06_data.csv
└── requirements.txt
```

---

How to Run

- Python 3.10+ or Docker

### Local Setup
```bash
pip install -r requirements.txt
streamlit run app.py
```

### Dockerized Setup
```bash
docker build -t turbine-dashboard .
docker run -p 8501:8501 turbine-dashboard
```
Then open [http://localhost:8501](http://localhost:8501)

---

Key Features
- Synthetic fault injection using statistical deviation patterns
- Realistic sensor augmentation with progressive and overlapping faults
- Grid-search over model hyperparameters with cost trade-off function
- Random Forest and MLP classifier support
- SCADA-based anomaly prediction
- HMI-style UI to visualize turbine status and component-level faults

Documentation
- Includes a detailed report that explains the background and overview of the topic, algorithms used, and results.
- 
Evaluation Metrics
- Fault-only classification accuracy
- Training/inference time per model
- Model size in MB
- Feature importance (RF only)
- Cost metric combining accuracy and resource trade-offs

 Deployment
- Containerized with Docker
- Suitable for cloud or edge deployment
- Integration-ready for SCADA/HMI interfaces
- Integration is ready for BMS

Contributors
- Amina Iskandarani — ami43@mail.aub.edu
- Ahmad Daher — ahd43@mail.aub.edu
- Ahmad Younes — amy04@mail.aub.edu

License
This project is developed solely for academic purposes at the American University of Beirut. No commercial usage is permitted without explicit permission.



