# Business Sales Forecasting and Analysis for Retail Stores

## Project Overview
This project presents a comprehensive retail sales forecasting solution by combining structured data analysis and unstructured customer review sentiment insights. The objective is to accurately predict Walmart's weekly sales to support decision-making in inventory management, promotions, and strategic planning. The solution integrates advanced machine learning and natural language processing techniques, culminating in a FastAPI deployment for real-time sales forecasting and review sentiment analysis.

## 📁 Dataset
- Walmart Store Sales Forecasting Dataset
- Store-level weekly sales data
- Economic indicators: CPI, fuel price, unemployment
- Holiday information
- Customer reviews (unstructured text)

## 🧠 Techniques Used
- Feature Engineering (Lag features, holiday flags, store type encoding)
- Time Series Modeling: SARIMA
- Machine Learning Models: Random Forest Regressor, LightGBM
- Sentiment Analysis: DistilBERT Transformer Model
- Deployment: FastAPI

## 🔍 Explorations & Findings
- Department 72 leads in peak holiday sales; Department 92 maintains highest average sales.
- Store 20 and Store 4 are consistently high performers in terms of average weekly sales.
- Store size (Type A, B, C) correlates with sales performance; Type A (largest) stores outperform others.
- Thanksgiving records the highest spike in sales across all holidays.
- Week 51 (Christmas) and weeks 47-50 mark seasonal shopping spikes.
- 2010 reported higher sales than subsequent years, with missing Nov-Dec data for 2012.
- Economic variables like CPI, fuel price, and unemployment showed limited predictive power.

## ⚙️ Methodology
### Structured Data Modeling:
- Data cleaning, outlier handling, and null imputation
- Exploratory Data Analysis using pandas, seaborn, and matplotlib
- SARIMA model trained on global weekly sales pattern
- Feature-rich machine learning using Random Forest and LightGBM

### Unstructured Data Processing:
- Customer reviews labeled manually
- DistilBERT fine-tuned for sentiment classification
- Sentiment features integrated into final regression models to enrich predictions

### Deployment:
- Built and deployed a FastAPI service
- Endpoints: `/predict_sales`, `/analyze_sentiment`
- Ready for cloud deployment with autoscaling via AWS/GCP

## 🚧 Limitations
- Global SARIMA models may miss store-department level seasonality
- Limited availability and impact of economic indicators
- Manual review labeling constrained sentiment model performance

## 📈 Future Enhancements
- Integrate additional variables (e.g., weather, competitor pricing)
- Implement LSTM and Transformer-based sequence models for time series
- Scale sentiment labeling via semi-supervised learning
- Cloud-based scalable deployment with CI/CD

## ✅ Conclusion
This project bridges traditional machine learning and modern NLP to deliver actionable, scalable retail forecasting. By combining LightGBM-based predictive models with transformer-based sentiment analysis (DistilBERT), it illustrates the power of integrating qualitative and quantitative signals in sales forecasting. Future work will focus on scalability, automation, and deeper time-series modeling with neural architectures.

---

### 📌 GitHub Repository Structure
```bash
├── data/                   # Processed datasets
├── notebooks/              # Jupyter notebooks for EDA and modeling
├── models/                 # Saved ML and NLP models
├── app/                    # FastAPI app and endpoints
├── scripts/                # Preprocessing, training, evaluation scripts
├── README.md               # Project description and instructions
├── requirements.txt        # Dependencies
└── Dockerfile              # For containerized deployment
```

### 💡 Key Technologies
- Python, Pandas, Numpy
- Scikit-learn, LightGBM, SARIMA (statsmodels)
- Transformers (HuggingFace, DistilBERT)
- FastAPI, Uvicorn
- Git, Docker
- AWS/GCP (planned)

### 🔗 Stay Tuned
More improvements coming soon — follow for updates on sequential deep learning, large-scale deployment, and enriched datasets!
