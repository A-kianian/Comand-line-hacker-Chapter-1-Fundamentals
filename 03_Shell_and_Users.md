# 03 – Shell, Users, and Navigating Linux (Core Basics)

## 🧠 Key Concepts

* **Shell**: Command interpreter interface (e.g., bash)
* **Terminal**: Text-based command interface (like a console window)
* **Root**: Superuser with full system privileges
* **User**: Regular account with limited permissions
* **Home directory**: Default file location for each user
* **Case sensitivity**: `File.txt` ≠ `file.txt` in Linux

----------------------------

## 🖥️ Starting the Terminal

* You can launch the terminal via:

  * Desktop icon
  * Shortcut: `CTRL + ALT + T`

----------------------------
## 🔍 Who Are You? – Using `whoami`

Use `whoami` to identify the current user:

whoami

Typical results:

* `root` → Admin-level account
* `kali` → Standard user

----------------------------

## 🔑 Root Privileges

* Some commands require admin rights.
* Prefix with `sudo`:

sudo apt update

* Or switch to root user entirely:

sudo su

* Return to normal user:

su kali

----------------------------

## 📁 Understanding the Filesystem

* Linux has a logical structure (not C:\ drive like Windows)
* Everything starts from `/` (root of filesystem)

### Common Directories

| Directory    | Description                |
| ------------ | -------------------------- |
| `/`          | Root of everything         |
| `/home/kali` | User directory             |
| `/root`      | Root’s home directory      |
| `/etc`       | Configuration files        |
| `/bin`       | Essential command binaries |
| `/media`     | Mounted external drives    |

----------------------------

## 📌 Where Am I? – `pwd`

Displays the current directory:

pwd

Example output:

/home/kali

----------------------------

## 📂 Moving Around – `cd`

Change directories:

cd /etc

Go back one level:

cd ..

Multiple levels:

cd ../../

To return to the root:

cd /

----------------------------

## 📋 Listing Contents – `ls`

Basic usage:

ls

Detailed listing:

ls -l

Show hidden files:

ls -a

Combined:

ls -la

### Sample Output (ls -l):

drwxr-xr-x  2 kali kali 4096 Jan 22 08:15 Documents
-rw-r--r--  1 kali kali  318 Jan 22 08:17 notes.txt

### Breakdown:

* `d` = directory, `-` = file, `l` = link
* `rwx` = permissions for owner, group, others
* Columns: type/permissions, links, owner, group, size, date, name

----------------------------

## 🔍 More Help

Use built-in help options:

ls --help
man ls

Exit `man` with `q`.

----------------------------

This section builds your comfort with shell basics and navigation. With these tools, you’ll move confidently in Linux and understand the file structure deeply. Ready to dive into file permissions and search tools next!
