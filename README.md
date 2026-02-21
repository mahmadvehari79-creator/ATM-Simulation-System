# ATM-Simulation-System (CLI-Based)

A Python-based ATM Simulation System that supports user authentication, Balance Checking, and withdrawals. It allows only three attempts for the user, which protects your account from unauthorised access. If any unauthorised person attempts to access your account without your permission, your account will be locked after 3 attempts.
The system uses a menu-driven approach implemented with loops and match-case, ensuring continuous interaction until the user chooses to exit. It also includes security features like limited login attempts and account blocking after three incorrect PIN entries. Additionally, the program handles validation for transactions and provides a low balance warning when funds drop below a defined threshold.
This project used programming fundamentals concepts
It serves as a foundational implementation of how ATM systems manage user authentication and transactions.

#Features
Secure Login with PIN Verification (3 Attempts).
User Friendly.
Account Blocking After Failed Attempts.
Low Balance Warning.
Uses match-case for menu handling.
Easy to Understand Code.
How It Works (Step-by-Step)

1. User Database
users = {
    "1001": {"pin": "1234", "balance": 5000, "name": "Ali"},
    ...
}

Stores account number as key

Each user has:

PIN

Balance

Name

👉 This acts like a mini database

2. Account Verification
3. 
acc_no = input("Enter Account Number: ")

Checks if the account exists

If not → "Account not found."

3. PIN Authentication
4. 
while attempts < 3:

User gets 3 chances

If correct → access granted

If wrong → attempts increase

If all fail → account blocked

4. ATM Menu (Core Logic)

Menu runs using an infinite loop:

while True:

Handled using:

match choice:

🔧 Functionalities
✅ Check Balance

Displays current balance:

print("Balance:", user["balance"])
💰 Deposit

Accepts amount

Must be greater than 0

Adds to balance

user["balance"] += amount
💸 Withdraw

Conditions:

Amount must be positive

Must not exceed balance

elif amount > user["balance"]:

After withdrawal:

Updates balance



Shows a warning if the balance < 1000

🚪 Exit

Breaks the loop and ends the program

🛠️ Concepts Used

Dictionary (data storage)

Loops (while)

Conditional statements (if-elif-else)

match-case (Python switch)

Input handling

State updates (balance changes)
