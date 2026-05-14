# 🔐 RinLock 2.0

A simple command-line password manager built with Python, SQLite, and Fernet encryption.

---

## ⚙️ Features
- AES-style encryption using `Fernet`
- Store app credentials (app, username, password)
- Master password protection
- Change master password
- Delete saved accounts
- Duplicate prevention system

---

## 🚀 Installation

### 1. Install dependency
```bash
pip install cryptography
2. Run the program
python3 rinlock2.0.py
📌 Commands
🔹 Add account
python3 rinlock2.0.py add <app> <username> <password>

Example:

python3 rinlock2.0.py add facebook john123 mypass123
🔹 Set master password (first time only)
python3 rinlock2.0.py setpass <password>

Example:

python3 rinlock2.0.py setpass rin123
🔹 Change master password
python3 rinlock2.0.py changepass <old_password> <new_password>

Example:

python3 rinlock2.0.py changepass rin123 newpass456
🔹 View saved passwords
python3 rinlock2.0.py view <master_password>

Example:

python3 rinlock2.0.py view rin123
🔹 Delete account
python3 rinlock2.0.py delete <app>

Example:

python3 rinlock2.0.py delete facebook
🔐 Security Notes

Passwords are encrypted using Fernet
Encryption key is stored in secret.key
Master password is stored in SQLite database
DO NOT delete secret.key or data cannot be recovered

📁 Storage (NEW UPDATE)
Database is now stored in AppData (hidden folder)
Key file is also stored securely in AppData

Windows path:

C:\Users\<User>\AppData\Roaming\RinLock\

Files:

rinlock.db → database storage
secret.key → encryption key
⚠️ Warning

This project is for educational purposes only.

Do not use it as a production password manager.

🧠 Example Workflow
python3 rinlock2.0.py setpass rin123
python3 rinlock2.0.py add fb adlrix 123
python3 rinlock2.0.py view rin123