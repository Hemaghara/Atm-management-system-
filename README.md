# Atm-management-system-
# Java ATM Console Application

This Java program is a basic console-based application that simulates an ATM machine, allowing users to perform simple banking operations such as withdrawing money, depositing money, and checking their account balance. The program uses a loop to continuously display an ATM menu and processes user inputs to perform the desired operations.

## Overview of the Key Components

### 1. **Main Class:**
- The `Main` class is the entry point of the program.
- It creates an instance of the `ATM` class and sets an initial balance of 10,000 units.
- The program runs in a continuous loop, displaying the ATM menu and accepting user choices.

### 2. **ATM Menu:**
- The menu offers four options:
  1. **Withdraw money**
  2. **Deposit money**
  3. **Check balance**
  4. **Exit**
- Based on the user's choice, the corresponding method in the `ATM` class is called.

### 3. **Withdraw Money:**
- The `withdrawMoney` method prompts the user to enter their account number, the amount they wish to withdraw, and their PIN.
- If the amount is valid and there is sufficient balance, the amount is deducted from the total balance.
- The method then displays the remaining balance.

### 4. **Deposit Money:**
- The `depositMoney` method prompts the user to enter their account number, the amount they wish to deposit, and their PIN.
- The amount is added to the total balance, provided it is a valid amount.
- The method then displays the updated balance.

### 5. **Check Balance:**
- The `checkBalance` method simply displays the current balance of the user.

### 6. **Exit:**
- The `exit` method displays a goodbye message and the program terminates.

## Key Concepts Covered
- **Control Flow:** The program demonstrates the use of loops, conditionals, and switch-case statements.
- **User Interaction:** The program interacts with the user via the console, accepting input and providing feedback.
- **Basic Banking Operations:** The program simulates basic ATM operations like withdrawals, deposits, and balance inquiries.
- **Modular Code:** The functionality is separated into methods within the `ATM` class, making the code more modular and easier to maintain.

This program is a good starting point for beginners to understand how to structure a simple Java application and perform basic operations based on user input.
