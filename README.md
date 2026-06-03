# ✍️ Handwritten Digits Recognition

## Project Overview
Image classification project to recognise handwritten digits (0–9) from the
MNIST dataset using classical ML models and a CNN deep learning model.

## Tasks Completed
| Task | Description |
|------|-------------|
| Task 1 | Complete EDA — 6 charts including pixel analysis, PCA variance, average digit images |
| Task 2 | Classify digits 0–9 using 6 ML models + 1 CNN |
| Task 3 | Model comparison report with production recommendation |
| Bonus  | Challenges Report inside notebook |

## Dataset
- **Source:** [Download Here](https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1002-HandwrittenDigits.zip)
- **OR:** Auto-downloaded from `keras.datasets.mnist`
- **Size:** 70,000 images (60,000 train + 10,000 test)
- **Image size:** 28×28 pixels, grayscale

## Project Structure
```
PRCP-1002-HandwrittenDigits/
│
├── PRCP-1002-HandwrittenDigits.ipynb   ← Main notebook (all tasks)
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/                    ← Optional: place downloaded zip here
│
├── plots/                   ← Auto-generated when notebook runs
│   ├── 01_sample_digits.png
│   ├── 02_class_distribution.png
│   └── ...
│
└── models/                  ← Auto-generated when notebook runs
    ├── random_forest_mnist.pkl
    ├── svm_mnist.pkl
    ├── pca_transform.pkl
    └── cnn_mnist.h5
```

## How to Run

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/PRCP-1002-HandwrittenDigits.git
cd PRCP-1002-HandwrittenDigits
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook PRCP-1002-HandwrittenDigits.ipynb
```
Then: **Kernel → Restart & Run All**

> Dataset auto-downloads from Keras — no manual download needed!

## Models Trained
| Model | Expected Accuracy |
|---|---|
| Logistic Regression | ~92% |
| Decision Tree | ~87% |
| Random Forest | ~97% |
| KNN (k=5) | ~96% |
| SVM (RBF) | ~97% |
| Gradient Boosting | ~95% |
| **CNN (Deep Learning)** | **~99%** |

## Key Techniques Used
- **PCA** — Reduced 784 features to ~154 (95% variance)
- **Dropout + BatchNorm** — Prevents CNN overfitting
- **Stratified subset** — 15k samples for slow models (SVM, KNN)

## Production Recommendation
- **Best accuracy:** CNN (~99%)
- **Lightweight deployment:** Random Forest + PCA (~97%)

## Author
**Patil Shreyash**
B.Tech — Computer Science Engineering, 2025
📧 Shreyashkp96@gmail.com
