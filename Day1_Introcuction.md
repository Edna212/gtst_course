
# 🛡️ GTST - Introduction to Ethical Hacking
**Instructor:** Nathan Hailu (GeezTech Security Tester®)
**Topics:** Course Overview, Git & GitHub, Introduction to Cyber Security, CIA Triad, Hacking Phases, Ethics.


## 1. Course Overview & Expectations
### Season 1 Curriculum
*   Introduction to Ethical Hacking (2)
*   Linux (9)
*   Python (8)
*   Bash (4)
*   Networking (2)

### Season 2 Curriculum
*   Footprinting and Recon (2)
*   Scanning Network (2)
*   Malware Threats (2)
*   Social Engineering (2)
*   Steganography & Cryptography (2)
*   Network Hacking (2)
*   System Penetration Testing (3)
*   Anonymity & Defensive Security (2)
*   Websites Security (3)
*   Wireless & Mobile Security (1)
*   Capture the Flag (CTF) (2)
*   Bug Bounty Hunting (1)
*   Report and Documentation (1)

### Grading & Rules
*   **Total Points:** 100pts (5 Assignments, 24+ Tasks, 1 Group Assignment, 2 Exams).
*   **Certificate:** Requires at least **60 pts** and passing the final exam.
*   **Attendance:** Must join before 2:30. Attendance is taken at the end of class. You need **70% attendance**, otherwise you lose 20pts.

### 7 Rules of the Class
1.  You DON'T #HACK because you know Hacking Theories. **Be practical.**
2.  You can't be a hacker in 1 night or with this class modules only. (It takes time).
3.  Stick to it. *Just do it.* (አይዱስ ዝሮችን ለመግር አተፍፋ).
4.  Try to simplify everything, don't make them hard.
5.  Enjoy the process (ሁልጊዜ ፈገግ ያልም!!!). The journey is bumpy.
6.  Things that seem useless have purpose (Detail later).
7.  Always Learn new things. *Everyday learning* is required.

> **Quote:** "Teachers can open the door, but you must enter it yourself."

---

## 2. Git & GitHub
*   **Git:** A version control system (tool) to manage changes on your files. Made by the Linux development community.
*   **GitHub:** A website/server where your Git files are hosted. Your files are stored in a folder called a **Repository**.

### Common Git Terms
| Term | Definition |
| :--- | :--- |
| **Push** | Uploading your data to the remote Git server (GitHub). |
| **Pull** | Downloading changes and integrating them into your local repository. |
| **Clone** | Downloading a new repository. |
| **Commit** | Saves your changes to the repository, creating a history (identified by a unique random string). |
| **Add** | Staging changes in your working directory to be included in the next commit. |

---

### 4 Methods to Publish Notes to GitHub

#### Method #1: The Git Command Line (Hardest)
*Requires Git Bash or Linux Terminal.*
```bash
# FOR FIRST TIME
cd Desktop
mkdir gtst && cd gtst
git init
git config --global user.name "Your Username"
git config --global user.email "Your Email"

# FOR NORMAL WORK
git status
git add .
git commit -m "Your Comment"
git log

# FOR GITHUB
git remote add origin <repositoryURL>
git push -u origin master
git clone <your project link>
```

#### Method #2: Visual Studio Code
1.  Open VS Code.
2.  Go to the Accounts icon (bottom left) -> **Turn on Settings Sync**.
3.  Sign in with GitHub.
4.  Authorize VS Code in the browser.
5.  Open your folder, make changes.
6.  Go to **Source Control** (branch icon on the left).
7.  Stage changes (+), type a commit message, and click **Commit**.
8.  Click **Sync Changes** to push to GitHub.

#### Method #3: The GitHub Website
1.  Login to GitHub.com.
2.  Create a new repository.
3.  Click **uploading an existing file**.
4.  Drag and drop your files, add a commit message, and click **Commit changes**.

#### Method #4: GitHub Desktop (Easiest)
1.  Open GitHub Desktop -> **Create a New Repository on your hard drive**.
2.  Give it a name, location, and initialize with a README.
3.  Open the repository folder in Obsidian or VS Code, and write your notes.
4.  Go back to GitHub Desktop. It will auto-detect changes.
5.  Type a Summary (commit message) and click **Commit to main**.
6.  Click **Publish repository** (top right) to push it to GitHub.

---

## 3. Introduction to Cyber Security
*   **Cybersecurity:** The practice of protecting systems, networks, and programs from digital attacks.
*   **Hacking:** Exploiting system vulnerabilities and compromising security controls to gain unauthorized access.
*   **Ethical Hacking:** Finding weak points/loopholes and reporting them to the organization.
*   **Vulnerability:** The state of being exposed to the possibility of being attacked or harmed.

### Types of Hackers (Based on Ethics)
1.  **Black Hat:** The "bad guys" (evil and malicious).
2.  **White Hat:** The "good guys" (ethical hackers).
3.  **Grey Hat:** Individuals who sometimes act ethically and other times engage in illegal activities.

### Types of Hackers (Based on Skill)
1.  **Newbie / Noob:** No knowledge about hacking.
2.  **Script Kiddie:** Unskilled individual who uses scripts/programs developed by others for malicious purposes.
3.  **Hacker:** Perfectly skilled, but with less experience.
4.  **Elite / Pro Hacker:** Perfectly skilled, with much more experience.

