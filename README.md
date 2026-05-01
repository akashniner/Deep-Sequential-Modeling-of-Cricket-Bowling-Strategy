
# 🏏 Deep Sequential Modeling of Cricket Bowling Strategy

## 📖 Overview

Cricket bowling is a sequential decision-making process where each delivery depends on previous balls, match context, and tactical intent. Traditional statistical approaches fail to capture these temporal dependencies effectively.

This project applies deep learning-based sequence models—**RNN, LSTM, and GRU**—to predict bowling strategies using ball-by-ball cricket data.

---

## 🎯 Objective

Given a sequence of previous deliveries, predict the next ball’s:

* 📍 Line
* 📏 Length
* ⚡ Speed

Additionally, compare the performance of:

* Simple RNN
* LSTM
* GRU

---

## ✨ Features

* Sequential modeling using sliding window approach
* Multi-output prediction (line, length, speed)
* Implementation of RNN, LSTM, and GRU architectures
* Model comparison using evaluation metrics
* Rolling prediction for future sequence simulation
* End-to-end deep learning pipeline

---

## 🧠 Model Architectures

### 🔹 Simple RNN

* SimpleRNN (64 units)
* Dense (32, ReLU)
* Output Dense (3)

### 🔹 LSTM

* LSTM (64 units)
* Dense (32, ReLU)
* Output Dense (3)

### 🔹 GRU

* GRU (64 units)
* Dense (32, ReLU)
* Output Dense (3)

---

## 📊 Dataset

* Ball-by-ball cricket dataset (Excel format)

### Features Used:

* Line
* Length
* Speed
* Over number
* Ball number

---

## ⚙️ Data Preprocessing

* Sorted by match, over, and ball
* Normalized using MinMaxScaler
* Converted into sequences using sliding window

### Sequence Setup:

* Input: 6 previous balls → shape `(6, 5)`
* Output: Next ball → shape `(3)`

---

## 🧪 Training Details

* **Loss Function:** Mean Squared Error (MSE)
* **Optimizer:** Adam
* **Epochs:** 10
* **Batch Size:** 32
* **Train-Test Split:** 80% training / 20% testing

---

## 📈 Evaluation Metrics

* Mean Squared Error (MSE)
* R² Score

---

## 📉 Results

* RNN → Highest error
* GRU → Better than RNN
* LSTM → Best performance (lowest MSE)

⚠️ **Key Observation:**
All models produced **negative R² scores**, indicating limited predictive capability.

---

## 🔁 Rolling Prediction

A rolling prediction approach was implemented:

* Input: First 6 balls
* Output: Next 18 balls (predicted sequentially)

This demonstrates real-world forecasting of bowling strategies.

---

## 💡 Insights

* Sequential models capture temporal patterns in cricket data
* LSTM performs slightly better due to memory mechanisms
* GRU provides faster training with comparable results

---

## ⚠️ Limitations

Model performance is limited due to lack of contextual features such as:

* Batsman type
* Field placement
* Match situation and pressure
* Bowler intent

---

## 🚧 Challenges Faced

* Data preprocessing and normalization
* Sequence generation complexity
* Low model performance despite training

---

## 🔮 Future Work

* Incorporate richer contextual features
* Apply attention mechanisms or Transformers
* Improve feature engineering
* Hyperparameter tuning for better performance

---

## 🛠️ Tech Stack

* Python
* TensorFlow / Keras
* NumPy
* Pandas
* Scikit-learn
* Matplotlib

---

## 📂 Project Structure

```
project/
│── data/
│── notebooks/
│── models/
│── utils/
│── results/
│── README.md
```

---

## 👨‍🎓 Author

**Akash N**
DA25M536
Indian Institute of Technology Madras

---

## 📚 Course

DA6401W – Deep Learning
Project Submission – April 2026

---

## 📜 License

This project is for academic and educational purposes only.

---


