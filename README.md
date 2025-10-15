# 🧠 CIFAR-100 Incremental Learning — Phase-Based Accuracy Analysis

## 📘 Project Overview
This project investigates **incremental learning** on the **CIFAR-100 dataset**, training a convolutional neural network (CNN) in two distinct phases.  
Each phase gradually increases the number of classes the model learns, allowing us to study how accuracy evolves as more data is introduced.

The implementation is done in **Google Colab** using **PyTorch**, and the dataset is imported directly from **Kaggle** via `kagglehub`.

---

## 📊 Dataset Information
- **Dataset:** CIFAR-100  
- **Total Superclasses:** 20  
- **Each Superclass:** Contains 5 subclasses (fine labels)  

### Assigned Superclasses — *Sanjana Kulkarni*
| Superclass | Classes (indices) |
|-------------|------------------|
| Aquatic mammals | 1–5 |
| Fish | 6–10 |
| Flowers | 11–15 |
| Food containers | 16–20 |
| Fruit and vegetables | 21–25 |

---

## ⚙️ Experimental Phases

### 🧩 **Phase 1**
1. Train the CNN on the **first 3 classes** of each of the 5 selected superclasses.  
2. Test the accuracy using images from only those 3 classes.  
3. Record the **Phase 1 Accuracy**.

### 🚀 **Phase 2**
1. Retrain the model on **all 5 classes** of the selected superclasses.  
2. Test the accuracy again and record the **Phase 2 Accuracy**.  
3. Compare the results:
   - Find the **accuracy difference** between Phase 1 and Phase 2.  
   - Determine the **number of epochs** in Phase 2 needed to achieve the same accuracy as Phase 1.

---

## 🧠 Methodology
- Dataset filtered by class indices for each phase.
- Training and testing performed with consistent architecture.
- Accuracy tracked across epochs for both phases.
- Comparison made to analyze incremental learning efficiency.

---

## 🧰 Tools & Libraries
| Tool | Purpose |
|------|----------|
| **PyTorch** | Model training & evaluation |
| **Torchvision** | Dataset utilities & transforms |
| **KaggleHub** | Download CIFAR-100 from Kaggle |
| **Matplotlib / NumPy** | Data visualization & numerical operations |
| **Google Colab** | Training environment |

---

## 🧮 Code Structure

### 📁 **Notebook Sections (Colab cells)**
1. **Import Dependencies**  
2. **Download Dataset (via KaggleHub)**  
3. **Define CIFAR-100 Class Mappings**  
4. **Filter Dataset for Selected Superclasses**  
5. **Define CNN Model Architecture**  
6. **Training & Evaluation Functions**  
7. **Phase 1 Execution**  
8. **Phase 2 Execution**  
9. **Plot Accuracy Comparison**  
10. **Analysis of Accuracy Difference**

---

## 📈 Example Results

| Phase | Classes Used | Accuracy | Epochs |
|:------|:--------------|:----------|:--------|
| **Phase 1** | 15 (3×5 superclasses) | 72.4% | 20 |
| **Phase 2** | 25 (5×5 superclasses) | 74.8% | 18 |

> 📌 *The actual results may vary based on hyperparameters and random seed.*

---

## 🧩 Key Insights
- Training on fewer classes gives higher per-class accuracy but lower generalization.  
- Introducing more classes requires more epochs to reach similar accuracy levels.  
- Phase-based learning helps measure model adaptability and incremental learning performance.

---

## 🧑‍💻 Author
**Sanjana Kulkarni**  
B.Tech in Computer Science  
Research Minor: Active Learning & AI Model Performance Analysis  

---

## 🧾 License
This project is released under the **MIT License**.  
Feel free to use and modify for educational or research purposes.

---

## 🌟 Acknowledgements
- **Dataset:** [CIFAR-100 — Kaggle (fedesoriano)](https://www.kaggle.com/datasets/fedesoriano/cifar100)  
- **Framework:** [PyTorch](https://pytorch.org/)  
- **Notebook Environment:** [Google Colab](https://colab.research.google.com/)
