# 🛍️ Black Friday Sales Prediction

A machine learning project that predicts **customer purchase amounts during Black Friday sales** using customer demographics, occupation, location, and product-category information.

The project applies **Linear Regression** to learn the relationship between customer/product attributes and purchase amount, then evaluates the model on unseen test data.

---

## 📌 Project Overview

Black Friday shopping generates large amounts of transactional data containing information about customers, products, and their purchasing behaviour.

The goal of this project is to build a regression model that can:

* Predict the **purchase amount** for a customer-product combination
* Measure how well customer and product attributes explain purchasing behaviour
* Evaluate the prediction performance using standard regression metrics
* Generate purchase predictions for new customer records

### 🎯 Prediction Target

**Input:** Customer and product attributes

**Output:** Predicted `Purchase` amount

---

## 📊 Dataset

The project uses the **Black Friday Sales dataset**, containing **550,068 purchase transactions** and 12 attributes.

| Feature                      | Description                                |
| ---------------------------- | ------------------------------------------ |
| `User_ID`                    | Unique customer identifier                 |
| `Product_ID`                 | Unique product identifier                  |
| `Gender`                     | Customer gender                            |
| `Age`                        | Customer age group                         |
| `Occupation`                 | Customer occupation category               |
| `City_Category`              | Category of the customer's city            |
| `Stay_In_Current_City_Years` | Number of years living in the current city |
| `Marital_Status`             | Customer marital status                    |
| `Product_Category_1`         | Primary product category                   |
| `Product_Category_2`         | Secondary product category                 |
| `Product_Category_3`         | Tertiary product category                  |
| `Purchase`                   | Purchase amount — **prediction target**    |

The observed purchase values range from **12 to 23,961**, with an average purchase amount of approximately **9,264**.

---

## 🤖 Machine Learning Model

### Linear Regression

The project uses **Linear Regression** as the primary prediction model.

The model learns a relationship between the available customer/product features and the purchase amount.

The modelling pipeline includes:

* Categorical feature encoding
* Numerical feature transformation
* Feature scaling
* Linear Regression

The final model is implemented using `scikit-learn` and trained on the training dataset before being evaluated on unseen test data.

---

## 📈 Model Performance

The model was evaluated using three regression metrics:

| Metric       |       Result |
| ------------ | -----------: |
| **MAE**      | **2,208.91** |
| **RMSE**     | **2,946.09** |
| **R² Score** |   **0.6546** |

The model achieved an **R² score of 0.6546 on the test set**, meaning that the model explains approximately **65.46% of the variation in purchase amounts** in the test data.

### Train vs Test Performance

| Dataset  | R² Score |
| -------- | -------: |
| Training |   0.6619 |
| Testing  |   0.6546 |

The relatively close training and testing R² scores indicate that the model's performance is similar across the two datasets.

---

## 📉 Linear Regression Results

The following plot shows the relationship between the **actual purchase amounts** and the **predicted purchase amounts** produced by the Linear Regression model.

<img width="765" height="549" alt="image" src="https://github.com/user-attachments/assets/abb87525-7af1-4abe-8537-346eeacfcad4" />

---

## 🧰 Technologies Used

* **Python**
* **Pandas** — data handling
* **NumPy** — numerical computation
* **Matplotlib** — visualization
* **Seaborn** — exploratory visualization
* **Scikit-learn** — machine learning and evaluation
* **Jupyter Notebook** — experimentation and analysis
* **Power BI** — additional dashboard visualizations

---

## ▶️ Running the Project

### 1. Clone the repository

```bash
git clone https://github.com/simran2104/black-friday-sales-prediction.git
cd black-friday-sales-prediction
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the notebook

Open:

```text
Black-Friday-Sales-Prediction.ipynb
```

and execute the cells to train the model, evaluate its performance, visualize the predictions, and generate purchase predictions.

---

## 📊 Power BI Dashboard

The project also includes an interactive Power BI dashboard for exploring Black Friday sales patterns and customer purchasing behaviour.

<img width="1576" height="846" alt="image" src="https://github.com/user-attachments/assets/f25de568-1207-4ad7-995f-49941847dee9" />
