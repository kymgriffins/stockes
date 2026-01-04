# **NSE Analytics API** 📈

A high-performance FastAPI application for analyzing and predicting Kenyan stock market trends using Nairobi Securities Exchange (NSE) data. This repository provides RESTful endpoints for market analytics, predictive modeling, and data visualization.

## ✨ Features

- **Real-time Market Data**: Fetch and process live NSE data
- **Predictive Analytics**: Machine learning models for stock price predictions
- **Comprehensive Analysis**: Technical indicators, trend analysis, and market insights
- **RESTful API**: Clean, documented endpoints with OpenAPI (Swagger) support
- **Data Visualization**: Generate charts and reports for market trends
- **Automated Updates**: Scheduled data collection and model retraining
- **Database Integration**: PostgreSQL/MongoDB support for historical data

## 🚀 Quick Start

### Prerequisites
- Python 3.9+
- pip or poetry
- PostgreSQL (optional, SQLite supported for development)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/nse-analytics-api.git
cd nse-analytics-api
```

2. **Create virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Set up environment variables**
```bash
cp .env.example .env
# Edit .env with your configuration
```

5. **Run the application**
```bash
uvicorn app.main:app --reload
```

Visit `http://localhost:8000/docs` for API documentation.

## 📁 Project Structure

```
nse-analytics-api/
├── app/
│   ├── api/           # API endpoints
│   ├── core/          # Core configurations
│   ├── models/        # Database models
│   ├── schemas/       # Pydantic schemas
│   ├── services/      # Business logic
│   ├── ml/            # Machine learning models
│   ├── utils/         # Utilities and helpers
│   └── main.py        # FastAPI application
├── tests/             # Test suite
├── data/              # Data storage
├── notebooks/         # Jupyter notebooks for analysis
├── requirements.txt   # Dependencies
└── docker-compose.yml # Docker setup
```

## 🔌 API Endpoints

### Market Data
- `GET /api/v1/stocks` - List all stocks
- `GET /api/v1/stocks/{symbol}/history` - Historical data
- `GET /api/v1/stocks/{symbol}/current` - Current price
- `GET /api/v1/market/indices` - Market indices

### Analytics
- `POST /api/v1/analyze/technical` - Technical indicators
- `POST /api/v1/analyze/trend` - Trend analysis
- `GET /api/v1/analyze/sentiment` - Market sentiment

### Predictions
- `POST /api/v1/predict/{symbol}` - Price predictions
- `GET /api/v1/predict/models` - Available ML models
- `POST /api/v1/predict/train` - Train new model

### Reports
- `GET /api/v1/reports/daily` - Daily market report
- `POST /api/v1/reports/custom` - Custom report generation

## 🧠 Machine Learning Models

The platform includes several predictive models:

1. **LSTM Neural Networks** for time-series forecasting
2. **Random Forest Regressor** for price predictions
3. **Prophet** for trend forecasting
4. **ARIMA** for statistical time-series analysis

## 🐳 Docker Deployment

```bash
# Build and run with Docker Compose
docker-compose up -d

# View logs
docker-compose logs -f
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📊 Data Sources

- Nairobi Securities Exchange (NSE) official data
- Yahoo Finance API
- Alternative data sources for market sentiment

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

## 🛠️ Tech Stack

- **Backend**: FastAPI, Python
- **Database**: PostgreSQL, SQLite
- **ML/DL**: TensorFlow, Scikit-learn, Prophet
- **Data Processing**: Pandas, NumPy
- **Visualization**: Plotly, Matplotlib
- **Deployment**: Docker, NGINX, Gunicorn
- **Monitoring**: Prometheus, Grafana

## 📈 Roadmap

- [ ] Real-time WebSocket support
- [ ] Mobile application
- [ ] Advanced portfolio optimization
- [ ] Social media sentiment integration
- [ ] Automated trading strategies (paper trading)

## 🔗 Links



**Disclaimer**: This tool is for educational and research purposes only. Not financial advice. Always do your own research before investing.

---
