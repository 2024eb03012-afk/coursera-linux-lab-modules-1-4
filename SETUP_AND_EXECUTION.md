# Linux Lab Assignment - Coursera Modules 1-4

## Complete Execution Guide

This guide provides comprehensive instructions for executing all 40 Linux tasks across 4 questions.

### Prerequisites
- macOS or Linux system
- Git installed and configured
- Terminal access
- Your GitHub account ready

### Step 1: Clone the Repository

```bash
git clone https://github.com/2024eb03012-afk/coursera-linux-lab-modules-1-4.git
cd coursera-linux-lab-modules-1-4
```

### Step 2: Create Directory Structure

```bash
mkdir -p Question_1 Question_2 Question_3 Question_4
```

### Step 3: Execute All Commands and Capture Output

Follow the detailed instructions in each Question folder. For each task:
1. Execute the Linux command
2. Capture the output
3. Take a screenshot
4. Document the explanation

---

## QUESTION 1: System Administration Basics (10 Tasks - 5 Points)

Navigate to Question_1 folder and execute:

### Task 1: User Identity Verification
```bash
id
groups
```
**Output Format:** Shows current user UID, GID, and group memberships.
**File:** Save output to `task1_output.txt`

### Task 2: Workspace Validation
```bash
pwd
ls -la
```
**Output Format:** Shows current working directory and files with permissions.
**File:** Save output to `task2_output.txt`

### Task 3: Environment Confirmation File
```bash
echo "Linux user environment verified" > user_info.txt
```
**Explanation:** Creates a text file with verification message in the current directory.

### Task 4: File Integrity Check
```bash
wc -c user_info.txt
```
**Explanation:** Displays the byte count of the user_info.txt file created in Task 3.

### Task 5: Learning the Tools - Man Page
```bash
man mkdir
```
**Explanation:** Open man page for mkdir command, find and document one useful option (e.g., -p for parents).

### Task 6: Home Directory Inspection
```bash
ls ~ -1S
```
**Explanation:** Lists home directory contents in single column, sorted by file size (largest first).

### Task 7: Log Investigation
```bash
echo "admin login attempt" >> log.txt
grep "admin" log.txt
```
**Explanation:** Creates log file and searches for specific pattern to demonstrate grep functionality.

### Task 8: System Information Check
```bash
uname -r
```
**Explanation:** Displays the kernel release version of your operating system.

### Task 9: Network Connectivity Test
```bash
ping -c 4 www.google.com
```
**Explanation:** Sends 4 ICMP packets to verify network connectivity and measure response time.

### Task 10: System Health Awareness
```bash
uptime
```
**Explanation:** Shows system uptime (how long system has been running), number of users, and load average (CPU utilization).

---

## QUESTION 2: File & Directory Management (10 Tasks - 5 Points)

Navigate to Question_2 folder and execute:

### Task 1: Project Workspace Setup
```bash
mkdir documents
```

### Task 2: File Creation
```bash
cd documents && touch plan.txt
```

### Task 3: Content Addition
```bash
echo "Your project notes here" > plan.txt
```

### Task 4: File Metadata Verification
```bash
ls -l plan.txt
```
**Explanation:** Displays long format listing showing permissions, owner, size, and timestamp.

### Task 5: File Duplication
```bash
cp plan.txt plan_copy.txt
```

### Task 6: Directory Renaming
```bash
cd ..
mv documents project_documents
```

### Task 7: Archival Structure
```bash
mkdir project_documents/archive
```

### Task 8: File Organization
```bash
mv project_documents/plan_copy.txt project_documents/archive/
```

### Task 9: Recursive Listing
```bash
ls -R project_documents
```
**Explanation:** Displays directory tree showing all subdirectories and files recursively.

### Task 10: Path Verification
```bash
readlink -f project_documents/archive/plan_copy.txt
```
**Explanation:** Shows the full absolute path of the file, resolving any symbolic links.

---

## QUESTION 3: Links & Disk Usage (10 Tasks - 5 Points)

Navigate to Question_3 folder and execute:

### Task 1: File Creation
```bash
echo "Sample data content" > sample_data.txt
```

### Task 2: Hard Link Creation
```bash
ln sample_data.txt sample_hard.txt
```

### Task 3: Symbolic Link Creation
```bash
ln -s sample_data.txt sample_soft.txt
```

### Task 4: Inode Verification
```bash
ls -i sample_data.txt sample_hard.txt sample_soft.txt
```
**Explanation:** Shows inode numbers - hard link shares same inode, symbolic link has different inode.

