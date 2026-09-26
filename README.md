# 💰 Personal Expense Tracker

A **CLI-based Personal Expense Tracker** developed using **Python, SQLite, and Matplotlib**.  
The application allows users to record, manage, search, analyze, and visualize their personal expenses through a simple command-line interface.

The project stores all expense records permanently in an **SQLite database (`expenses.db`)** and can generate a **category-wise expense report** along with a **pie chart (`chart.png`)** showing the distribution of expenses.

---

## 📌 Project Overview

Managing daily expenses manually can make it difficult to understand where money is being spent. The **Personal Expense Tracker** provides a simple digital solution for recording and analyzing expenses.

The application allows users to:

- Add new expenses
- Store expenses in an SQLite database
- View all recorded expenses
- Search expenses by date
- Search expenses by category
- Generate category-wise expense summaries
- Calculate the percentage contribution of each category
- Generate a pie chart for visual analysis
- Delete/reset stored expenses

The project is designed as a **beginner-friendly Python CSE project** while demonstrating important programming concepts such as functions, database operations, SQL queries, exception handling, file management, and data visualization.

---

# 🎯 Objectives

The main objectives of this project are:

1. To develop a simple application for managing personal expenses.
2. To store expense information in a structured SQLite database.
3. To provide an easy-to-use command-line interface.
4. To allow users to search and filter expense records.
5. To calculate category-wise spending.
6. To display the percentage of total spending for each category.
7. To visualize expense distribution using a pie chart.
8. To demonstrate practical applications of Python programming and SQL.
9. To develop a project that can be maintained and extended with additional features.

---

# ✨ Features

## 1. ➕ Add Expense

Users can add a new expense by entering:

- Date
- Category
- Amount

Example:

```text
Date: 26-09-2026
Category: Food
Amount: 150
```

The information is then stored permanently in the SQLite database.

---

## 2. 📋 View All Expenses

The application displays all expenses stored in the database.

Example:

```text
------------------------------------------------
ID    Date          Category       Amount
------------------------------------------------
1     26-09-2026    Food           ₹150
2     26-09-2026    Travel         ₹80
3     25-09-2026    Shopping       ₹500
------------------------------------------------
```

---

## 3. 🔍 Search Expenses

Users can search for expenses using:

### Search by Date

Example:

```text
Enter date: 26-09-2026
```

The program displays all expenses recorded on that date.

### Search by Category

Example:

```text
Enter category: Food
```

The application displays all expenses belonging to the selected category.

SQL `LIKE` queries can be used to provide flexible searching.

---

## 4. 📊 Category-wise Expense Report

The program calculates the total amount spent in each category.

Example:

```text
Category        Total
-------------------------
Food            ₹2500
Travel          ₹1200
Shopping        ₹3500
Education       ₹1800
```

It also calculates the percentage contribution of each category to the overall expenditure.

### Percentage Formula

```text
Category Percentage =
(Category Total / Overall Total) × 100
```

Example:

```text
Food = ₹2500
Overall Expense = ₹10000

Percentage =
(2500 / 10000) × 100

= 25%
```

---

# 📈 Expense Visualization

The project uses **Matplotlib** to generate a pie chart representing the distribution of expenses across different categories.

The generated chart is saved as:

```text
chart.png
```

Example categories that can be visualized:

```text
Food
Travel
Shopping
Education
Bills
Entertainment
Health
Other
```

The chart makes it easier to understand which categories account for a larger portion of the total expenditure.

---

# 🗑️ Reset / Delete Expenses

The application provides an option to delete or reset stored expense records.

This can be useful when:

- Starting a new tracking period
- Removing old records
- Testing the application
- Clearing sample data

---

# 🛠️ Technologies / Tools Used

| Technology             | Purpose                                     |
| ---------------------- | ------------------------------------------- |
| Python 3.8+            | Main programming language                   |
| SQLite                 | Database for storing expenses               |
| `sqlite3`              | Python's built-in SQLite database module    |
| Matplotlib             | Data visualization and pie chart generation |
| SQL                    | Database queries and data manipulation      |
| Command Line Interface | User interaction                            |
| Git & GitHub           | Version control and project hosting         |

---

# 🐍 Python Concepts Used

This project demonstrates several important Python concepts:

### Variables

Used to store dates, categories, amounts, and other information.

### Functions

The application is divided into functions so that each operation can be performed independently.

Examples:

```python
add_expense()
view_expenses()
search_expenses()
generate_report()
```

### Conditional Statements

Used for menu selection and input validation.

```python
if choice == "1":
    add_expense()
elif choice == "2":
    view_expenses()
```

### Loops

Used for displaying records and processing database results.

### Exception Handling

Used to handle invalid input and prevent the program from terminating unexpectedly.

### Lists and Dictionaries

Used for temporarily storing and processing expense data.

### Modules

The project uses Python modules such as:

