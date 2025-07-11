# 💱 Currency Converter App

## 📌 Description
This is a beginner-friendly Python project that converts currency values between four major currencies:  
- USD (US Dollar)  
- EUR (Euro)  
- INR (Indian Rupee)  
- GBP (British Pound)  

It uses static exchange rates (with INR as base) to perform simple calculations based on user input.

---

## ⚙️ Features
- Supports 4 major currencies
- Converts using predefined rates
- Shows result with emoji-enhanced formatting
- Validates inputs to ensure accuracy

---

## 💡 Sample Output
```
💱 Welcome to the Currency Converter App

Available Currencies:
1. USD (US Dollar)
2. EUR (Euro)
3. INR (Indian Rupee)
4. GBP (British Pound)

Enter the currency you want to convert from (USD/EUR/INR/GBP): INR  
Enter the currency you want to convert to (USD/EUR/INR/GBP): USD  
Enter the amount to convert: 2

✅ 2.0 INR = 0.02 USD
```

---

## 💻 Python Code

```python
print("💱 Welcome to the Currency Converter App")

# Display available currencies
print("\nAvailable Currencies:")
print("1. USD (US Dollar)")
print("2. EUR (Euro)")
print("3. INR (Indian Rupee)")
print("4. GBP (British Pound)")

# Currency rates with respect to INR
rates = {
    'USD': 83.2,
    'EUR': 90.1,
    'INR': 1,
    'GBP': 105.5
}

# Take user input
from_currency = input("\nEnter the currency you want to convert from (USD/EUR/INR/GBP): ").upper()
to_currency = input("Enter the currency you want to convert to (USD/EUR/INR/GBP): ").upper()
amount = float(input("Enter the amount to convert: "))

# Check if currencies are valid
if from_currency in rates and to_currency in rates:
    # Convert to INR first
    amount_in_inr = amount * rates[from_currency]
    # Then convert INR to target currency
    converted_amount = amount_in_inr / rates[to_currency]
    
    print(f"\n✅ {amount} {from_currency} = {round(converted_amount, 2)} {to_currency}")
else:
    print("\n⚠️ Invalid currency input. Please use only USD, EUR, INR, or GBP.")
```




## 📌 Note
Due to file upload error in GitHub mobile, this project has been created using manually written `.py` code and screenshot. Please copy the code from here and try running it on Google Colab, Jupyter, or any Python IDE.

---

#
