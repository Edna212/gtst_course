
# 🐉 Linux For User - Complete Class Notes
**Instructor:** Nathan Hailu (GeezTech Security Tester®)
**Topics:** Overview of Kali Linux, The Linux Shell, Linux Command Basics, Multiple Command Executions, Text Manipulation with Linux.

---

## 1. Overview of Kali Linux
> **Info:** Kali Linux was previously known as *Backtrack*. It is a Debian-derived Linux distribution designed for digital forensics and penetration testing.

*   **Desktop Environment:** The class uses GNOME, but KDE Plasma and Xfce are also available. Debian is recommended as the base.
*   **Login:** You can switch between Desktop environments (GNOME, GNOME Classic, Plasma, Xfce) at the login screen.

### Kali Linux Menu Categories
Kali organizes tools into specific categories:
1.  **Information Gathering:** `dmitry`, `ike-scan`, `legion`, `maltego`, `netdiscover`, `nmap`, `p0f`, `recon-ng`, `spiderfoot`
2.  **Vulnerability Analysis:** `legion`, `lynis`, `nikto`, `nmap`, `unix-privesc`
3.  **Web Application Analysis:** `burpsuite`, `commix`, `httrack`, `paros`, `skipfish`, `sqlmap`, `webscarab`, `wpscan`, `ZAP`
4.  **Database Assessment:** `jsql-injection`, `mdb-sql`, `oscanner`, `sidguesser`, `sqldict`, `SQLite data`, `sqlmap`, `sqlninja`, `sqlsus`, `tnscmd10g`
5.  **Password Attacks:** `cewl`, `crunch`, `hashcat`, `john`, `johnny`, `medusa`, `ncrack`, `ophcrack`, `rainbowcrack`, `rcracki_mt`, `wordlists`
6.  **Wireless Attacks:** `aircrack-ng`, `chirp`, `cowpatty`, `fern wifi cra...`, `kismet`, `mdk3`, `mfc`, `mfterm`, `pixiewps`, `reaver`, `wifite`
7.  **Reverse Engineering:** `apktool`, `bytecode-vi...`, `clang`, `clang++`, `dex2jar`, `edb-debug...`, `ghidra`, `jadx-gui`, `javasnoop`, `NASM shell`, `ollydbg`, `radare2`
8.  **Exploitation Tools:** `armitage`, `beef xss fra...`, `metasploit f...`, `msf payloa...`, `searchsploit`, `social engin...`, `sqlmap`, `termineter`
9.  **Sniffing & Spoofing:** `driftnet`, `ettercap-gr...`, `hamster`, `macchanger`, `mitmproxy`, `netsniff-ng`, `responder`, `wireshark`
10. **POST Exploitation:** `backdoor-f...`, `exe2hex`, `mimikatz`, `nishang`, `powersploit`, `proxychains4`, `weevely`
11. **Forensics:** `autopsy`, `binwalk`, `bulk_extrac...`, `chkrootkit`, `foremost`, `galleta`, `hashdeep`
12. **Reporting Tools:** `cutycapt`, `dradis fram...`, `faraday IDE...`, `maltego`, `pipal`, `recordmyd...`
13. **Social Engineering Tools:** `backdoor-f...`, `beef xss fra...`, `maltego`, `msf payloa...`, `social engin...`
14. **System Services:** Buttons to start/stop services (e.g., `beef start`, `dradis start`).

### Desktop Features
*   **Shutdown/Lock/Restart:** Available in the top-right system menu.
*   **Workspace Manager:** Used to classify work across different windows (Workspace 1, 2, etc.).
*   **Desktop Properties:** Right-click the desktop to change background, open terminal, or configure display settings.

### File Managers
*   **Dolphin** (KDE)
*   **Thunar** (Xfce)
*   **Nautilus** (GNOME)
*   *Note:* Windows file managers (like Shrestha Files) are not free.

---

## 2. The Linux Shell (Terminal)
The shell helps us communicate with the kernel and execute code. 

### Terminal Structure (5 Parts)
Example: `(rexder㉿HunterMachine)-[~]`

1.  **Username:** `rexder`
2.  **Hostname:** `HunterMachine`
3.  **Current Directory (PATH):** `~` (Home directory)
4.  **Privileged:** `$` (User) or `#` (Root)
5.  **Command Place:** Where you type.