```python
sqlite3
datetime
matplotlib
```

---

# 🗄️ Database

The application uses **SQLite** as its database.

SQLite is lightweight, serverless, and included with Python through the built-in `sqlite3` module.

The database file is:

```text
expenses.db
```

---

## Database Table

The main expense table contains fields such as:

| Column     | Description                        |
| ---------- | ---------------------------------- |
| `id`       | Unique identifier for each expense |
| `date`     | Date on which the expense occurred |
| `category` | Expense category                   |
| `amount`   | Amount spent                       |

Example database record:

```text
ID: 1
Date: 26-09-2026
Category: Food
Amount: 150
```

---

# 🔎 SQL Concepts Used

The project demonstrates basic SQL operations.

### INSERT

Used to add an expense:

```sql
INSERT INTO expenses
(date, category, amount)
VALUES (?, ?, ?);
```

### SELECT

Used to retrieve expenses:

```sql
SELECT * FROM expenses;
```

### WHERE

Used for filtering:

```sql
SELECT * FROM expenses
WHERE category = ?;
```

### LIKE

Used for flexible searching:

```sql
SELECT * FROM expenses
WHERE category LIKE ?;
```

### DELETE

Used to remove records:

```sql
DELETE FROM expenses;
```

---

# 📁 Project Structure

The recommended project structure is:

```text
Personal-Expense-Tracker/
│
├── expense_tracker.py
├── chart.png
├── README.md
│
└── screenshots/
    ├── main_menu.png
    ├── add_expense.png
    ├── expense_list.png
    └── expense_report.png
```

### File Description

| File                 | Purpose                                    |
| -------------------- | ------------------------------------------ |
| `expense_tracker.py` | Main Python application                    |
| `expenses.db`        | SQLite database containing expense records |
| `chart.png`          | Generated expense visualization            |
| `README.md`          | Project documentation                      |
| `screenshots/`       | Project output screenshots                 |

---

# ⚙️ Installation

## 1. Install Python

Download and install **Python 3.8 or newer**.

Check whether Python is installed:

```bash
python --version
```

or:

```bash
python3 --version
```

---

## 2. Clone the Repository

Clone the project from GitHub:

```bash
git clone https://github.com/YOUR-USERNAME/Personal-Expense-Tracker.git
```

Move into the project directory:

```bash
cd Personal-Expense-Tracker
```

---

## 3. Create a Virtual Environment

Creating a virtual environment is optional but recommended.

### Windows

```bash
python -m venv .venv
```

Activate it:

```bash
.venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv .venv
```

Activate it:

```bash
source .venv/bin/activate
```

---

# ▶️ How to Run

After completing the installation steps, run:

### Windows

```bash
python expense_tracker.py
```

### macOS / Linux

```bash
python3 expense_tracker.py
```

The application will open in the terminal.

---

# 🖥️ Application Menu

The application provides options similar to:

```text
========================================
       PERSONAL EXPENSE TRACKER
========================================

1. Add Expense
2. View All Expenses
3. Search Expense
4. Generate Expense Report
5. Generate Pie Chart
6. Delete All Expenses
7. Exit

========================================
Enter your choice:
```

Select the required option by entering its corresponding number.

---

# 🧪 Example Workflow

A typical user session may look like this:

### Step 1 — Add Expense

```text
Enter date: 26-09-2026
Enter category: Food
Enter amount: 150

Expense added successfully!
```

### Step 2 — Add another expense

```text
Enter date: 26-09-2026
Enter category: Travel
Enter amount: 80

Expense added successfully!
```

### Step 3 — View Expenses

```text
ID    Date          Category       Amount
------------------------------------------------
1     26-09-2026    Food           ₹150
2     26-09-2026    Travel         ₹80
```

### Step 4 — Generate Report

```text
Category-wise Expense Report

Food       ₹150       65.22%
Travel     ₹80        34.78%

Total      ₹230
```

### Step 5 — Generate Chart

The program generates:

```text
chart.png
```

The chart visually represents the percentage of total expenses belonging to each category.

---

# 🔐 Data Storage

All expense information is stored locally in:

```text
expenses.db
```

This means the data remains available even after the program is closed.

The project does not require an external database server.

---

# 🧩 Functional Modules

The project can be divided into the following modules:

```text
                 Personal Expense Tracker
                          │
        ┌─────────────────┼─────────────────┐
        │                 │                 │
        ▼                 ▼                 ▼
   Expense Entry     Expense Search    Expense Analysis
        │                 │                 │
        ▼                 ▼                 ▼
     SQLite          Date/Category     Category Report
                                           │
                                           ▼
                                      Pie Chart
```

---

# 🧠 Program Flow

