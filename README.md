# 🏥 Nabha Telemedicine Platform

> Smart India Hackathon (SIH) 2025 Project | Top 100 Teams at Bennett University

A full-stack, microservices-based rural healthcare platform developed for **Smart India Hackathon 2025**. The platform aims to bridge the healthcare gap in underserved rural communities by providing accessible digital healthcare services, AI-powered diagnostics, telemedicine, and secure health record management.

🏆 **Achievement:** Ranked among the **Top 100 teams out of 500+ teams** at Bennett University during SIH 2025.

---

## 🚀 Key Features

| Module | Description | Port |
|----------|-------------|------|
| Main Platform | Central healthcare dashboard | 3000 |
| Community Chat & Forum | Real-time community discussions and doctor-verified Q&A | 5050 |
| Skin Disease Detection | AI-powered skin disease diagnosis using CNN | 5002 |
| Village Health Hub | Nearby healthcare resources and village health information | 5176 |
| Pregnancy & Period Tracker | Women's health and pregnancy monitoring | 5177 |
| Blood Donation System | Blood donor matching and blood bank locator | 5178 |
| Digital Health Records | Secure cloud-based medical records | 3002 |
| Medicine Availability Tracker | Medicine search and pharmacy stock availability | 5002 |
| Video Consultation | Real-time doctor-patient consultation | 5175 |
| Unified Backend | API gateway for all services | 8000 |

---

## 🛠️ Technology Stack

### Frontend
- React 18
- Vite
- TypeScript
- Tailwind CSS
- Socket.IO Client

### Backend
- Node.js
- Express.js
- Python Flask
- Socket.IO
- JWT Authentication

### Database & Cloud
- SQLite
- Firebase Firestore
- MySQL (Optional)

### AI / Machine Learning
- TensorFlow
- Keras
- Convolutional Neural Networks (CNN)
- Custom Trained `.h5` Model

### Third-Party Integrations
- ZEGOCLOUD Video Calling
- Firebase
- JWT Security
- Role-Based Access Control (RBAC)

---

## 🏗️ System Architecture

```text
                     ┌────────────────────┐
                     │   Main Platform    │
                     │   Port : 3000      │
                     └─────────┬──────────┘
                               │
        ┌──────────────────────┼──────────────────────┐
        │                      │                      │
        ▼                      ▼                      ▼

 ┌─────────────┐      ┌───────────────┐      ┌─────────────┐
 │ Chat Forum  │      │ Health Records│      │ Unified API │
 │ Port :5050  │      │ Port :3002    │      │ Port :8000  │
 └─────────────┘      └───────────────┘      └─────────────┘

        │
        ▼

 ┌─────────────────────────────────────────────┐
 │            Micro Frontends                  │
 ├─────────────────────────────────────────────┤
 │ Skin Disease Detection      → Port 3001     │
 │ Video Consultation          → Port 5175     │
 │ Village Health Hub          → Port 5176     │
 │ Pregnancy Tracker           → Port 5177     │
 │ Blood Donation System       → Port 5178     │
 └─────────────────────────────────────────────┘
```

---

## 📂 Project Structure

```text
Nabha-Telemedicine-Platform/
│
├── Main Platform
├── Community Chat & Forum
├── Digital Health Records
├── Medicine Availability API
├── Skin Disease Detection
├── Unified Backend
├── Video Consultation
├── Village Health Hub
├── Pregnancy & Period Tracker
└── Blood Donation System
```

---

## ⚙️ Installation

### Prerequisites

- Node.js v18+
- Python 3.11+
- npm
- Git

### Clone Repository

```bash
git clone https://github.com/shaauryaa/team-console-healthcare.git
cd team-console-healthcare
```

---

## 📦 Install JavaScript Dependencies

