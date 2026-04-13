# AI LAB Advanced

A complete Streamlit-based ML/DL platform for data handling, training, evaluation, inference, model lifecycle management, and multi-provider AI assistant integration.

**Created by Mohammad Saeed Angiz**

## Features

- **Data Hub**
  - Upload CSV/JSON
  - Basic preprocessing (drop duplicates, handle nulls, reset index)
  - Interactive visualizations with Plotly

- **ML Training**
  - Algorithms: Random Forest, XGBoost, Logistic Regression
  - Real hyperparameter optimization using `GridSearchCV`
  - K-Fold cross-validation
  - Progress tracking and test-set evaluation

- **Deep Learning**
  - Keras neural network builder (add/remove layers)
  - Configurable units, activation, dropout, LR, epochs, batch size
  - Callback support: EarlyStopping + ReduceLROnPlateau

- **AI Assistant**
  - OpenAI API integration
  - Anthropic API integration
  - Ollama local API integration
  - Custom URL + custom headers + payload template support
  - Chat history UI

- **Evaluation**
  - Classification: accuracy, precision, recall, F1, confusion matrix, ROC curve
  - Regression: RMSE, MAE, R²
  - Feature importance / coefficient visualization

- **Prediction**
  - Single-record prediction form
  - Batch CSV prediction with downloadable output

- **Model Management**
  - Save/load model bundles with pickle
  - Metadata storage in JSON

- **Settings**
  - Configure AI providers and save in `config.json`

- **User Guide** page inside app

---

## Project Structure

```bash
ai_lab_advanced/
├── app.py
├── requirements.txt
├── config.json
└── README.md
```

---

## Setup Instructions

1. **Create and activate a virtual environment (recommended)**

```bash
python -m venv .venv
source .venv/bin/activate   # Linux/macOS
# .venv\Scripts\activate   # Windows
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Run the app**

```bash
streamlit run app.py
```

4. **Open in browser**

Streamlit typically runs at:

```text
http://localhost:8501
```

---

## AI Provider Configuration

Edit in-app at **Settings** page (recommended), or edit `config.json` manually.

### OpenAI
- Add API key
- Set model and base URL

### Anthropic
- Add API key
- Set model and base URL

### Ollama
- Ensure Ollama service is running locally
- Set model and endpoint (`http://localhost:11434/api/chat`)

### Custom API
- Provide URL, model, headers JSON, payload template JSON
- Placeholders: `{prompt}`, `{model}`

---

## Notes

- For classification targets in text form, labels are encoded automatically.
- Batch prediction requires matching input columns used during training.
- Deep learning tab uses one-hot encoding for non-numeric features.
- Saved models are stored in `saved_models/`.

---

## Troubleshooting

- **XGBoost errors**: ensure `xgboost` installed successfully.
- **TensorFlow install issues**: match Python version with TensorFlow compatibility.
- **API call failures**: verify API key, model name, and endpoint URL.

---

## License

Use and modify as needed for your own projects.
