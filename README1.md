# 🌳 Decision Tree Classifiers with Jupyter Notebooks  

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)  
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)  
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML%20Library-yellow?logo=scikit-learn)  
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple?logo=pandas)  
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green?logo=plotly)  

This repository contains two projects demonstrating the use of **Decision Tree Classifiers** on well-known datasets using **Python** and **Jupyter Notebooks**.  

---

## 📂 Projects  

### 🔹 1. Decision Tree Classifier on the *Iris Dataset*  
- **Dataset**: The [Iris dataset](https://scikit-learn.org/stable/datasets/toy_dataset.html#iris-plants-dataset) is a classic dataset used in pattern recognition, containing 150 samples of iris flowers from three species (*setosa*, *versicolor*, *virginica*).  
- **Features**:  
  🌸 Sepal length  
  🌸 Sepal width  
  🌸 Petal length  
  🌸 Petal width  
- **Target**: Species of Iris flower.  
- **Notebook Highlights**:  
  ✅ Dataset exploration  
  ✅ Train-test split  
  ✅ Decision Tree Classifier with `scikit-learn`  
  ✅ Tree visualization & performance evaluation  

---

### 🔹 2. Decision Tree Classifier on the *Titanic Dataset*  
- **Dataset**: The [Titanic dataset](https://www.kaggle.com/c/titanic) contains passenger information from the Titanic disaster, including survival outcome.  
- **Features (examples)**:  
  🚢 Passenger class (`Pclass`)  
  🚢 Sex  
  🚢 Age  
  🚢 Fare  
  🚢 Embarked location  
- **Target**: Survival status → (0 = Did not survive, 1 = Survived).  
- **Notebook Highlights**:  
  ✅ Data preprocessing (missing values, categorical encoding)  
  ✅ Exploratory Data Analysis (EDA)  
  ✅ Training a Decision Tree Classifier  
  ✅ Visualization of decision paths  
  ✅ Evaluation with accuracy, precision, recall & confusion matrix  

---
                       [ Is PetalLength <= 2.45? ]
                          /                   \
                     Yes /                     \ No
                        /                       \
                 [Predict: setosa]      [ Is PetalWidth <= 1.75? ]
                                         /                    \
                                    Yes /                      \ No
                                       /                        \
                            [ Is PetalLength <= 4.95? ]      [Predict: virginica]
                                /             \
                           Yes /               \ No
                              /                 \
                [Predict: versicolor]     [Predict: virginica]

----------------------------  TITANIC (illustrative) ----------------------------

                       [ Is Sex == male? ]
                          /           \
                      Yes /             \ No
                         /               \
        [ Is Pclass == 1 or 2? ]      [Predict: Survived]
           /           \ 
         Yes           No
         /               \
[ Is Age <= 15? ]     [Predict: Did not survive]
   /     \
 Yes     No
 /         \
[Predict: Survived] [Predict: Did not survive]


Iris Dataset 🌸

Achieves high accuracy in classifying flower species.

Clear decision boundaries visible in the decision tree visualization.

Titanic Dataset 🚢

Captures key survival factors (e.g., class, sex, age).

Shows the interpretability of decision trees but also their tendency to overfit complex datasets.

📝 Notes

🛠 Titanic dataset requires preprocessing due to missing values & categorical variables.

🌳 Decision Trees are prone to overfitting → tune hyperparameters (max_depth, min_samples_split) for better generalization.

🔍 Visualizations are essential for interpreting decision paths and feature importance.

✨ Enjoy exploring Decision Trees! ✨
