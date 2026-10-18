# Day 03 — TryHackMe Pre Security

**Path:** TryHackMe Pre Security  
**Day:** 03  
**Topics Completed:** Windows Basics, Linux CLI Basics, Windows CLI Basics, Operating System Security

---

## 1. Windows Basics

Today I learned the basic concepts of the Windows operating system, its file system, user accounts, and how users interact with the system.

### What Is Windows?

Windows is an operating system developed by Microsoft. It provides a graphical user interface (GUI) that allows users to interact with applications, files, folders, and hardware.

### Important Windows Concepts

**1. File System**

Windows organizes files and folders into a hierarchical structure.

Examples:

- `C:\` — commonly the main Windows drive.
- `C:\Users\` — contains user profile directories.
- `C:\Windows\` — contains important Windows system files.
- `C:\Program Files\` — commonly stores installed application files.

**2. User Accounts**

Windows supports different types of user accounts and permissions.

- **Administrator:** Can perform many system-level tasks.
- **Standard User:** Has more limited permissions for everyday activities.
- **Guest or restricted accounts:** May be available depending on the Windows configuration.

Using a standard account for everyday activities can help reduce the impact of certain attacks.

**3. Task Manager**

Task Manager helps users monitor running applications, processes, system performance, and startup applications.

It can be opened using `Ctrl + Shift + Esc`.

**4. Windows Security**

Windows includes security features such as Microsoft Defender Antivirus, Windows Firewall, account controls, and security updates.

### Why Windows Matters in Cybersecurity

Windows is widely used in homes and organizations. Understanding it helps me learn about:

- User accounts and permissions.
- Running processes and services.
- Windows security settings.
- Malware detection and prevention.
- Common Windows attack techniques.

### Important Terms

- Windows OS
- File System
- Administrator
- Standard User
- Task Manager
- Windows Defender
- Windows Firewall

---

## 2. Linux CLI Basics

Today I learned how to interact with a Linux operating system using the Command-Line Interface (CLI).

### What Is the Linux CLI?

The Linux CLI allows users to interact with the operating system by entering text commands into a terminal.

It is especially useful for system administration, automation, troubleshooting, and cybersecurity tasks.

### Important Linux Commands

**1. `pwd` — Print Working Directory**

Displays the current directory.

Example:

```bash
pwd
```

**2. `ls` — List Files**

Displays files and directories in the current location.

```bash
ls
ls -l
ls -la
```

- `ls -l` displays a detailed listing.
- `ls -la` also displays hidden entries.

**3. `cd` — Change Directory**

Moves from one directory to another.

```bash
cd Documents
cd ..
cd /
```

- `cd Documents` opens the Documents directory relative to the current location.
- `cd ..` moves to the parent directory.
- `cd /` moves to the root directory.

**4. `cat` — Display File Contents**

Displays the contents of a text file.

```bash
cat notes.txt
```

**5. `less` — Read Files Page by Page**

Useful for reading large text files.

```bash
less notes.txt
```

Press `q` to quit.

**6. `mkdir` — Create a Directory**

```bash
mkdir practice
```

Creates a directory named `practice`.

**7. `touch` — Create an Empty File**

```bash
touch notes.txt
```

Creates an empty file if it does not already exist.

**8. `cp` — Copy Files**

```bash
cp notes.txt backup.txt
```

Copies the file to a new name.

**9. `mv` — Move or Rename Files**

```bash
mv notes.txt old-notes.txt
```

Renames the file in this example.

**10. `rm` — Remove Files**

```bash
rm notes.txt
```

Removes the specified file. Use this command carefully because the deleted file may not be easily recoverable.

### Absolute and Relative Paths

- **Absolute path:** Specifies a location starting from the root directory, such as `/home/user/Documents`.
- **Relative path:** Specifies a location in relation to the current directory, such as `Documents/notes.txt`.

### Why Linux CLI Matters in Cybersecurity

Many cybersecurity tools run on Linux or are commonly operated through a terminal.

Learning CLI commands helps me:

- Navigate a system efficiently.
- Read configuration and log files.
- Manage files and directories.
- Investigate suspicious activity.
- Work with security tools and lab environments.

### Important Terms

- Terminal
- Shell
- CLI
- Directory
- Root Directory
- Absolute Path
- Relative Path
- Hidden Files

---

## 3. Windows CLI Basics

Today I learned that Windows can also be controlled through command-line tools instead of relying only on its graphical interface.

### What Is the Windows CLI?

The Windows CLI allows users to execute commands using tools such as Command Prompt (CMD) and PowerShell.

CMD and PowerShell are different command-line environments, each with its own capabilities and syntax.

### Important Windows Commands

**1. `dir` — List Files and Directories**

Displays the contents of the current directory.

```cmd
dir
```

**2. `cd` — Change Directory**

```cmd
cd Documents
cd ..
```

Moves into a directory or moves to its parent directory.

**3. `cls` — Clear the Screen**

```cmd
cls
```

Clears the Command Prompt screen.

**4. `type` — Display File Contents**

```cmd
type notes.txt
```

Displays the contents of a text file in CMD.

**5. `mkdir` — Create a Directory**

```cmd
mkdir practice
```

Creates a new directory.

**6. `copy` — Copy Files**

```cmd
copy notes.txt backup.txt
```

Copies a file to another file name or location.

**7. `move` — Move Files**

```cmd
move notes.txt Documents
```

Moves the specified file into the Documents directory, assuming that destination exists relative to the current location.

**8. `del` — Delete Files**

```cmd
del notes.txt
```

Deletes the specified file. Check the target carefully before running this command.

**9. `ipconfig` — View Network Configuration**

```cmd
ipconfig
```

Displays basic network configuration, including IP addresses for network adapters.

**10. `whoami` — Identify the Current User**

```cmd
whoami
```

Displays the current user's account identity.

### Linux CLI vs Windows CMD

| Task | Linux | Windows CMD |
|---|---|---|
| List files | `ls` | `dir` |
| Change directory | `cd` | `cd` |
| Show current directory | `pwd` | `cd` |
| Clear screen | `clear` | `cls` |
| Display file contents | `cat` | `type` |
| Create directory | `mkdir` | `mkdir` |
| Copy file | `cp` | `copy` |
| Move file | `mv` | `move` |
| Delete file | `rm` | `del` |

Note: PowerShell has additional commands and aliases. For example, `Get-ChildItem` lists directory contents, and `Get-Location` displays the current location.

### Why Windows CLI Matters in Cybersecurity

The Windows command line can help me:

- Inspect network configuration.
- Identify the current user.
- Navigate system directories.
- Manage files.
- Troubleshoot system issues.
- Perform basic system investigation.

### Important Terms

- Command Prompt (CMD)
- PowerShell
- Command
- Directory
- `ipconfig`
- `whoami`

---

## 4. Operating System Security

Today I learned the basic principles used to protect operating systems from unauthorized access and malicious activity.

### What Is Operating System Security?

Operating system security refers to the measures used to protect an operating system, its users, applications, files, and system resources against threats.

### Important Security Concepts

**1. Authentication**

Authentication verifies the identity of a user.

Example: Logging in using a username and password, with an additional authentication factor where enabled.

**2. Authorization**

Authorization determines what an authenticated user is allowed to access or do.

Example: A standard user may not be allowed to change certain system-wide settings.

**3. User Permissions**

Permissions control access to files, directories, applications, and other resources.

Incorrect permissions can expose sensitive data or allow unauthorized changes.

**4. Principle of Least Privilege**

Users and applications should receive only the permissions necessary to perform their tasks.

For example, an ordinary application should not automatically run with administrator privileges unless required.

**5. Software Updates and Patching**

Updates fix known vulnerabilities, improve stability, and may add security protections.

Keeping the operating system and applications updated helps reduce exposure to known security weaknesses.

**6. Firewalls**

A firewall controls network traffic according to configured rules.

It can help restrict unwanted network connections, although it cannot prevent every type of attack.

**7. Antivirus and Endpoint Protection**

Security software can help detect, block, and investigate malicious files or activities.

**8. Logging and Monitoring**

System logs record events such as logins, errors, and other system activities.

Reviewing relevant logs can help identify suspicious behavior.

### Common Operating System Security Risks

- Weak or reused passwords.
- Unnecessary administrator privileges.
- Outdated software.
- Misconfigured file permissions.
- Unnecessary services running on the system.
- Malware and malicious downloads.
- Unauthorized remote access.
- Poorly configured firewall rules.

### Basic Security Best Practices

- Use strong, unique passwords.
- Enable multi-factor authentication where available.
- Apply security updates regularly.
- Use standard accounts for routine work when practical.
- Enable and configure a firewall.
- Install software from trusted sources.
- Review account permissions.
- Back up important files.
- Investigate unexpected system activity.

### Why This Matters in Cybersecurity

Understanding operating system security helps me recognize how attackers may exploit weak configurations and how defenders reduce risk.

It also provides a foundation for learning vulnerability assessment, penetration testing, incident response, and system hardening.

### Important Terms

- Authentication
- Authorization
- User Permissions
- Least Privilege
- Vulnerability
- Security Patch
- Firewall
- Malware
- Logging
- System Hardening

---

## 5. What I Learned Today

Today I studied four important areas:

1. **Windows Basics:** How Windows organizes files, manages users, and provides system utilities.
2. **Linux CLI Basics:** How to navigate directories and manage files using Linux commands.
3. **Windows CLI Basics:** How to perform common tasks using CMD and understand the role of PowerShell.
4. **Operating System Security:** How authentication, permissions, updates, firewalls, and monitoring help protect a system.

These topics helped me understand how to interact with operating systems and why secure configuration is important in cybersecurity.

---

## 6. Things I Need to Revise

- [ ] Windows file system and user accounts
- [ ] Linux commands: `pwd`, `ls`, `cd`, `cat`, `mkdir`, `cp`, `mv`, `rm`
- [ ] Windows CMD commands: `dir`, `cd`, `type`, `copy`, `move`, `del`
- [ ] Difference between CMD and PowerShell
- [ ] Linux paths vs Windows paths
- [ ] Authentication vs Authorization
- [ ] Principle of Least Privilege
- [ ] Purpose of firewalls and security updates
- [ ] Why system logs are useful

---

## 7. Self-Assessment

Before moving to the next topic, I should be able to answer these questions:

1. What is the difference between a Windows GUI and CLI?
2. What does the Linux `pwd` command do?
3. What is the difference between `ls` and `cd`?
4. Which Windows CMD command displays network configuration?
5. What is the difference between CMD and PowerShell?
6. What is the difference between authentication and authorization?
7. What is the principle of least privilege?
8. Why should operating systems receive regular security updates?
9. How can incorrect file permissions create a security risk?
10. Why are system logs useful during a security investigation?

---

## TryHackMe Progress

**Pre Security Path**

- [x] Windows Basics
- [x] Linux CLI Basics
- [x] Windows CLI Basics
- [x] Operating System Security

**Day 03 Status: Completed ✅**
