# Simple Bank App

bank_accounts = {}

def create_account():
    name = input("Enter your name: ")
    account_number = input("Choose an account number: ")
    if account_number in bank_accounts:
        print("Account already exists!")
        return
    bank_accounts[account_number] = {"name": name, "balance": 0}
    print(f"Account created for {name} with account number {account_number}.")

def deposit():
    account_number = input("Enter account number: ")
    if account_number not in bank_accounts:
        print("Account not found.")
        return
    amount = float(input("Enter amount to deposit: "))
    bank_accounts[account_number]["balance"] += amount
    print(f"Deposited ₹{amount}. New Balance: ₹{bank_accounts[account_number]['balance']}")

def withdraw():
    account_number = input("Enter account number: ")
    if account_number not in bank_accounts:
        print("Account not found.")
        return
    amount = float(input("Enter amount to withdraw: "))
    if bank_accounts[account_number]["balance"] >= amount:
        bank_accounts[account_number]["balance"] -= amount
        print(f"Withdrawn ₹{amount}. Remaining Balance: ₹{bank_accounts[account_number]['balance']}")
    else:
        print("Insufficient balance.")

def view_balance():
    account_number = input("Enter account number: ")
    if account_number in bank_accounts:
        print(f"Account Holder: {bank_accounts[account_number]['name']}")
        print(f"Current Balance: ₹{bank_accounts[account_number]['balance']}")
    else:
        print("Account not found.")

def menu():
    while True:
        print("\n---- Bank Menu ----")
        print("1. Create Account")
        print("2. Deposit Money")
        print("3. Withdraw Money")
        print("4. View Balance")
        print("5. Exit")

        choice = input("Choose an option (1-5): ")

        if choice == '1':
            create_account()
        elif choice == '2':
            deposit()
        elif choice == '3':
            withdraw()
        elif choice == '4':
            view_balance()
        elif choice == '5':
            print("Thank you for using the bank app!")
            break
        else:
            print("Invalid option, try again.")

# Start the app
menu()