```text
START
  │
  ▼
Initialize SQLite Database
  │
  ▼
Display Main Menu
  │
  ▼
Get User Choice
  │
  ├── Add Expense
  │       │
  │       ▼
  │   Store in Database
  │
  ├── View Expenses
  │       │
  │       ▼
  │   Retrieve Records
  │
  ├── Search Expense
  │       │
  │       ▼
  │   Filter Database Records
  │
  ├── Generate Report
  │       │
  │       ▼
  │   Calculate Totals & Percentages
  │
  ├── Generate Chart
  │       │
  │       ▼
  │   Create Pie Chart
  │
  ├── Delete Expenses
  │       │
  │       ▼
  │   Remove Database Records
  │
  └── Exit
          │
          ▼
         END
```

---

# ✅ Input Validation

The application should validate user input before storing it.

Examples:

- Amount should be numeric.
- Amount should be greater than zero.
- Date should follow the expected format.
- Category should not be empty.
- Invalid menu choices should be handled.
- Database operations should handle errors safely.

Example:

```python
try:
    amount = float(input("Enter amount: "))

    if amount <= 0:
        print("Amount must be greater than zero.")

except ValueError:
    print("Please enter a valid amount.")
```

---

# 🚨 Error Handling

The project uses exception handling to prevent common runtime errors.

For example:

```python
try:
    amount = float(input("Enter amount: "))
except ValueError:
    print("Invalid amount entered.")
```

This improves the reliability and user experience of the application.

---

# 📊 Data Analysis

The project performs basic expense analysis.

For each category:

```text
Category Total
      ↓
Overall Total
      ↓
Percentage Calculation
      ↓
Report + Visualization
```

The percentage is calculated using:

```text
Percentage = (Category Total / Total Expense) × 100
```

---

# 📸 Screenshots

Screenshots of the application can be added to this section.

### Main Menu

Add a screenshot here:

```text
screenshots/main_menu.png
```

### Adding an Expense

```text
screenshots/add_expense.png
```

### Expense List

```text
screenshots/expense_list.png
```

### Expense Report

```text
screenshots/expense_report.png
```

### Expense Pie Chart

```text
screenshots/chart.png
```

---

# 🔮 Future Enhancements

The project can be extended with additional features in the future.

Possible improvements include:

- 📅 Monthly and yearly expense tracking
- 💵 Income tracking
- 📊 Bar charts and line graphs
- 📈 Monthly spending trends
- 🔔 Budget limit notifications
- 💳 Multiple payment methods
- 🔐 User login and authentication
- 🖥️ Graphical User Interface using Tkinter
- 🌐 Web version using Flask or Django
- 📱 Mobile application
- 📤 Export reports to CSV or PDF
- ☁️ Cloud database integration
- 🤖 AI-based spending analysis
- 💡 Personalized budgeting suggestions

---

# 🎓 Learning Outcomes

After completing this project, the developer gains practical experience with:

- Python programming
- Functions and modular programming
- Conditional statements and loops
- Exception handling
- File and database management
- SQLite databases
- SQL queries
- CRUD operations
- Data filtering and searching
- Data analysis
- Matplotlib visualization
- Command-line application development
- Git and GitHub
- Project documentation

---

# 💻 CRUD Operations

The project demonstrates the basic **CRUD** concept:

| CRUD Operation | Project Feature                      |
| -------------- | ------------------------------------ |
| **Create**     | Add an expense                       |
| **Read**       | View/search expenses                 |
| **Update**     | Can be added as future functionality |
| **Delete**     | Delete/reset expenses                |

---

# 📌 Limitations

The current version is intentionally designed as a lightweight CLI application.

Some limitations include:

- No graphical user interface
- No online/cloud synchronization
- No user authentication
- Data is stored locally
- No automatic budget recommendations
- No multi-user support

These limitations can be addressed through future enhancements.

---

# 🌟 Why This Project?

The Personal Expense Tracker was selected as a practical CSE project because it combines multiple programming concepts into one real-world application.

Instead of demonstrating Python concepts through isolated programs, this project combines:

```text
Python
   +
SQL
   +
SQLite
   +
Data Analysis
   +
Visualization
   +
GitHub
   =
Complete CSE Project
```

---

# 👩‍💻 Author

**Name:** Kathyaini Thota  
**Course:** B.Tech – ECE - AI & CYBERNETICS  
**Project:** Personal Expense Tracker

---

# 📜 License

This project is created for **educational and academic purposes**.

You may modify and extend the project for learning and personal use.

---

# ⭐ Acknowledgement

This project was developed as part of learning **Python programming, database management, SQL, data visualization, and software project development**.

---

## 🚀 Future Vision

The goal is to gradually transform this simple command-line application into a complete personal finance management system with:

```text
CLI Application
       ↓
Database Management
       ↓
Data Analysis
       ↓
Visualization
       ↓
GUI Application
       ↓
Web Application
       ↓
Complete Personal Finance Platform
```

**Personal Expense Tracker — Track. Analyze. Understand.**
