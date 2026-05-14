# 🔐 RinLock 2.0

A simple command-line password manager built with Python, SQLite, and Fernet encryption.

---

# ⚙️ Features

- AES-style encryption using `Fernet`
- Store app credentials (app, username, password)
- Master password protection
- Change master password
- Delete saved accounts
- Duplicate prevention system
- Cross-platform storage support (Windows + Linux)

---

# 🚀 Installation

## 1. Install dependency

```bash
pip install cryptography
```

## 2. Run the program

```bash
python3 r2.py
```

---

# 📌 Commands

## 🔹 Add account

```bash
python3 r2.py add <app> <username> <password>
```

Example:

```bash
python3 r2.py add facebook john123 mypass123
```

---

## 🔹 Set master password (first time only)

```bash
python3 r2.py setpass <password>
```

Example:

```bash
python3 r2.py setpass rin123
```

---

## 🔹 Change master password

```bash
python3 r2.py changepass <old_password> <new_password>
```

Example:

```bash
python3 r2.py changepass rin123 newpass456
```

---

## 🔹 View saved passwords

```bash
python3 r2.py view <master_password>
```

Example:

```bash
python3 r2.py view rin123
```

---

## 🔹 Delete account

```bash
python3 r2.py delete <app>
```

Example:

```bash
python3 r2.py delete facebook
```

---

# 🔐 Security Notes

- Passwords are encrypted using Fernet
- Encryption key is stored in `secret.key`
- Master password is stored in SQLite database
- DO NOT delete `secret.key` or data cannot be recovered

---

# 📁 Storage (NEW UPDATE)

Database and encryption files are now stored in hidden system directories depending on the operating system.

## 🪟 Windows

```text
C:\Users\<User>\AppData\Roaming\RinLock
```

Files:

```text
rinlock.db   → database storage
secret.key   → encryption key
```

---

## 🐧 Linux

```text
~/.local/share/RinLock
```

Files:

```text
rinlock.db   → database storage
secret.key   → encryption key
```

---

# ⚠️ Warning

This project is for educational purposes only.

Do not use it as a production password manager.

---

# 🧠 Example Workflow

```bash
python3 r2.py setpass rin123

python3 r2.py add fb aldrix 123

python3 r2.py view rin123
```
