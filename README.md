# 📰 AI Fake News Detector

An **AI-powered Fake News Detection web application** that uses a Neural Network to classify news headlines/text as **REAL** or **FAKE**.

The model is trained **directly inside the web browser** using **TensorFlow.js**, so no Python backend or external server is required.

---

## 🚀 Features

* 🤖 AI-powered news classification
* 🧠 Neural Network using TensorFlow.js
* 🌐 Runs completely in the browser
* 📊 Trained on **5,000 news headlines**

  * 2,500 Real
  * 2,500 Fake
* 🔤 Automatic text tokenization and vocabulary creation
* 📏 Text padding/truncation to a fixed sequence length
* 🎯 Binary classification: **REAL / FAKE**
* 📈 Displays prediction confidence
* ⚡ No backend required
* 💻 Simple and responsive web interface

---

## 🧠 How It Works

The application follows these main steps:

```text
News Dataset
     ↓
Create Vocabulary
     ↓
Convert Text → Numerical Sequences
     ↓
Padding / Truncation
     ↓
Embedding Layer
     ↓
Flatten Layer
     ↓
Dense Neural Network
     ↓
Sigmoid Output
     ↓
REAL / FAKE Prediction
```

The application uses an **Embedding → Flatten → Dense → Dropout → Dense** architecture.

The model is compiled using:

* **Optimizer:** Adam
* **Loss:** Binary Cross Entropy
* **Metric:** Accuracy
* **Epochs:** 25
* **Batch Size:** 32
* **Validation Split:** 10%

The model architecture and training configuration are implemented directly in the JavaScript code.

---

## 📚 Dataset

The project uses news data sampled from:

```text
True.csv
Fake.csv
```

The application contains:

```text
5,000 total examples
├── 2,500 Real News
└── 2,500 Fake News
```

Each news item has:

```javascript
{
    text: "News headline...",
    label: 1
}
```

where:

```text
1 → Real News
0 → Fake News
```

The project description and dataset labeling are defined in the application itself.

---

## 🛠️ Technologies Used

| Technology      | Purpose                |
| --------------- | ---------------------- |
| HTML5           | Webpage structure      |
| CSS3            | User interface styling |
| JavaScript      | Application logic      |
| TensorFlow.js   | Machine Learning       |
| Neural Networks | Text classification    |

TensorFlow.js is loaded directly from a CDN in the application.

---

## 🧩 Model Architecture

The neural network consists of the following layers:

```text
Input
  ↓
Embedding
  ↓
Flatten
  ↓
Dense (32 neurons, ReLU)
  ↓
Dropout (30%)
  ↓
Dense (1 neuron, Sigmoid)
  ↓
Prediction
```

### Embedding Layer

Converts word IDs into numerical vector representations.

```text
Embedding Dimension = 16
```

### Dense Layer

A fully connected layer with:

```text
32 neurons
Activation: ReLU
```

### Dropout

A dropout rate of:

```text
30%
```

is used during training to help reduce overfitting.

### Output Layer

The final layer contains one neuron using the **Sigmoid** activation function.

```text
Output → value between 0 and 1
```

The application interprets:

```text
Score > 0.5 → REAL NEWS
Score ≤ 0.5 → FAKE NEWS
```

---

## 🖥️ User Interface

The application provides two main steps.

### 1. Train AI Model

Click:

```text
Train AI Model
```

The browser creates the vocabulary, prepares the dataset, builds the neural network and trains the model.

Training progress is displayed on the page, including:

* Epoch
* Training Accuracy
* Validation Accuracy
* Loss

### 2. Enter News

After training is completed, enter a news headline or text.

Example:

```text
German foreign ministers meet after detainee released...
```

Then click:

```text
Predict Fake/Real
```

The application displays the classification and confidence percentage.

---

## 📁 Project Structure

```text
AI-Fake-News-Detector/
│
├── index.html
└── README.md
```

The main application, including the HTML, CSS, JavaScript, dataset and machine-learning model, is contained in `index.html`.

---

## ▶️ How to Run

### Option 1 — Open Directly

Simply open:

```text
index.html
```

in a modern web browser.

No Python installation is required.

No Node.js installation is required.

No backend server is required.

---

### Option 2 — VS Code

1. Open the project folder in VS Code.
2. Open `index.html`.
3. Use **Live Server** if installed.
4. Open the generated local URL.
5. Click **Train AI Model**.
6. Wait for training to complete.
7. Enter a news headline.
8. Click **Predict Fake/Real**.

---

## ⚠️ Important Limitation

This project is an **educational/demo machine-learning application**, not a definitive fact-checking system.

The model learns patterns from its training dataset. A prediction of:

```text
REAL NEWS
```

does **not** prove that the news is factually true.

Likewise:

```text
FAKE NEWS
```

does not independently verify that the claim is false.

For real-world fact checking, information should be verified using reliable sources and independent evidence.

---

## 🔮 Future Improvements

Possible improvements include:

* [ ] Use a larger and more diverse dataset
* [ ] Add a proper train/test split
* [ ] Add precision, recall and F1-score
* [ ] Add confusion matrix visualization
* [ ] Improve text preprocessing
* [ ] Use TF-IDF or more advanced NLP techniques
* [ ] Use pretrained NLP models
* [ ] Add multilingual news detection
* [ ] Add URL-based article analysis
* [ ] Add source credibility analysis
* [ ] Add explainable AI features
* [ ] Deploy the application online
* [ ] Add a backend API for scalable inference

---

## 🎯 Project Objective

The main objective of this project is to demonstrate how **Machine Learning and Natural Language Processing concepts can be implemented directly in a web browser**.

It combines:

```text
Web Development
       +
JavaScript
       +
Natural Language Processing
       +
Neural Networks
       +
TensorFlow.js
```

into a single interactive application.

---

## 👨‍💻 Author

**Shikhar Khare**

B.Tech CSE (AI) Student

Interested in:

* Artificial Intelligence
* Machine Learning
* Data Science
* Web Development
* Software Development

---

## ⭐ Project

If you found this project useful or interesting, consider giving the repository a ⭐ on GitHub.

---


