# 🩺 Anemia Detection from Lip Images

Predicting hemoglobin levels using computer vision and machine learning to detect anemia from lip images.

---

## 📋 Project Overview

This project uses advanced machine learning techniques to predict hemoglobin (HgB) levels from lip images, enabling non-invasive anemia screening. The analysis explores both:

- **Regression:** Predicting exact HgB values (g/dL)
- **Classification:** Detecting anemia (anemic vs. not anemic)

### Key Features:

- ✅ 94 advanced image features (color spaces, texture, spatial analysis)
- ✅ State-of-the-art models (XGBoost, LightGBM, CatBoost)
- ✅ Proper cross-validation (Leave-One-Group-Out)
- ✅ Comprehensive exploratory data analysis
- ✅ Professional visualizations and reporting

---

## 🚀 Quick Start Guide

### Prerequisites

- **Python 3.8+** (Python 3.10 or higher recommended)
- **Git** (for cloning the repository)
- **Jupyter Notebook** or **VS Code** with Jupyter extension

### Step 1: Clone the Repository

```bash
git clone https://github.com/alanantony24/DSA-Code.git
cd DSA-Code
```

### Step 2: Install Required Dependencies

#### Option A: Install Core Dependencies (Minimum)

```bash
pip install pandas numpy opencv-python scikit-learn matplotlib pillow pillow-heif scipy
```

#### Option B: Install All Dependencies (Recommended)

```bash
pip install pandas numpy opencv-python scikit-learn matplotlib pillow pillow-heif scipy xgboost lightgbm catboost
```

**Note:** The notebook will automatically install XGBoost, LightGBM, and CatBoost if they're not present.

### Step 3: Ensure Image Files are Present

Make sure you have the `images/` folder in the same directory as `analysis.ipynb` with your lip image files (.jpg, .jpeg, .heic).

### Step 4: Run the Notebook

#### Using Jupyter Notebook:

```bash
jupyter notebook analysis.ipynb
```

#### Using VS Code:

1. Open `analysis.ipynb` in VS Code
2. Select Python kernel (Python 3.8+)
3. Run all cells: Press `Ctrl+Shift+P` → "Notebook: Run All"

---

## 📂 Project Structure

```
DSA-Code/
│
├── analysis.ipynb           # Main Jupyter notebook with complete analysis
├── readme.md               # This file
├── ANALYSIS_SUMMARY.md     # Detailed findings and recommendations
│
├── images/                 # Lip images dataset
│   ├── HgB_*.heic
│   ├── HgB_*.jpg
│   └── Random_*.jpg
│
└── Output Files (generated after running):
    ├── predictions.csv          # Model predictions
    ├── model_comparison.csv     # Performance comparison
    ├── model_performance.png    # Visualization
    └── feature_importance.png   # Feature analysis
```

---

## 🔬 How to Use the Notebook

### Running All Cells (Recommended for First Time)

1. **Open the notebook:** `analysis.ipynb`
2. **Run all cells in order:** Click "Run All" or execute cells sequentially
3. **Wait for execution:** The full analysis takes ~2-5 minutes
4. **Review results:** Scroll through to see visualizations and metrics

### Section-by-Section Execution

The notebook is organized into 8 main sections:

1. **📚 Setup:** Import libraries
2. **📂 Data Loading:** Load and parse image files
3. **📊 EDA:** Explore data distribution
4. **🔬 Feature Engineering:** Extract 94 image features
5. **⚙️ Feature Extraction:** Process all images
6. **🤖 ML Models (Regression):** Train baseline models
7. **🚀 Advanced Models:** XGBoost, LightGBM, CatBoost
8. **📈 Specialized Analysis:** Binary classification alternative

**Tip:** You can run sections independently, but ensure you run Sections 1-5 first!

---

## 📊 Expected Results

### Regression Approach

- **Best Model:** XGBoost_v2
- **MAE:** ~1.88 g/dL (Target: ≤0.8 g/dL)
- **Challenge:** Limited data (31 images from 23 individuals)

### Classification Approach

- **Best Model:** Logistic Regression
- **Accuracy:** ~71% (Target: 80%+)
- **More achievable** with current limited dataset

---

## 🛠️ Troubleshooting

### Issue: "ModuleNotFoundError: No module named 'pillow_heif'"

**Solution:**

```bash
pip install pillow-heif
```

### Issue: "ModuleNotFoundError: No module named 'xgboost'"

**Solution:** The notebook auto-installs these, but you can manually install:

```bash
pip install xgboost lightgbm catboost
```

### Issue: Images not loading

**Solution:**

- Ensure the `images/` folder is in the same directory as the notebook
- Check that image files have correct extensions (.jpg, .jpeg, .heic)

### Issue: Kernel crashes or memory errors

**Solution:**

- Restart kernel: `Kernel → Restart Kernel`
- Close other applications to free up memory
- Use a machine with at least 4GB RAM

---

## 📈 Output Files

After running the notebook, you'll get:

1. **predictions.csv** - Individual predictions for each image
2. **model_comparison.csv** - Performance metrics for all models
3. **model_performance.png** - Visualization of model results
4. **feature_importance.png** - Most important features for prediction

---

## 🎯 Key Findings

- **Limited Data Challenge:** With only 31 images from 23 individuals, achieving clinical-grade accuracy (MAE ≤ 0.8 g/dL) is extremely difficult
- **Best Performance:** Advanced gradient boosting models (XGBoost, LightGBM) perform best
- **Classification Alternative:** Binary classification (anemic vs. not anemic) is more achievable with limited data
- **Recommendation:** Collect 200-500+ images with standardized conditions for production-ready model

See `ANALYSIS_SUMMARY.md` for detailed findings and recommendations.

---

## 📚 Dependencies Reference

| Package       | Version | Purpose               |
| ------------- | ------- | --------------------- |
| pandas        | Latest  | Data manipulation     |
| numpy         | Latest  | Numerical operations  |
| opencv-python | Latest  | Image processing      |
| scikit-learn  | Latest  | ML models and metrics |
| matplotlib    | Latest  | Visualizations        |
| pillow        | Latest  | Image handling        |
| pillow-heif   | Latest  | HEIC image support    |
| scipy         | Latest  | Statistical functions |
| xgboost       | Latest  | Gradient boosting     |
| lightgbm      | Latest  | Gradient boosting     |
| catboost      | Latest  | Gradient boosting     |

---

## 👨‍💻 Author

**Alan Antony**

- GitHub: [@alanantony24](https://github.com/alanantony24)
- Repository: [DSA-Code](https://github.com/alanantony24/DSA-Code)

---

## 📝 License

This project is for educational and research purposes.

---

## 🤝 Contributing

Issues and suggestions are welcome! Please open an issue or submit a pull request.

---

**Note:** This is a research project demonstrating ML capabilities. For production medical applications, significantly more data, clinical validation, and regulatory approval would be required.
