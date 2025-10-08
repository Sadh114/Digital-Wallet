# Digital-Wallet


https://github.com/user-attachments/assets/1eb25f7c-d433-47a4-8e15-d2726e7ced59





Overview:
This application simulates a simple ATM system using a client-server model.
The ATMServer manages accounts, PINs, and balances, while ATMClient provides
a console-based interface for users to interact with the server.

Features:
- Login and Logout with account number and PIN
- Check account balance (BAL)
- Deposit money (DEP <amount>)
- Withdraw money (WDR <amount>) with sufficient funds check
- Handles multiple clients concurrently using thread pool
- Proper EXIT option for safe disconnection

Server Details (ATMServer.java):
- Listens on a TCP port (default: 5555)
- Stores account balances in ConcurrentHashMap for thread-safety
- Uses ExecutorService to manage multiple client connections
- Commands supported: LOGIN, BAL, DEP, WDR, LOGOUT, EXIT

Client Details (ATMClient.java):
- Connects to server on localhost:5555
- Provides an interactive menu:
    1. Check Balance
    2. Deposit Money
    3. Withdraw Money
    4. Logout
    5. Exit
- Sends commands to server and prints server responses
- Validates inputs and handles login/logout gracefully


How to Run:
1. Compile:
   javac ATMServer.java ATMClient.java
2. Start Server:
   java ATMServer
3. Start Client:
   java ATMClient
4. Follow menu prompts on client side

Notes:
- Server handles invalid commands and incorrect amounts with error messages.
- Supports multiple clients simultaneously.

=========================================================


