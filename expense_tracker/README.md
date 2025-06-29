# 💰 Personal Expense Tracker

This is an intermediate Python project designed for students who have completed basic Python concepts and want to practice more advanced features. Building on file handling and JSON skills, this project introduces:

* Working with dates and time
* Data filtering and analysis
* Creating simple reports and statistics
* Input validation and error handling
* Using Python's `datetime` and `collections` modules

## 📦 Features

* ✅ Add expenses with category, amount, description, and date
* 📁 Store data in JSON format with automatic backup
* 📊 View expenses by category, date range, or month
* 💹 Generate spending reports and statistics
* 🔍 Search expenses by description or category
* 💾 Export data to CSV format
* 🎯 Set monthly budgets and track spending against them

## 🧠 Skills Practiced

* Advanced file handling with error management
* Working with `datetime` for date parsing and formatting
* Using `collections.defaultdict` for data grouping
* List comprehensions and filtering
* Exception handling with try/except blocks
* Creating reusable utility functions
* Data validation and user input sanitization
* Basic data analysis and reporting

## 🚀 How to Run

1. Make sure you have Python 3.10+ installed
2. Clone or download the repository
3. Open terminal and run:
```bash
python3 main.py
```

## 📁 Project Structure

```
EXPENSE_TRACKER/
├── main.py                    # Main application entry point
├── README.md                  # Project documentation
├── data/
│   ├── .gitkeep              # Keep data folder in git
│   ├── expenses.json         # Main expense data storage
│   ├── budgets.json          # Monthly budget settings
│   └── backups/              # Automatic backups folder
├── utils/
│   ├── .gitkeep              # Keep utils folder in git
│   ├── expense_manager.py    # Core expense CRUD operations
│   ├── report_generator.py   # Statistics and report functions
│   ├── data_validator.py     # Input validation utilities
│   └── file_handler.py       # File operations and backup management
└── exports/                  # CSV export destination
    └── .gitkeep
```

## 💡 Sample Categories to Try

| Category | Examples |
|----------|----------|
| Food | Groceries, Restaurants, Coffee |
| Transport | Fuel, Matatu, Uber |
| Entertainment | Movies, Games, Books |
| Bills | Electricity, Water, Internet |
| Health | Medicine, Doctor visits |
| Shopping | Clothes, Electronics |

## ✅ Sample Interaction

```
$ python3 main.py

💰 Welcome to Personal Expense Tracker
======================================

Choose an option:
1. Add new expense
2. View all expenses
3. View expenses by category
4. View monthly summary
5. Set monthly budget
6. Generate spending report
7. Search expenses
8. Export to CSV
9. Exit

> 1

📝 Add New Expense
------------------
Enter description: Lunch at Java House
Enter amount (KES): 850
Enter category: Food
Enter date (YYYY-MM-DD) or press Enter for today: 2024-12-15
✅ Expense added successfully!

> 4

📊 Monthly Summary - December 2024
==================================
Food: KES 2,450.00
Transport: KES 1,200.00
Entertainment: KES 800.00
Bills: KES 3,500.00
----------------------------------
Total Spent: KES 7,950.00
Budget: KES 10,000.00
Remaining: KES 2,050.00 ✅

> 6

📈 Spending Report - Last 30 Days
=================================
Total Expenses: 15
Total Amount: KES 12,340.00
Average per day: KES 411.33

Top Categories:
1. Food: KES 4,200.00 (34.0%)
2. Bills: KES 3,500.00 (28.4%)
3. Transport: KES 2,800.00 (22.7%)

Spending Trend: ↗️ Increasing
Budget Status: Within limit ✅
```

## 📄 Sample Data Files

### `expenses.json`
```json
[
  {
    "id": "exp_001",
    "description": "Lunch at Java House",
    "amount": 850.0,
    "category": "Food",
    "date": "2024-12-15",
    "timestamp": "2024-12-15T12:30:00"
  },
  {
    "id": "exp_002", 
    "description": "Uber to town",
    "amount": 320.0,
    "category": "Transport",
    "date": "2024-12-15",
    "timestamp": "2024-12-15T09:15:00"
  }
]
```

### `budgets.json`
```json
{
  "2024-12": {
    "total_budget": 10000.0,
    "category_budgets": {
      "Food": 3000.0,
      "Transport": 2000.0,
      "Entertainment": 1500.0,
      "Bills": 3500.0
    }
  }
}
```

## 🔧 Key Learning Concepts

### 1. Date Handling
```python
from datetime import datetime, date
import calendar

# Parse user input dates
def parse_date(date_str):
    try:
        return datetime.strptime(date_str, '%Y-%m-%d').date()
    except ValueError:
        return None

# Get month name
month_name = calendar.month_name[date.today().month]
```
📖 **Learn more**: [Python datetime documentation](https://docs.python.org/3/library/datetime.html)

### 2. Data Validation
```python
def validate_amount(amount_str):
    try:
        amount = float(amount_str)
        if amount <= 0:
            raise ValueError("Amount must be positive")
        return amount
    except ValueError:
        return None
```

### 3. Data Analysis
```python
from collections import defaultdict

def analyze_spending_by_category(expenses):
    category_totals = defaultdict(float)
    for expense in expenses:
        category_totals[expense['category']] += expense['amount']
    return dict(category_totals)
```
📖 **Learn more**: [Python collections documentation](https://docs.python.org/3/library/collections.html)

## 🎯 Challenge Extensions

Once the basic version is working, try adding:

1. **Recurring Expenses**: Monthly bills that auto-add
2. **Multiple Currencies**: Convert between KES, USD, EUR
3. **Visual Charts**: Use `matplotlib` for spending graphs
4. **Email Reports**: Send monthly summaries via email
5. **Web Interface**: Convert to Flask web app
6. **Database**: Replace JSON with SQLite database

##  New Python Concepts Introduced

* **datetime module**: Working with dates and time - [Official Documentation](https://docs.python.org/3/library/datetime.html)
* **collections.defaultdict**: Automatic dictionary initialization - [Official Documentation](https://docs.python.org/3/library/collections.html#collections.defaultdict)
* **Exception handling**: Proper error management
* **List comprehensions**: Concise data filtering
* **String formatting**: Modern f-string usage
* **File operations**: Reading, writing, and backup management
* **CSV module**: Data export functionality
* **UUID module**: Generating unique identifiers

##  Learning Objectives

By completing this project, your sister will:
- Understand date/time manipulation in Python
- Practice advanced data structures and algorithms
- Learn proper error handling techniques
- Gain experience with data analysis and reporting
- Develop skills in user input validation
- Build confidence with modular programming

This project bridges the gap between basic Python and more advanced applications, preparing her for real-world programming challenges!