*   **Home Directory:** `~`
*   **Local Directory:** `.`
*   **All Directories:** `*`
*   **Directory** = Folder

---

## 3. Linux Command Basics
Format: `command --option argument`
*   **Options:** Additional settings (e.g., `--add`)
*   **Arguments:** Different inputs (e.g., `1 1`)
*   **Command:** "Small programs that do one task well"

### File & Directory Management

| Command | Description | Example |
| :--- | :--- | :--- |
| `ls` | List directory contents | `ls Desktop Documents` |
| `tree` | List files/folders in a tree structure | `tree GTSTv1/` |
| `ls -Rla` | **R**ecursive, **L**ong list, **A**ll (hidden files start with `.`) | `ls -la` |
| `cd` | Change directory | `cd Downloads` |
| `cd ..` | Go back 1x | `cd ../` |
| `cd` | Go back to home dir | `cd` |
| `pwd` | Print working directory (full path) | `pwd` |
| `echo` | Display line of text/string | `echo "Hello"` |
| `touch` | Create empty file | `touch Day3.md` |
| `mkdir` | Make directory | `mkdir GeeZTech` |
| `mkdir -p` | Create nested directories | `mkdir -p folder1/folder2` |
| `clear` | Clear terminal screen | `clear` |
| `rm` | Remove file | `rm Day3.md` |
| `rm -r` | Recursive (folders) | `rm -r Folder` |
| `rm -i` | Prompt before delete | `rm -i file.txt` |
| `rm -f` | Force delete | `rm -rf 'Geez Tech'` |
| `cp` | Copy file/folder | `cp geez.txt Documents` |
| `cp -r` | Copy folder with files | `cp -r Desktop/ /root/` |
| `mv` | Move/Rename file/folder | `mv adb.1000.log ~/Downloads/` |

### Output Redirecting
*   `>` : Write output to file (Overwrites)
    ```bash
    echo text > file.txt
    ```
*   `>>` : Append output to file
    ```bash
    echo text >> file.txt
    ```

### Viewing Files
*   `cat [FILE]` : Show whole file content
*   `head [FILE]` : Show first 10 lines
*   `tail [FILE]` : Show last 10 lines
*   `less [FILE]` : View file page by page

---

## 4. Text Manipulation & Filtering

### `grep` (Global Regular Expression Print)
Searches a file for a particular pattern of characters and displays lines containing that pattern.

| Option | Description |
| :--- | :--- |
| `grep -i "search" file` | Case insensitive |
| `grep -c "search" file` | Count numbers of lines |
| `grep -l "search"` | Displays filename |
| `grep -r "search" folder` | Search text recursively in folders |
| `grep -v "term" file` | Display lines **without** this term |
| `grep -n "term" file` | Display the line number of the match |
| `grep -o "pattern" file` | Display that specific word only |

**Examples:**
```bash
# Find "hello" regardless of case in all files
grep -i "hello" *

# Find "HTB" recursively, show line numbers, and only the match
grep -rno HTB
```markdown


```bash
wc grep_test.txt
# Output: 1 13 59 grep_test.txt (1 line, 13 words, 59 bytes)
```

---

## 5. Multiple Command Executions
You can run multiple commands in one line using 3 methods:

### AND (`&&`)
Executes the second command **only if** the first command succeeds.
```bash
touch Day3.md && echo "Multi-lining"
```
*If `touch` fails, `echo` will NOT run.*

### OR (`||`)
Executes the second command **only if** the first command fails.
```bash
touch test || echo "not working"
```
*If `touch` fails, `echo "not working"` WILL run.*

### Piping (`|`)
Uses the output of the first command as the input for the next command.
```bash
cat grep_test.txt | grep "hello"
cat grep_test.txt | wc -l
```

---

## 6. Advanced Text Processing

### `sed` (Stream Editor)
A powerful command-line tool for parsing and transforming text in Linux. Processes files line-by-line.

*   **Syntax:** `sed [options] 'command' file`
*   **Substitute (Replace):** `sed 's/old/new/' file`
    *   Use `g` at the end to replace all occurrences in a line: `'s/old/new/g'`
*   **Delete lines matching a pattern:** `sed '/pattern/d' file`

**Examples:**
```bash
# Replace Nathan with Minte
cat temp.txt | sed 's/Nathan/Minte/'

# Replace all Hello with Hi
cat temp.txt | sed 's/Hello/Hi/g'

# Delete any line containing "Nathan"
cat temp.txt | sed '/Nathan/d'
```

