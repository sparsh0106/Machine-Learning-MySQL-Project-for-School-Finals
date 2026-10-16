# Linear Regression with MySQL History

A Tkinter coursework application that fits a scikit-learn Linear Regression model to ten user-entered values, predicts the next value, and stores prediction history in MySQL.

## Prerequisites

- Python with Tkinter
- A running MySQL server
- The Python packages below

```bash
python -m pip install mysql-connector-python pandas numpy scikit-learn
```

Create the database and table expected by the application:

```sql
CREATE DATABASE IF NOT EXISTS old_results;
USE old_results;

CREATE TABLE IF NOT EXISTS ReSuLt (
    Prediction DOUBLE NOT NULL
);
```

## Configure the connection

The application reads connection settings from environment variables. It defaults to host `localhost` and database `old_results`; set the user and password for your local MySQL installation.

**Linux or macOS**
```bash
export MYSQL_HOST=localhost
export MYSQL_USER=your_mysql_user
export MYSQL_PASSWORD=your_mysql_password
export MYSQL_DATABASE=old_results
```

**Windows PowerShell**
```powershell
$env:MYSQL_HOST = "localhost"
$env:MYSQL_USER = "your_mysql_user"
$env:MYSQL_PASSWORD = "your_mysql_password"
$env:MYSQL_DATABASE = "old_results"
```

Run the GUI:

```bash
python main.py
```

Keep real database credentials out of source control. The model's displayed (R^2) score is computed on its training subset and should not be interpreted as test accuracy.
