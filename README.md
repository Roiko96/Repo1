# Budget Manager

תיאור קצר:  
סקריפט ניהול תקציב פשוט ונוח, המאפשר מעקב אחרי יתרה, הוספת עסקאות (הכנסות והוצאות) ועדכון אוטומטי של היתרה.

## תכונות
- **ניהול תקציב**: מעקב אחרי יתרה עסקית.
- **ניהול עסקאות**: הוספת הכנסות והוצאות.
- **עדכון דינמי**: חישוב אוטומטי של היתרה לאחר כל עסקה.

## שימוש
1. **יצירת אובייקט Budget**  
   אתחלו את התקציב עם יתרה התחלתית ועסקאות קיימות, במידת הצורך.

2. **הוספת עסקה**  
   השתמשו בפונקציה `add_transaction` להוספת עסקה חדשה ולהתאמת היתרה בהתאם לסוג העסקה (income/expense).

### דוגמה לשימוש:
```python
# אתחול התקציב עם יתרה התחלתית ועסקאות קיימות
budget_data = Budget(balance=300, transactions=[
    {"type": "income", "amount": 1000, "description": "Salary"},
    {"type": "expense", "amount": 500, "description": "Rent"}
])

# הוספת עסקה חדשה
budget_data.add_transaction("expense", 200, "Groceries")

# הצגת היתרה והעסקאות
print(budget_data.balance)        # פלט צפוי: 600
print(budget_data.transactions)
