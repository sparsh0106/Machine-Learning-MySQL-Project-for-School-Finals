# 🗄️ Machine Learning & MySQL Prediction System (Tkinter GUI)

A desktop application developed for the Class 12 Computer Science finals project that integrates a **Tkinter GUI**, **scikit-learn Linear Regression**, and a **MySQL relational database** (`mysql-connector-python`). Users can input 10 sequential data values to forecast the next value, inspect model $R^2$ accuracy, and persist/query historical prediction records in MySQL.

---

## 📂 Repository Structure

- `main.py`: Complete Tkinter GUI, `scikit-learn` Linear Regression model, and MySQL database CRUD integration.
- `README.md`: Project overview and setup instructions.

---

## ✨ Key Features

- **Real-Time Linear Regression**: Accepts 10 numerical inputs, fits a `LinearRegression` model, predicts the $11^{	ext{th}}$ value, and computes $R^2$ accuracy.
- **MySQL Persistence**: Connects to a local MySQL database (`old_results`) to log predictions and retrieve past runs (`SELECT * FROM ReSuLt`) in a dedicated history window.
- **Full-Screen Desktop Interface**: Built with Tkinter (`1600x900`) for classroom demonstration.

---

## 🚀 Getting Started

### 1. Prerequisites
Ensure you have Python 3 and a local MySQL server running with a database named `old_results` and table `ReSuLt`:
```sql
CREATE DATABASE IF NOT EXISTS old_results;
USE old_results;
CREATE TABLE IF NOT EXISTS ReSuLt (
    Prediction VARCHAR(255),
    Accuracy VARCHAR(255)
);
```

### 2. Install Python Dependencies
```bash
pip install mysql-connector-python pandas numpy scikit-learn
```

### 3. Run the Application
Update the `ms.connect(...)` credentials in `main.py` to match your local MySQL user/password, then run:
```bash
python main.py
```

---

## 👤 Author

**Sparsh Agarwal** — [GitHub](https://github.com/sparsh0106)
