

# 🐧 Further on Linux - Complete Class Notes

**Topics:** Linux File Hierarchy, VIM, NANO, Linux User Management

---

## 1. Linux File Hierarchy
Unlike Windows (which uses drive letters like `C:\`), Linux uses a single, unified directory structure starting from the **Root Directory (`/`)**. 

> **System Files:** In Windows, system files appear under `C:\Windows`. In Linux, they appear under `/`.

### The 13 Essential Directories

| Directory | Description | Examples / Notes |
| :--- | :--- | :--- |
| **`/` (Root)** | The base of the entire file system. Every file and directory starts here. Only the root user has write access here. | *Note: `/root` is the root user's home folder, which is different from `/`.* |
| **`/bin`** | Binary executables. Essential commands needed in single-user mode for all users. | `cat`, `ls`, `cp`, `pwd` |
| **`/boot`** | Boot loader files. Kernel and boot configuration files. | `vmlinuz`, `initrd.img`, `grub` |
| **`/dev`** | Essential device files. Represents hardware attached to the system. | `/dev/tty1`, `/dev/usbmon0` |
| **`/etc`** | Configuration files required by all programs. Contains startup/shutdown scripts. | `/etc/resolv.conf`, `/etc/passwd`, `/etc/shadow` |
| **`/home`** | Home directories for normal users to store personal files. | `/home/nathan` (Denoted by `~`). *You cannot access other users' home folders without permissions.* |
| **`/lib`** | Libraries essential for the binaries in `/bin` and `/sbin`. | `ld-2.11.1.so`, `libncurses.so.5.7` |
| **`/media`** | Mount points for removable media. | `/media/cdrom`, `/media/usb` |
| **`/mnt`** | Temporary mount directory where sysadmins can mount filesystems. | |
| **`/opt`** | Optional application software packages (add-on apps from vendors). | `/opt/microsoft` |
| **`/sbin`** | Essential system binaries used by the system administrator for maintenance. | `adduser`, `ifconfig` |
| **`/tmp`** | Temporary files created by the system and users. **Deleted upon reboot.** | |
| **`/usr`** | User Utilities. Contains binaries, libraries, docs, and source code. | `/usr/bin`, `/usr/sbin`, `/usr/lib` |

---

## 2. Text Editors

### VIM (Vi Improved)
A very powerful but cryptic text editor. It is hard to learn, especially for Windows users. 
*   **Syntax:** `vim filename`
*   **Default State:** VIM opens in **Normal/Command Mode**. 

#### VIM Modes
1.  **Insert Mode:** Press `i` to type and edit text.
2.  **Command/Normal Mode:** Press `Esc` to return here.
3.  **Visual Mode:** For selecting blocks of text.

#### Essential VIM Commands (from Command Mode)
| Command | Action |
| :--- | :--- |
| `:w` | Save (Write) |
| `:q` | Quit |
| `:wq` | Save and Quit |
| `:wq!` | Force Save and Quit |
| `:q!` | Force Quit (without saving) |
| `:undo` or `:u` | Undo last change |
| `%! yourcommand` | Execute a bash command and replace text (e.g., `%! grep fun`) |

#### VIM Visual Mode
*   **`v`**: Character-wise (selects text character by character).
*   **`Shift + v`**: Line-wise (selects entire lines).
*   **`Ctrl + v`** (or `Ctrl + q`): Block-wise (selects rectangular blocks).
*   **Common Actions:** `d` (Delete selected), `y` (Yank/Copy selected), `p` (Paste).

### NANO
A user-friendly, free, and open-source text editor pre-installed in most Linux systems.
*   **Syntax:** `nano filename`
*   Unlike VIM, you can just start typing immediately.

#### Nano Hotkeys
| Hotkey | Action |
| :--- | :--- |
| `Ctrl + S` | Save |
| `Alt + U` | Undo |
| `Alt + E` | Redo |
| `Ctrl + X` | Exit |
| `Ctrl + T` | Command Execute |
| `Alt + 6` | Copy |
| `Ctrl + K` | Cut |
| `Ctrl + U` | Paste |
| `Shift + Arrow` | Select text |
| `Ctrl + R` | Read/Insert file (appends text from another file) |

---

## 3. Linux User Management
On a computer system, the person who uses the computer is called a "user". Every user has a group and their own files/applications. 
*   To know your current username: `whoami`

### Types of Users
1.  **Root User (ID = 0):** Has the power to do everything on Linux.
2.  **Normal User (ID = 1-999):** Standard users with restricted permissions.
*   To run a command as root, normal users use `sudo` (Superuser do).

### Creating Users
*   `useradd` -> Simple creation.
*   `adduser` -> Detailed creation (recommended).
```bash
sudo adduser username
*   *Note:* When you create a user, a group with that same name is also created. 
*   User files are stored in `/etc/passwd`.
*   User passwords are stored in `/etc/shadow`.

### Accessing the Root User
To switch to the root user account:
```bash
sudo su
```
*(Once you are root, the terminal prompt changes from `$` to `#`).*

---

## 📝 Class Practice
Try these commands in your Linux terminal:

**Task 1:**
1. Create a text file called "takeme.txt" using **vim**.
   *   Text: `"This is The Inserted Text from Planet Mars!"`
   *   Save and Exit.
2. Create another text file called "Day3_MoreLinux.md" using **nano**.
   *   Text: `"This is day 3 course note."`
   *   Save and exit.
3. Open `Day3_MoreLinux.md` in **nano**, read the file `takeme.txt`, and add it to `Day3_MoreLinux.md` using `Ctrl + R`.

---

### 1. Create `takeme.txt` using VIM

Open your terminal and run:
```bash
vim takeme.txt
```

**Inside VIM:**
1. Press **`i`** to enter Insert Mode.
2. Type: `This is The Inserted Text from Planet Mars!`
3. Press **`Esc`** to return to Command Mode.
4. Type **`:wq`** and press **Enter** to Save and Exit.

---

### 2. Create `Day3_MoreLinux.md` using NANO

Run this command in your terminal:
```bash
nano Day3_MoreLinux.md
```

**Inside NANO:**
1. Type: `This is day 3 course note.`
2. Press **`Ctrl + O`** (the letter O, not zero) and press **Enter** to save.
3. Press **`Ctrl + X`** to exit nano.

---

### 3. Read `takeme.txt` into `Day3_MoreLinux.md` using NANO

Run this command to open the file you just created:
```bash
nano Day3_MoreLinux.md
```

**Inside NANO (While the file is open):**
1. Press **`Ctrl + R`** (Read File).
2. At the bottom, NANO will prompt: `File to insert [from ./]:`
3. Type: **`takeme.txt`** and press **Enter**.
4. This will insert the text from `takeme.txt` into your current file.
5. Press **`Ctrl + O`** and **Enter** to save the changes.
6. Press **`Ctrl + X`** to exit.

---

### 🛠️ How to verify it worked:
Run this command in your terminal to see the final result:
```bash
cat Day3_MoreLinux.md
```

**Expected Output:**
```text
This is day 3 course note.
This is The Inserted Text from Planet Mars!
```