```bash
cd chat-sih
npm install

cd client
npm install

cd ../../"Smart India Hackathon 2025/Digital health records"
npm install

cd ../"Rural Healthcare Website Design (2)"
npm install

cd "ZEGOCLOUD-VideoCalling-App-main"
npm install

cd ../../../"Village Health Hub"
npm install

cd ../"Pregnancy and Period Tracker"
npm install

cd ../"Blood Donation App Features"
npm install

cd ../"Skin-Disease-Prediction-main/Skin Disease Prediction Form"
npm install
```

---

## 🐍 Setup Python Environments

### Medicine Availability API

```bash
python -m venv "Smart India Hackathon 2025/API/venv"

"Smart India Hackathon 2025/API/venv/Scripts/pip" install -r \
"Smart India Hackathon 2025/API/requirements.txt"

pip install bcrypt PyJWT
```

### Unified Backend

```bash
python -m venv "Smart India Hackathon 2025/unified-backend/venv"

"Smart India Hackathon 2025/unified-backend/venv/Scripts/pip" install -r \
"Smart India Hackathon 2025/unified-backend/requirements.txt"
```

### Skin Disease Detection API

```bash
python -m venv "Skin-Disease-Prediction-main/venv_new"

"Skin-Disease-Prediction-main/venv_new/Scripts/pip" install -r \
"Skin-Disease-Prediction-main/requirements.txt"

pip install flask-cors
```

---

## 🔐 Environment Variables

Create environment files before running the project.

### Community Chat Service

```env
PORT=5050
DB_TYPE=sqlite
DB_PATH=./database/community.db
JWT_SECRET=your-secret-key
```

### Digital Health Records

```env
FIREBASE_API_KEY=your_key
FIREBASE_PROJECT_ID=your_project
FIREBASE_AUTH_DOMAIN=your_domain
```

Configure additional Firebase credentials as required.

---

## ▶️ Running the Project

### 1. Main Website

```bash
cd "Smart India Hackathon 2025/Rural Healthcare Website Design (2)"
npx vite --port 3000 --host
```

### 2. Community Chat Backend

```bash
cd chat-sih
node server.js
```

### 3. Health Records Backend

```bash
cd "Smart India Hackathon 2025/Digital health records"
node server.js
```

### 4. Medicine Availability API

```bash
cd "Smart India Hackathon 2025/API"
./venv/Scripts/python app.py
```

### 5. Unified Backend

```bash
cd "Smart India Hackathon 2025/unified-backend"
./venv/Scripts/python app.py
```

### 6. Skin Disease Detection API

```bash
cd "Skin-Disease-Prediction-main"
./venv_new/Scripts/python app.py
```

### 7. Micro Frontends

```bash
# Skin Disease Detection UI
cd "Skin-Disease-Prediction-main/Skin Disease Prediction Form"
npx vite --port 3001

# Video Consultation
cd "ZEGOCLOUD-VideoCalling-App-main"
npx vite --port 5175

# Village Health Hub
cd "Village Health Hub"
npx vite --port 5176

# Pregnancy Tracker
cd "Pregnancy and Period Tracker"
npx vite --port 5177

# Blood Donation System
cd "Blood Donation App Features"
npx vite --port 5178
```

---

## 🌐 Access the Platform

After all services are running:

```text
http://localhost:3000
```

---

## 🔒 Security Features

- JWT Authentication
- Secure Health Record Storage
- Firebase Cloud Security
- Role-Based Access Control
- Protected API Routes
- Secure Video Consultations

---

## 🎯 Impact

The Nabha Telemedicine Platform addresses several critical healthcare challenges in rural India:

- Improved healthcare accessibility
- AI-assisted disease detection
- Secure digital medical records
- Emergency blood donation support
- Women's health monitoring
- Real-time doctor consultations
- Community-driven healthcare awareness

---

## 👨‍💻 Team

### Team Console
Smart India Hackathon 2025

Contributors:
- Ishank Pandey
- Team Console Members

---

## 📜 License

This project is licensed under the MIT License.

---

### ⭐ If you found this project useful, don't forget to star the repository!