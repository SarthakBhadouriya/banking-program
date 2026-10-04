# 🏦 Python Banking Program

A simple, menu-driven command-line banking app written in pure Python. Check your balance, deposit money, and withdraw funds, all from the terminal with no dependencies.

![Python](https://img.shields.io/badge/python-3.6%2B-blue?logo=python&logoColor=white)
![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)
![Status](https://img.shields.io/badge/status-beginner%20project-yellow)

---

## 📖 Overview

This project is a beginner-friendly console application that simulates basic banking operations. It runs in a loop, showing a menu until the user chooses to exit. The entire program lives in a single file, `main.py`, which makes it easy to read, run, and learn from.

## ✨ Features

- **Show balance**: view your current balance, formatted to two decimal places
- **Deposit**: add money to your account, with rejection of negative amounts
- **Withdraw**: take money out, with checks for insufficient funds and negative amounts
- **Interactive menu**: simple numbered options that loop until you exit
- **Zero dependencies**: uses only the Python standard library

## 🖥️ Demo

```text
*******************************
Banking Program
*******************************
1. Show Balance
2. Deposit
3. Withdraw
4. Exit
*******************************
Enter you choice (1-4): 2
*******************************
Enter an amount to be deposited: 250
*******************************
```

```text
Enter you choice (1-4): 1
*******************************
Your balance is $250.00
*******************************
```

## 🚀 Getting Started

### Prerequisites

- [Python 3.6 or newer](https://www.python.org/downloads/) (the code uses f-strings)

Check your version with:

```bash
python --version
```

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/SarthakBhadouriya/banking-program.git
   ```

2. Move into the project folder:

   ```bash
   cd banking-program
   ```

### Running the program

```bash
python main.py
```

On some systems you may need to use `python3` instead of `python`.

## 🎮 Usage

When the program starts, you'll see a menu. Type the number of the action you want and press **Enter**.

| Option | Action       | Description                                              |
| :----: | ------------ | -------------------------------------------------------- |
|   `1`  | Show Balance | Prints your current balance                              |
|   `2`  | Deposit      | Prompts for an amount and adds it to your balance        |
|   `3`  | Withdraw     | Prompts for an amount and subtracts it from your balance |
|   `4`  | Exit         | Ends the program                                         |

Your starting balance is **$0.00**.

### Validation rules

| Action   | Condition                    | Result                                  |
| -------- | ---------------------------- | --------------------------------------- |
| Deposit  | Amount is negative           | Rejected, balance unchanged             |
| Withdraw | Amount is greater than balance | Rejected with an insufficient-funds message |
| Withdraw | Amount is negative           | Rejected, balance unchanged             |
| Menu     | Choice is not `1`–`4`        | "Not a valid choice" message, menu repeats |

## 🗂️ Project Structure

```text
banking-program/
└── main.py     # Entire application: menu loop plus deposit, withdraw, and balance functions
```

### How it works

| Function         | Purpose                                                                       |
| ---------------- | ----------------------------------------------------------------------------- |
| `show_balance()` | Prints the current balance formatted as currency                              |
| `deposit()`      | Reads an amount from the user and returns it if valid, otherwise returns `0`  |
| `withdraw()`     | Reads an amount, validates it against the balance, and returns the amount to subtract |
| `main()`         | Runs the menu loop and updates the balance based on the user's choice         |

## ⚠️ Known Limitations

This is a learning project, so keep these in mind:

- **No persistence**: the balance lives in memory only and resets to $0.00 every time the program restarts.
- **No input error handling**: entering non-numeric text (e.g. `abc`) when asked for an amount will raise a `ValueError` and crash the program.
- **Single account, no authentication**: there are no users, PINs, or multiple accounts.
- **Floating-point money**: amounts are stored as `float`, which can introduce rounding errors in real-world financial software.

## 🛣️ Ideas for Improvement

- [ ] Handle invalid (non-numeric) input with `try`/`except`
- [ ] Save and load the balance from a file or database
- [ ] Add a transaction history
- [ ] Support multiple accounts with PIN-based login
- [ ] Use `decimal.Decimal` for accurate currency handling
- [ ] Add unit tests with `pytest`

## 🤝 Contributing

Suggestions and improvements are welcome. To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## 📄 License

No license has been specified for this project yet. If you'd like others to be able to reuse it, consider adding one, such as [MIT](https://choosealicense.com/licenses/mit/).

## 👤 Author

**Sarthak Bhadouriya**
GitHub: [@SarthakBhadouriya](https://github.com/SarthakBhadouriya)
