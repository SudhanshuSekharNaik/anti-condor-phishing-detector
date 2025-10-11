# ANTI-CONDOR: Phishing URL Detection System

A machine learning-based phishing detection system that uses Random Forest algorithm to identify malicious URLs in real-time. This implementation analyzes URL characteristics to distinguish between legitimate and phishing websites with high accuracy.

## 🚀 Features

- **Real-time URL Analysis**: Instant phishing detection
- **17 Feature Extraction**: Comprehensive URL characteristic analysis
- **Random Forest Algorithm**: Ensemble learning for robust classification
- **Interactive Testing**: Test any URL directly
- **Visual Analytics**: Comprehensive performance metrics and graphs

## 📊 Model Performance Results

### Evaluation Metrics
- **Accuracy**: 92.5%
- **Precision**: 90.3%
- **Recall**: 95.0%
- **F1-Score**: 92.6%

The model demonstrates excellent performance in detecting phishing URLs while maintaining low false positive rates, making it suitable for real-world deployment.

## 📈 Graph Explanations

<img width="1490" height="1181" alt="image" src="https://github.com/user-attachments/assets/1366128f-2707-4394-bdde-35860d2fd139" />


### 1. Confusion Matrix
**Purpose**: Shows model classification performance
- **True Positives (TP)**: Correctly identified phishing URLs
- **True Negatives (TN)**: Correctly identified legitimate URLs
- **False Positives (FP)**: Legitimate URLs misclassified as phishing
- **False Negatives (FN)**: Phishing URLs missed by the model

**Outcome**: The matrix shows high diagonal values (correct predictions) and low off-diagonal values (errors), indicating reliable classification.

### 2. Feature Importance
**Purpose**: Identifies which URL features contribute most to detection
- **Key Features**: URL length, special character counts, entropy
- **Insight**: Longer URLs with special characters and high entropy are strong phishing indicators
- **Outcome**: Helps understand what makes a URL suspicious and guides feature engineering

### 3. URL Length Distribution
**Purpose**: Compares URL lengths between legitimate and phishing sites
- **Observation**: Phishing URLs are typically longer than legitimate ones
- **Reason**: Phishing sites often use long parameters, redirects, and obfuscation
- **Outcome**: URL length is a reliable distinguishing feature between the two classes

### 4. Feature Correlation Matrix
**Purpose**: Shows relationships between different URL features
- **High Correlation**: Features that move together (e.g., various special character counts)
- **Low Correlation**: Independent features that provide unique information
- **Outcome**: Ensures model uses diverse, non-redundant features for better generalization

## 🛠️ Installation

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## 💻 Usage

```python
from phishing_detector import PhishingDetector

# Initialize detector
detector = PhishingDetector()

# Train model (with your dataset)
detector.train_model(X_train, y_train)

# Predict URL
prediction, probability = detector.predict("https://example.com")
print(f"Phishing: {prediction == 1}, Confidence: {probability[1]:.2%}")
```

## 📋 Feature Set

The system analyzes 17 URL characteristics:
- Structural features (length, subdomains, TLD)
- Security indicators (HTTPS, IP addresses)
- Content analysis (keywords, entropy)
- Pattern detection (special characters, shortening services)

## 🎯 Key Outcomes

1. **High Detection Rate**: 95% recall ensures most phishing attempts are caught
2. **Low False Positives**: 90% precision minimizes disruption to legitimate browsing
3. **Real-time Performance**: Processes URLs in milliseconds
4. **Interpretable Results**: Feature importance provides transparency
5. **Adaptive Learning**: Can be retrained with new phishing patterns

## 🔮 Future Enhancements

- Browser extension integration
- Deep learning models for improved accuracy
- Real-time threat intelligence updates
- Multi-language support for international phishing patterns

## 📝 License

This project is for educational and research purposes. Please cite appropriately if used in academic work.

---

**ANTI-CONDOR**: Protecting users from phishing threats one URL at a time.
