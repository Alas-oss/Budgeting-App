# Budgeting-App
The Budgeting System is a Python program designed to help manage finances by categorizing expenses, tracking deposits and withdrawals, and visualizing spending distribution. The core functionality revolves around a Category class for financial management and a create_spend_chart function for generating spending visualizations.
## Features
### Category Class
The Category class represents a single budget category and provides methods to handle deposits, withdrawals, transfers, and balance checks. Each instance maintains a ledger to record financial transactions.

### Attributes:

- name: The name of the budget category.
- ledger: A list of transactions, each stored as a dictionary with amount and description.

### Methods:

- deposit(amount, description=""): Adds a deposit to the ledger with an optional description.
- withdraw(amount, description=""): Records a withdrawal if sufficient funds are available. Returns True if successful, otherwise False.
- get_balance(): Computes the current balance by summing all transaction amounts.
- transfer(amount, category): Moves funds from one category to another, creating appropriate entries in both ledgers. Returns True if successful.
- check_funds(amount): Verifies if sufficient funds exist for a given amount. Returns True or False.
- __str__(): Provides a string representation of the category, showing its name, transactions, and total balance in a visually appealing format.

### Spending Chart
The create_spend_chart(categories) function generates a vertical bar chart to visualize the percentage of spending across multiple categories.

### Steps:
1. Calculates the total spending and spending per category.
2. Converts spending into percentages, rounded down to the nearest 10%.
3. Constructs a text-based chart showing spending distribution and category labels.
