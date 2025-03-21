# Budget Manager
**short description:**  
a simple and convenient budget management script that allows tracking the balance,
adding transactions (income and expenses), and automatically updating the balance.

## Features
- **Budget Management**: Track your financial balance.
- **Transaction Management**: Add income and expense transactions.
- **Dynamic Updates**: Automatically calculate the balance after each transaction.

## Usage
1. **Create a Budget Object**  
   Initialize the budget with a starting balance and, optionally, existing transactions.
2. **Add a Transaction**  
   Use the `add_transaction` function to add a new transaction and adjust the balance based on the transaction type (income/expense).

### Example:
```python      
# Initialize the budget with a starting balance and existing transactions
budget_data = Budget(balance=300, transactions=[
    {"type": "income", "amount": 1000, "description": "Salary"},
    {"type": "expense", "amount": 500, "description": "Rent"}
])
# Add a new transaction
budget_data.add_transaction("expense", 200, "Groceries")
# Display the balance and transactions
print(budget_data.balance)        # Expected output: 600
print(budget_data.transactions)
```
# enjoyy