### `awk`
A programming language used for pattern scanning and processing. By default, it determines columns separated by spaces (delimiter).

*   **Change Delimiter:** `-F "Sign"`
*   **Built-in Variables:**
    *   `$0`: Entire line of text
    *   `$1`, `$2`, ...: Represents each column (field)
    *   `NR`: Line (record) number
    *   `NF`: Number of fields in the current record

**Examples:**
```bash
# Print the first column
cat log1.txt | awk '{print $1}'

# Print the second column using a space delimiter
cat log1.txt | awk -F " " '{print $2}'

# Print the last column of a comma-separated file
cat log.txt | awk -F "," '{print $NF}'

# Print rows where column 3 is > 50
awk '$3 > 50 {print $1, $3}' file.txt
```

---

## 📝 Exercises & Tasks (With Answers)

### Task 1 (Basic Commands)
**Questions:**
1. Create 2 Folders called `gts` & `linux`.
2. Open `gts`, create a file called `linux.txt` with text "Hello this is my first text".
3. Create a python file with empty inside called `code.py`.
4. Create a markdown file with "# Test is Going." called `hacker.md`.
5. Move the python file you created to the `linux` folder.

**Answer Commands:**
```bash
# 1. Create folders
mkdir gts linux

# 2. Create file with text inside gts folder
cd gts
echo "Hello this is my first text" > linux.txt

# 3. Create empty python file
touch code.py

# 4. Create markdown file with text
echo "# Test is Going." > hacker.md

# 5. Move the python file to the linux folder
mv code.py ../linux/
```

### Task 2 (Piping & WC)
**Questions:**
1. Create a text file with name `paragraph.txt`:
   `"Hello my name is <Yourname>, i got this course of linux and said hello, and am trying to learn linux. I love linux, so i said HELLO world"`
2. How many times did the word "hello" get written?
3. How many bytes is the size of this text?
4. How many words are there?

**Answer Commands:**
```bash
# 1. Create the file
echo "Hello my name is Edna, i got this course of linux and said hello, and am trying to learn linux. I love linux, so i said HELLO world" > paragraph.txt

# 2. Count how many times "hello" appears (case-insensitive, count lines)
grep -i -c "hello" paragraph.txt

# 3. How many bytes?
wc -c paragraph.txt

# 4. How many words?
wc -w paragraph.txt
```

### Exercise #1 - `sed`
**Data:**
```text
1, John Doe, Sales, $3500
2, Jane Smith, IT, 4000
3, Sam Brown, Marketing, 3800
4, Lisa Ray, IT, 4200
5, Tom Scott, Sales, 3300
6, Anna White, Marketing, 4100
7, Bill Blue, Sales, 3600
8, Emma Gray, IT, 3900
```
**Questions:**
1. Replace all occurrences of "IT" with "Information Technology".
2. Delete lines that contain "Sales".

**Answer Commands:**
```bash
# (Assuming the data above is saved in a file called data.csv)

# 1. Replace IT with Information Technology (using g for global replacement)
sed 's/IT/Information Technology/g' data.csv

# 2. Delete lines containing "Sales"
sed '/Sales/d' data.csv
```

### Exercise #2 - `awk`
**Data:**
```text
Student, Subject, Grade
Alice, Math, 89
Bob, Science, 78
Charlie, Math, 95
Alice, Science, 92
Bob, Math, 85
Charlie, Science, 87
```
**Questions:**
1. **Total Grade:** Calculate the Total grade for each student.
2. **Student Names:** Display the student Name Only.
3. **Specific Subject:** Print all grades for Science.

**Answer Commands:**
```bash
# (Assuming the data is saved in a file called grades.csv)

# 1. Total Grade for each student (Using comma as delimiter)
awk -F "," 'NR>1 {sum[$1]+=$3} END {for (name in sum) print name, sum[name]}' grades.csv

# 2. Display Student Names Only
awk -F "," 'NR>1 {print $1}' grades.csv

# 3. Print all grades for Science
awk -F "," '$2 == "Science" {print $3}' grades.csv
```

---

## 📌 Assignments
1. Write notes on GitHub.
2. Do the exercises again; these are the most basic and essential ones.

#obsidian #linux #kali #cheatsheet
```