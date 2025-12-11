# Netflix Age Rating Classification using MLP

This project builds a machine-learning pipeline to **predict age certifications** (e.g., TV-MA, PG-13, TV-14) for Netflix titles based solely on their **text descriptions**.  
It uses **TF–IDF text vectorization** and a **Multilayer Perceptron (MLP)** classifier to model rating categories from plot summaries.

📄 This work is based on the analysis and methodology described in the accompanying project report.

---


## 🚀 Objective

The goal of this project is to demonstrate a complete NLP + neural network workflow:

- Preprocess Netflix text descriptions  
- Convert them into numerical features using **TF–IDF**  
- Train an **MLP classifier** to predict age ratings  
- Evaluate model performance using accuracy, classification report, and confusion matrix  

---

## 📊 Dataset

The dataset contains Netflix metadata, including:

- `description`
- `age_certification`
- `type`
- `runtime`
- `IMDb score`

Only the **description** and **age_certification** fields are used here.  
To reduce imbalance, the **top 6 most frequent rating labels** are retained.

---

## 🔧 Methodology

### 1️⃣ Preprocessing
- Remove missing descriptions or ratings  
- Convert descriptions to string  
- Filter to top age certification categories  
- Stratify train-test split (80/20)

### 2️⃣ Feature Extraction — TF–IDF  
Configured with:

- `max_features = 10000`
- English stopword removal

### 3️⃣ Model — Multilayer Perceptron  
Key hyperparameters:

- Hidden layers: `(128,)`
- Activation: ReLU  
- Optimizer: Adam  
- Epochs: 20  
- Random State: 42  

MLP is embedded in a Scikit-learn Pipeline.

---

## 📈 Results

- **Accuracy:** (insert result here)
- **Classification Report:** shows performance per rating class  
- **Confusion Matrix:** indicates confusion mainly between TV-14 and TV-MA  

See the full report for detailed explanations. :contentReference[oaicite:2]{index=2}

---

## 🧠 Future Improvements

- Deeper or wider neural networks  
- Use embeddings (Word2Vec, GloVe, BERT)  
- Oversampling or class weights  
- Hyperparameter tuning  
- Add auxiliary metadata features  

---

## ⚖️ Ethical Considerations

- Automated rating systems should **support** human evaluators, not replace them  
- Misclassification risks exposing younger audiences to inappropriate content  
- Dataset bias must be handled carefully  

---

## 📚 References

- Scikit-learn Documentation  
- Netflix Movies & TV Shows Dataset (Kaggle Variant)  
- Speech and Language Processing – Jurafsky & Martin  
- Pattern Recognition and Machine Learning – Bishop  

---

## 📎 GitHub Repository

You can find the repository link:
https://github.com/savaramsuryateja/Machine-Learning.git

---

## 📝 License

This project is released under the **MIT License**.  
See the `LICENSE` file for details.
