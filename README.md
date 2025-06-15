# 🚫 Vulgar Phrase Detector using DistilBERT

An open-source Natural Language Processing (NLP) project that identifies and classifies vulgar or offensive phrases using [DistilBERT](https://huggingface.co/distilbert-base-uncased).  
This project is designed to support moderation systems, intelligent bots, and content filters by detecting inappropriate language in real time.

<p align="center">
  <img src="https://img.shields.io/github/license/virendra-tarate/vulgar-phrase-detector" />
  <img src="https://img.shields.io/github/stars/virendra-tarate/vulgar-phrase-detector" />
  <img src="https://img.shields.io/github/forks/virendra-tarate/vulgar-phrase-detector" />
</p>

---

## 🔍 Features

- ✅ Built using `DistilBERT`, a lighter, faster variant of BERT
- 📊 Binary classification: **Vulgar (1)** or **Non-Vulgar (0)**
- 📁 Includes notebook, dataset, and pre-trained model (downloadable via release)
- ⚙️ Easily extendable with your own dataset or architecture
- 🤝 Open to contributions and community support

---

## 📁 Project Structure

vulgar-phrase-detector/  
├── data/  
│ └── dataset.csv   
├── vulgar_detector.ipynb  
├── requirements.txt  
├── README.md  
└── LICENSE  


---

## 📊 Dataset

The model is trained on a custom dataset of **8,334 text entries** labeled as:

- `0`: Non-vulgar
- `1`: Vulgar

The dataset is included under `data/dataset.csv`.  
We welcome contributions to expand and diversify the dataset! 🙌

---

## 📥 Download the Trained Model

Due to GitHub's 100MB file limit, the trained model is stored under **Releases**.

👉 [Download model.zip from the latest release](https://github.com/virendra-tarate/vulgar-phrase-detector/releases/latest)

### After Downloading:
1. Extract `model.zip`
2. Place the extracted `model/` folder in the root of your project.

---

## 🚀 How to Run

### 1. Clone the Repo

```bash
git clone https://github.com/virendra-tarate/vulgar-phrase-detector.git
cd vulgar-phrase-detector
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run Prediction

```Python
from transformers import pipeline

classifier = pipeline("text-classification", model="./abuse_detection_model", tokenizer="./abuse_detection_model")

print(classifier("You are big dick head"))
print(classifier("You are so helpful, thank you!"))

```

#### Expected Output:

```bash
[{'label': 'LABEL_1', 'score': 0.98}]  # Vulgar
[{'label': 'LABEL_0', 'score': 0.99}]  # Clean

```
---

## 📈 Future Improvements

- [ ] REST API deployment (e.g., FastAPI)
- [ ] Data augmentation & multilingual support
- [ ] Browser extension for live moderation
- [ ] Multi-label detection: hate speech, spam, etc.

---

## 🤝 Contributing

We welcome all contributions, from adding new data to improving the model.

### How to Contribute

1. **Fork** the repository
2. **Create a branch**: `git checkout -b feature/your-feature`
3. **Commit your changes**: `git commit -m "Add feature"`
4. **Push to your branch**: `git push origin feature/your-feature`
5. **Open a Pull Request**

---

## 🛡 License

This project is licensed under the [MIT License](./LICENSE).

---

## 🙋 Contact

- 👤 Maintainer: [Virendra Tarate](https://github.com/virendra-tarate)
- 📧 Email: virendratarte22@gmail.com

---

## 🙌 Acknowledgements

- [HuggingFace Transformers](https://huggingface.co/transformers/)
- [Google Colab](https://colab.research.google.com/)
- The open-source community ❤️


> _Let’s build a cleaner, more respectful internet together._
