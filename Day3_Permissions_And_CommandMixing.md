## 🔐 Day 3 – Linux Permissions & Command Mixing

---

### 🧠 What I Learned Today:
Today I explored **Linux file permissions** (`rwx`, `chmod`, `chown`) and how to **combine multiple commands** using operators like `;`, `&&`, and `|`.

---

### 🔐 File Permissions & Ownership Commands:

#### 📜 ls -l – View file permissions
```bash
ls -l
```
Displays permission details (`rwxr-xr--`), owner, group, and file info.

---

#### 🛡️ chmod – Change file permissions
```bash
chmod +x filename      # Add execute permission
chmod 755 filename     # Owner: rwx, Group: r-x, Others: r-x
```
Controls who can read/write/execute a file.

---

#### 👤 chown – Change file owner/group
```bash
sudo chown root:root filename
```
Changes ownership to the specified user and group (e.g., `root`).

---

### ⚙️ Command Mixing & Piping

#### ➕ ; – Run commands one after another
```bash
mkdir test; cd test
```
Executes both, even if the first fails.

---

#### ✅ && – Run second command **only if** the first succeeds
```bash
cd scripts && ls
```
If `cd` is successful, then `ls` runs.

---

#### 🔗 | (pipe) – Send output of one command into another
```bash
ls /etc | grep conf
```
Lists only the `/etc` files that contain "conf".

---

### 🧪 Challenge Summary:

- Created a folder and file using `mkdir`, `touch`, and `echo`
- Gave it execute permission with `chmod`
- Changed its ownership to `root` with `chown`
- Combined commands with `;` and `&&`
- Used `|` to filter command output like a pro

---

### 👀 Observations:
- Without `chmod +x`, scripts won’t run
- `|` is extremely powerful for fast filtering
- `chmod 755` is commonly used for safe executable access

---