### Why do we learn Cyber Security?
1.  To prevent hackers from gaining access.
2.  To uncover vulnerabilities.
3.  To strengthen the organization.
4.  To safeguard the data.
5.  To avoid security breaches.
6.  To enhance security awareness.
7.  The industry needs Cyber Security Experts.

### Why do hacks happen?
> **ATTACKS = MOTIVE (GOAL) + METHOD + VULNERABILITY**
*   **Motive:** Information theft, manipulating data, financial loss, revenge, ransom, damaging reputation.

---

## 4. CIA Triad (Elements of Information Security)
The CIA triad is the basis for the development of security systems.

| Element | Definition | Example |
| :--- | :--- | :--- |
| **Confidentiality** | Keeping data secret/private. Only authorized users can access it. (ሚስጥራዊነት) | Encrypting patient data in a hospital. |
| **Integrity** | Making sure data is trustworthy and free from tampering/change. (ታማኝነት) | Ensuring bank balance records are accurate and not altered. |
| **Availability** | Ensuring information resources (hardware, software, networks) are accessible when needed. (ተገኝነት) | System is up and running so users can access it. |

### CIA Triad Exercises (Answers)
1.  *Only doctors can view medical records:* **Confidentiality**
2.  *Bank system crashes, clients can't access accounts:* **Availability**
3.  *Hackers modified financial data:* **Integrity**
4.  *Company uses encryption so stolen data can't be read:* **Confidentiality**
5.  *Bank ensures account balance shown is accurate:* **Integrity**
6.  *Emergency response system is down due to attack:* **Availability**
7.  *Healthcare organization encrypts patient data:* **Confidentiality**
8.  *No one can alter source code without authorization:* **Integrity**

---

## 5. Phases of Hacking
1.  **Reconnaissance:** Gathering information about the target (Passive/Active).
2.  **Scanning:** Identifying open ports, services, and vulnerabilities using tools.
3.  **Gaining Access:** Exploiting vulnerabilities to access the target system.
4.  **Maintaining Access:** Establishing backdoors or persistence for continuous access.
5.  **Covering Tracks:** Erasing logs and hiding signs of intrusion.

---

## 6. Penetration Testing
A method of evaluating the security of an information system or network by simulating an attack to find vulnerabilities, security measures, and prepare documentation.

### Types of Pentesting
1.  **Black Box Pentesting:** Testing system **without** prior knowledge. You test as an attacker.
2.  **White Box Pentesting:** Testing system **with** prior knowledge. You test as a developer.
3.  **Grey Box Pentesting:** Testing system with **limited** knowledge. You test as a user.

### Pentesting Exercises (Answers)
1.  *Hired to hack website without knowing internal structure:* **Black Box Pentest**
2.  *Given login credentials but no source code, testing as a regular user:* **Gray Box Pentest**
3.  *Given access to code, network architecture, and admin credentials:* **White Box Pentest**

### Field Terms
*   **Red Teaming (Offensive Security):** Simulating real-world attacks to test security.
*   **Blue Teaming (Defensive Security):** Defending against attacks, monitoring systems, and responding to threats.
*   **Security Audit:** Comprehensive evaluation of systems, controls, and procedures for compliance.
*   **Vulnerability Assessment:** Identifying and classifying security flaws via scans and manual testing.

---

## 7. Ethics of Cyber Security
> **#1 Respect the privacy of others.**
> **#2 Think before you type.**
> **#3 With great power comes great responsibility.**

*   Ethics is the most important concept in cyber security. A single bypass can put your life at risk. **Always have "PERMISSION!"**
*   **Ethiopian Law:** Ethiopia has a Cyber Crime Law called "ከጥጥፒተር ወንጀል አዋጅ" which has 6 parts detailing cyber attacks and their punishments.
*   As Ethical Hackers, our goal is to create a safe environment. We think like Black Hats to protect devices, but only for *educational purposes*.

---

## 8. Jobs in Cyber Security
*   Cyber Security Expert
*   Security / SOC Analyst
*   Cyber Security Consultant
*   Web Penetration Tester
*   Mobile Penetration Tester
*   Internal and External Penetration Tester
*   Network Security Tester
*   Bug Bounty Hunter

*Salary Example (US):* $92k - $150k per year depending on position.

---

## 📝 Exercise Time (GitHub Notes)
**Task:**
1. Create a Repository on your computer named `gtst_course`.
2. Create a Markdown file `Day1_Introduction.md` and a `README.md`.
3. Inside `Day1_Introduction.md`, write:
   ```markdown
   # DAY1: ETHICAL HACKING
   Hello **this** is test
   ```
4. Inside `README.md`, write:
   ```markdown
   This is note written while taking the Geez Tech Security Tester® course.
   ```
5. Push it to your GitHub.

**Answer (Using Git Command Line):**
```bash
mkdir gtst_course
cd gtst_course
git init

# Create the files
echo "# DAY1: ETHICAL HACKING
Hello **this** is test" > Day1_Introduction.md

echo "This is note written while taking the Geez Tech Security Tester® course." > README.md

# Commit and Push
git add .
git commit -m "Added Day 1 notes and README"
# (Go to GitHub, create the repo, and copy the URL)
git remote add origin <your_repo_url>
git push -u origin main
```

