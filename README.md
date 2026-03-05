# 🧠 AI-Powered API Monitoring & Anomaly Detection System

An **AI-driven observability and monitoring platform** designed for large-scale distributed API ecosystems across **on-premise, cloud, and multi-cloud environments**.

The system combines **OpenTelemetry observability, Grafana monitoring, and machine learning models** to detect anomalies, predict failures, and automatically alert engineers with **AI-generated Root Cause Analysis (RCA)**.

---

# 🎯 Problem It Solves

Modern distributed API systems face challenges such as:

- Performance degradation
- Latency spikes
- Hidden service dependencies
- Delayed incident detection
- Difficult root cause identification

This platform provides:

✅ Intelligent monitoring  
✅ Predictive analytics  
✅ Automated incident alerts  
✅ AI-generated RCA reports  

Helping teams **reduce downtime and improve API reliability.**

---

# 🚀 Key Features

## 🤖 AI Phone Alert & Automation System
- Automated **phone alerts triggered by logs, metrics, and traces**
- **Workflow-based automated recovery tasks**
- **AI-generated Root Cause Analysis reports**
- Voice-enabled **incident reporting and status updates**

---

## 🔍 Intelligent Root Cause Analysis Engine
- Correlates **logs, metrics, and traces**
- Uses **Prophet for time-series forecasting**
- Uses **Isolation Forest for anomaly detection**
- Automatically generates **comprehensive RCA reports**

---

## 📊 Real-time Monitoring Stack

- **Grafana** → Visualization dashboards  
- **Loki** → Log aggregation  
- **Tempo** → Distributed tracing  
- **Mimir** → Long-term metrics storage  

---

## 🔥 Advanced Anomaly Detection

- **Isolation Forest ML model**
- Detects:
  - Latency spikes
  - Error rate anomalies
  - Traffic pattern deviations
- Environment-aware alert thresholds
- Real-time anomaly scoring

---

## 📈 Predictive Analytics

- Powered by **Prophet forecasting**
- Predicts:
  - Traffic trends
  - Potential service failures
  - Resource usage
- Enables **proactive alerts before incidents occur**

---

## 🧭 End-to-End API Tracking

- Tracks **complete API request lifecycle**
- Cross-service dependency mapping
- Performance bottleneck detection
- Service mesh observability

---

## 📊 Centralized Visualization

Unified **Grafana dashboards** provide:

- Real-time metrics
- Log and trace correlation
- Historical trend analysis
- Custom alerting rules

---

# 🏗️ System Architecture
┌─────────────────┐ ┌──────────────────┐ ┌─────────────────┐
│ Node.js API │───▶│ OpenTelemetry │───▶│ Grafana │
│ Application │ │ Collector │ │ (Dashboard) │
└─────────────────┘ └──────────────────┘ └─────────────────┘
│
▼
┌──────────────────┐
│ Observability │
│ Stack │
├──────────────────┤
│ • Loki (Logs) │
│ • Tempo (Traces) │
│ • Mimir (Metrics)│
└──────────────────┘
│
▼
┌──────────────────┐
│ AI/ML Engine │
├──────────────────┤
│ • Prophet │
│ • Isolation │
│ Forest │
└──────────────────┘
│
▼
┌──────────────────┐
│ Alert System │
├──────────────────┤
│ • Phone Calls │
│ • RCA Reports │
│ • Automation │
└──────────────────┘


---

# 🛠️ Components

| Component | Description |
|------|------|
| Node.js Express API | Sample API generating telemetry data |
| OpenTelemetry SDK | Collects metrics, logs, traces |
| OpenTelemetry Collector | Processes and routes telemetry |
| Grafana | Visualization dashboards |
| Loki | Centralized log aggregation |
| Tempo | Distributed tracing backend |
| Mimir | Long-term Prometheus metrics storage |
| Prophet | Time-series forecasting model |
| Isolation Forest | ML-based anomaly detection |
| AI Alert System | Phone alerts + automated RCA |

---

# 📋 Prerequisites

- Node.js **v16+**
- Docker & Docker Compose
- Python **3.8+**
- Twilio Account (for phone alerts)
- Gemini API Key (for RCA generation)

---

# 🚀 Setup Instructions

## 1️⃣ Clone the Repository

```bash
git clone <repository-url>
cd ai-api-monitoring-system

2️⃣ Install Dependencies
Node.js
npm install
Python
pip install -r requirements.txt
3️⃣ Configure Environment Variables

## Twilio Configuration
TWILIO_ACCOUNT_SID=your_twilio_account_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_PHONE_NUMBER=your_twilio_phone_number

# Gemini API
GEMINI_API_KEY=your_gemini_api_key

# Alert Configuration
ALERT_PHONE_NUMBERS=+1234567890,+0987654321

# Application Configuration
NODE_ENV=production
API_PORT=8080

4️⃣ Start Infrastructure
docker-compose up -d

Verify services:

docker-compose ps
5️⃣ Initialize Observability Stack
sleep 60

./scripts/setup-dashboards.sh
./scripts/setup-datasources.sh
6️⃣ Start the API Application
npm start

Development mode:

npm run dev
7️⃣ Start AI/ML Services
python ai/anomaly_detector.py &
python ai/prophet_forecaster.py &
python ai/alert_system.py &
python ai/rca_engine.py &
8️⃣ Generate Test Traffic
docker-compose run load-tester

Or

python scripts/traffic_generator.py
🧪 Testing the System
API Endpoints
curl http://localhost:8080/rolldice
curl http://localhost:8080/health
curl http://localhost:8080/error
curl http://localhost:8080/heavy
curl http://localhost:8080/db-query
Load Testing
artillery run load-test.yml

Or

python scripts/load_test.py --duration 300 --rps 50
📊 Accessing Dashboards
Grafana
http://localhost:3000

Login:

username: admin
password: admin
Available Dashboards

API Overview
Anomaly Detection
Predictive Analytics
Distributed Tracing
Infrastructure Monitoring

📈 Key Metrics to Monitor
Response Time (P50, P95, P99)
Error Rate (4xx / 5xx)
Request Throughput
Isolation Forest Anomaly Scores
Prophet Prediction Accuracy

🚨 Alert System Configuration

Example thresholds:

ANOMALY_THRESHOLD = 0.7
ERROR_RATE_THRESHOLD = 0.05
LATENCY_THRESHOLD = 2000
ALERT_COOLDOWN = 300
🤖 AI/ML Components
Prophet Forecasting

Predicts:
Future API traffic
Expected response time
Resource utilization
Potential failure windows
Isolation Forest
Detects anomalies in:
Latency distributions
Error patterns
Traffic spikes
Cross-service correlations

🔍 Troubleshooting
Check Service Logs
docker logs otel-collector
docker logs grafana
docker logs loki
docker logs tempo
docker logs mimir
AI Service Logs
tail -f logs/anomaly_detector.log
tail -f logs/alert_system.log
🛡️ Security Considerations
Store credentials in environment variables
Enable TLS for inter-service communication
Secure Grafana dashboards
Protect AI endpoints with API keys

🤝 Contributing
Fork the repository
Create a branch
git checkout -b feature/amazing-feature
Commit changes
git commit -m "Add amazing feature"
Push branch
git push origin feature/amazing-feature
Open a Pull Request