### Task 5: Inode Analysis
**Explanation:** The hard link (sample_hard.txt) and original file (sample_data.txt) share the same inode number because they point to the same data block. The symbolic link has a different inode as it's a separate file containing just the path reference.

### Task 6: File Metadata Inspection
```bash
stat sample_data.txt
```
**Explanation:** Displays detailed file information including inode, permissions, size, access/modify times, and more.

### Task 7: Disk Usage Check
```bash
du -h ~
```
**Explanation:** Shows disk usage summary of home directory in human-readable format (KB, MB, GB).

### Task 8: File Size Overview
```bash
ls -lh ~
```
**Explanation:** Lists home directory files with sizes in human-readable format.

### Task 9: Link Deletion Test
```bash
rm sample_soft.txt
ls sample_data.txt
```
**Explanation:** Removing symbolic link doesn't affect the original file. Removing hard link decrements link count but preserves data if other links exist.

### Task 10: Disk Utility Demonstration
```bash
du -sh ~/*
df -h
```
**Explanation:** Shows disk usage summary for each item in home directory and filesystem disk space utilization in human format.

---

## QUESTION 4: System Monitoring (10 Tasks - 5 Points)

Navigate to Question_4 folder and execute:

### Task 1: System Uptime Verification
```bash
uptime
```

### Task 2: User Process Listing
```bash
ps aux --user=$USER
```
**Explanation:** Lists all processes running under current user account with detailed information.

### Task 3: CPU Usage Analysis
```bash
ps aux --user=$USER --sort=-%cpu | head -5
```
**Explanation:** Shows top 5 processes consuming most CPU resources, sorted by %CPU usage.

### Task 4: Background Process Execution
```bash
sleep 300 &
jobs
```
**Explanation:** Starts background process (300 second sleep) and lists active background jobs.

### Task 5: Process Priority Management
```bash
renice +5 -p <PID>
ps -p <PID> -o pid,ni,cmd
```
**Note:** Replace <PID> with actual process ID from background process. Positive nice value lowers priority.
**Explanation:** Changes process priority (nice value) and displays the modified process with new priority level.

### Task 6: Memory Usage Monitoring
```bash
free -h
```
**Explanation:** Displays memory usage statistics in human-readable format showing total, used, free, and cache memory.

### Task 7: Disk Space Inspection
```bash
df -h /home
```
**Explanation:** Shows disk space usage for /home filesystem including total, used, available space, and usage percentage.

### Task 8: Shell Identification
```bash
echo $SHELL
```
**Explanation:** Displays the current user's login shell (usually /bin/bash or /bin/zsh on macOS).

### Task 9: Output Redirection
```bash
uname -a > system_report.txt
cat system_report.txt
```
**Explanation:** Redirects system information output to file, then displays file contents to verify redirection worked.

### Task 10: Disk Usage Visualization
```bash
du -sh ~/* | sort -hr
```
**Explanation:** Shows disk usage for each directory in home, sorted by size in descending order.

---

## Step 4: Document Everything in GitHub

For each Question folder, create a `README.md` file with:
- All command outputs
- Screenshots
- 1-2 sentence explanations for each task
- Command syntax clarity

### README Template Structure

```
# Question X: [Title]

## Task 1: [Task Name]

**Command:**
\`\`\`bash
[command here]
\`\`\`

**Output:**
[paste actual output here]

**Explanation:** 
[Your 1-2 sentence explanation]

[Screenshot here or reference]
```

---

## Step 5: Push to GitHub

```bash
# From repository root directory
git add .
git commit -m "Add Question 1-4 lab assignment with outputs and explanations"
git push origin main
```

---

## Step 6: Submit to Coursera

1. Copy your repository URL: `https://github.com/2024eb03012-afk/coursera-linux-lab-modules-1-4`
2. Return to Coursera assignment page
3. Paste URL in the "URL" field
4. Enter Title: "Linux Lab Assignment Modules 1-4"
5. Enter Caption: "Complete documentation of all 4 questions with commands, outputs, and explanations"
6. Check the Honor Code checkbox
7. Click "Submit"

---

## Key Requirements Checklist

✓ Repository is PUBLIC
✓ Each task has command, output, and 1-2 sentence explanation
✓ Screenshots included for documentation
✓ All created files saved (user_info.txt, plan.txt, system_report.txt, etc.)
✓ README.md files for each Question folder
✓ Proper Git commits with descriptive messages
✓ Final submission to Coursera before January 2, 11:59 PM IST

## Total Points: 20 points (5 per Question)
## Due Date: January 2, 2025, 11:59 PM IST
## Attempts Available: 2
