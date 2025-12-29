# Linux Lab Assignment - Coursera Modules 1-4

## Project Overview

This repository contains a comprehensive graded lab assignment for Linux Command Line Interfaces and Scripting covering 4 modules with 40 total tasks (10 tasks per module, 5 points per module = 20 total points).

## Repository Structure

```
coursera-linux-lab-modules-1-4/
├── README.md                          # This file - overview and instructions
├── SETUP_AND_EXECUTION.md             # Comprehensive execution guide for all tasks
├── execute_all_labs.sh                # Automated shell script for task execution
├── Question_1/                        # System Administration Basics
│   ├── README.md                      # Task outputs and explanations
│   ├── task1_output.txt
│   ├── task2_output.txt
│   ├── user_info.txt
│   ├── log.txt
│   └── [other task outputs]
├── Question_2/                        # File & Directory Management
│   ├── README.md                      # Task outputs and explanations
│   ├── project_documents/
│   │   ├── plan.txt
│   │   └── archive/
│   │       └── plan_copy.txt
│   └── [task documentation]
├── Question_3/                        # Links & Disk Usage
│   ├── README.md                      # Task outputs and explanations
│   ├── sample_data.txt
│   ├── sample_hard.txt
│   ├── sample_soft.txt (symlink)
│   └── [task documentation]
└── Question_4/                        # System Monitoring
    ├── README.md                      # Task outputs and explanations
    ├── system_report.txt
    └── [task documentation]
```

## Quick Start Guide

### 1. Clone Repository
```bash
git clone https://github.com/2024eb03012-afk/coursera-linux-lab-modules-1-4.git
cd coursera-linux-lab-modules-1-4
```

### 2. Create Directory Structure
```bash
mkdir -p Question_1 Question_2 Question_3 Question_4
```

### 3. Execute Tasks
Choose one of the following approaches:

**Option A: Automated Execution (Recommended)**
```bash
chmod +x execute_all_labs.sh
./execute_all_labs.sh
```

**Option B: Manual Execution**
Follow the detailed instructions in `SETUP_AND_EXECUTION.md`

### 4. Document and Commit
```bash
git add .
git commit -m "Add Question 1-4 lab assignment with outputs and explanations"
git push origin main
```

## Assignment Details

### Question 1: System Administration Basics (5 points)
10 tasks covering:
- User identity and group verification
- Workspace validation
- Environment configuration
- File integrity
- Man page navigation
- Directory inspection
- Log investigation
- System information
- Network connectivity
- System health monitoring

### Question 2: File & Directory Management (5 points)
10 tasks covering:
- Directory creation and navigation
- File creation and content manipulation
- File metadata inspection
- File duplication and copying
- Directory renaming and movement
- Archival structures
- File organization
- Recursive listing
- Path verification

### Question 3: Links & Disk Usage (5 points)
10 tasks covering:
- Hard link creation and management
- Symbolic link creation and testing
- Inode analysis and verification
- File metadata inspection (stat command)
- Disk usage calculation and reporting
- File size overview
- Link deletion behavior
- Disk utility demonstrations

### Question 4: System Monitoring (5 points)
10 tasks covering:
- System uptime monitoring
- Process listing and analysis
- CPU usage tracking
- Background process management
- Process priority modification
- Memory usage monitoring
- Disk space inspection
- Shell identification
- Output redirection
- Disk usage visualization

## Key Requirements

✓ Repository is PUBLIC (required for grading)
✓ Each of 40 tasks includes:
  - Command syntax
  - Actual command output
  - 1-2 sentence explanation
  - Screenshot reference

✓ All created files are saved:
  - user_info.txt
  - plan.txt
  - system_report.txt
  - sample_data.txt and links
  - log files
  - Any other task-specific files

✓ README.md documentation for each Question folder

✓ Proper Git commits with descriptive messages

✓ Final submission URL to Coursera

## Submission Information

- **Assignment:** Linux Command Line Interfaces and Scripting - Graded Lab
- **Total Points:** 20 (5 per question)
- **Due Date:** January 2, 2025, 11:59 PM IST
- **Attempts Available:** 2
- **Submission Format:** GitHub Repository URL

## GitHub URL
`https://github.com/2024eb03012-afk/coursera-linux-lab-modules-1-4`

## Coursera Submission

1. Copy the GitHub repository URL above
2. Go to Coursera assignment page
3. Paste URL in the "URL" field
4. Title: "Linux Lab Assignment Modules 1-4"
5. Caption: "Complete documentation of all 4 questions with commands, outputs, and explanations"
6. Check Honor Code checkbox
7. Submit

## Files in This Repository

- **SETUP_AND_EXECUTION.md** - Detailed step-by-step execution guide
- **execute_all_labs.sh** - Automated script for all tasks
- **Question_1/README.md** - System Administration tasks documentation
- **Question_2/README.md** - File Management tasks documentation
- **Question_3/README.md** - Links & Disk Usage tasks documentation
- **Question_4/README.md** - System Monitoring tasks documentation

## Learning Outcomes

Upon completing this assignment, you will have:

1. **System Administration Skills:**
   - Understanding of user identity and permissions
   - Knowledge of system information commands
   - Network connectivity testing capabilities

2. **File & Directory Management:**
   - Ability to create and organize file hierarchies
   - File permission and metadata understanding
   - Directory traversal and management skills

3. **Advanced File Concepts:**
   - Deep understanding of inodes and links
   - Difference between hard and symbolic links
   - Disk usage analysis and optimization

4. **System Monitoring:**
   - Process monitoring and analysis
   - Performance metric understanding
   - Resource utilization tracking

5. **Linux Command Proficiency:**
   - 40+ Linux commands mastered
   - Command output interpretation
   - Shell scripting basics

## Additional Resources

- Linux man pages: `man [command_name]`
- Coursera course materials
- Linux documentation online

## Notes

- Ensure all commands are executed in the appropriate Question directories
- Take screenshots of terminal output for documentation
- Verify all files are created before committing
- Test symlinks and hard links thoroughly
- Document explanations in your own words

---

**Assignment Status:** Ready for Execution
**Repository Status:** PUBLIC ✓
**Last Updated:** December 29, 2025
