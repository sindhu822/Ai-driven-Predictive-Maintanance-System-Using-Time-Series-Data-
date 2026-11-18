# 🔧 AI-Driven Predictive Maintenance System

An AI-powered Predictive Maintenance system that analyzes equipment sensor data and predicts the **Remaining Useful Life (RUL)** of industrial equipment.

The system uses Machine Learning / Deep Learning models to analyze sensor readings and estimate equipment degradation. It also provides risk assessment, maintenance recommendations, prediction confidence, RUL trends, and SHAP-based Explainable AI.

---

## 🚀 Features

- 📊 Remaining Useful Life (RUL) Prediction
- ⚠️ Equipment Risk Assessment
- 🔧 Dynamic Maintenance Recommendations
- 📈 RUL Prediction Trend Visualization
- 🧠 SHAP Explainable AI
- 📊 Prediction Confidence
- 📁 CSV Sensor Data Upload
- 🌐 Interactive React Dashboard
- ⚡ FastAPI Backend

---

## 🛠️ Technologies Used

### Frontend

- React
- Vite
- Axios
- Recharts
- CSS

### Backend

- Python
- FastAPI
- Uvicorn
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- SHAP

---

# 📂 Project Structure

```text
AI-Predictive-Maintenance/
│
├── backend/
│   ├── main.py
│   ├── requirements.txt
│   ├── model/
│   └── ...
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   ├── UploadFile.jsx
│   │   │   ├── PredictionCard.jsx
│   │   │   ├── RiskCard.jsx
│   │   │   ├── RecommendationCard.jsx
│   │   │   └── ShapChart.jsx
│   │   │
│   │   ├── pages/
│   │   │   └── Dashboard.jsx
│   │   │
│   │   ├── App.jsx
│   │   ├── index.css
│   │   └── main.jsx
│   │
│   ├── package.json
│   └── vite.config.js
│
└── README.md
```

---

# ⚙️ Prerequisites

Make sure the following software is installed.

### Python

Python 3.10 or above is recommended.

Check Python:

```bash
python --version
```

### Node.js

Check Node.js:

```bash
node --version
```

### npm

Check npm:

```bash
npm --version
```

---

# 📥 Clone the Repository

Open a terminal and run:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Example:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

Move into the project:

```bash
cd YOUR-REPOSITORY
```

---

# 🐍 Backend Setup

Open a terminal and move to the backend folder:

```bash
cd backend
```

Create a virtual environment:

### Windows

```bash
python -m venv venv
```

Activate the virtual environment:

```bash
venv\Scripts\activate
```

### Linux / Ubuntu

```bash
python3 -m venv venv
```

Activate:

```bash
source venv/bin/activate
```

Install required packages:

```bash
pip install -r requirements.txt
```

Run the FastAPI backend:

```bash
uvicorn main:app --reload
```

The backend will run at:

```text
http://127.0.0.1:8000
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

---

# 💻 Frontend Setup

Open another terminal.

Move to the frontend folder:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the React application:

```bash
npm run dev
```

The frontend will usually run at:

```text
http://localhost:5173
```

Open the URL in your browser.

---

# ▶️ How to Run the Complete Application

You need to run both the backend and frontend.

## Terminal 1 – Backend

```bash
cd backend
```

Activate the virtual environment:

### Windows

```bash
venv\Scripts\activate
```

### Linux / Ubuntu

```bash
source venv/bin/activate
```

Run:

```bash
uvicorn main:app --reload
```

Backend:

```text
http://127.0.0.1:8000
```

---

## Terminal 2 – Frontend

```bash
cd frontend
```

Run:

```bash
npm install
npm run dev
```

Frontend:

```text
http://localhost:5173
```

---

# 📊 How to Use the Application

1. Start the FastAPI backend.
2. Start the React frontend.
3. Open:

```text
http://localhost:5173
```

4. Upload an equipment sensor CSV file.
5. Click the prediction/upload button.
6. The system will generate:

   - Remaining Useful Life prediction
   - Prediction confidence
   - Equipment risk level
   - Maintenance recommendation
   - RUL prediction trend
   - SHAP feature importance

---

# 🔌 API Endpoints

The frontend communicates with the FastAPI backend.

| Endpoint | Method | Description |
|---|---|---|
| `/predict` | POST | Upload sensor CSV and generate prediction |
| `/uncertainty` | GET | Get prediction uncertainty/confidence |
| `/shap` | GET | Get SHAP feature importance |

Backend base URL:

```text
http://127.0.0.1:8000
```

---

# 🧠 Explainable AI

The system uses **SHAP (SHapley Additive exPlanations)** to explain which sensor features have the highest impact on the RUL prediction.

The SHAP visualization helps users understand:

- Which sensor features influence the prediction
- Feature importance
- Relative impact of equipment parameters
- Model decision interpretation

---

# 📈 System Workflow

```text
                ┌──────────────────────┐
                │   Sensor CSV File    │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │   FastAPI Backend    │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │ Data Preprocessing   │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │  ML / DL RUL Model   │
                └──────────┬───────────┘
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
     RUL Prediction    Risk Level      Confidence
          │
          ▼
  Maintenance Recommendation
          │
          ├──────────────► RUL Trend
          │
          └──────────────► SHAP Explanation
                           │
                           ▼
                ┌──────────────────────┐
                │   React Dashboard    │
                └──────────────────────┘
```

---

# 🧪 Input Data

The application accepts equipment sensor data in CSV format.

Example structure:

```text
cycle,sensor_1,sensor_2,sensor_3,...
1,0.25,0.45,0.67,...
2,0.28,0.48,0.65,...
3,0.30,0.50,0.70,...
```

The exact CSV format should match the format expected by the trained model.

---

# ⚠️ Important Notes

- Make sure the backend is running before starting predictions.
- The frontend expects the backend at:

```text
http://127.0.0.1:8000
```

- Do not rename or remove trained model files.
- Make sure the required model files are included in the project.
- Install all dependencies before running the application.
- Use a CSV file with the correct sensor columns.

---

# 👩‍💻 Author

**Harshitha B**

B.E. Artificial Intelligence & Machine Learning

---

# 📄 License

This project is created for educational and academic purposes.