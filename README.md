<div align="center">
  
# 🐧 Linux Commands for Ethical Hacking
  
**Your Ultimate Guide to Mastering Linux for Cybersecurity & Penetration Testing**

[![GitHub stars](https://img.shields.io/github/stars/sobj41/Linux--?style=social)](https://github.com/sobj41/Linux--/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/sobj41/Linux--?style=social)](https://github.com/sobj41/Linux--/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Made with Love](https://img.shields.io/badge/Made%20with-❤️-red.svg)](https://github.com/sobj41)

</div>

---

## 📖 Table of Contents
- [Linux File System Overview](#-linux-file-system-overview)
- [Important Directories for Ethical Hacking](#-important-directories-for-ethical-hacking)
- [Essential Linux Commands](#-essential-linux-commands-for-hackers)
- [Practical Tips](#-practical-tips)
- [How to Contribute](#-how-to-contribute)
- [License](#-license)

---

## 📁 Linux File System Overview

> *"In Linux, everything is a file – including hardware, processes, and devices."*

Linux follows a **hierarchical file system** starting from the root directory (`/`). Understanding this is the **first step** to becoming an ethical hacker.

### Key Concepts

| Concept | Description | Example |
|---------|-------------|---------|
| **Root Directory (`/`)** | The top-most directory in the file system | `/` |
| **Absolute Path** | Full path starting from root | `/home/user/file.txt` |
| **Relative Path** | Path relative to current directory | `./file.txt` or `../file.txt` |
| **Hidden Files** | Files starting with a dot (`.`) | `.bashrc`, `.ssh/` |

---

## 📂 Important Directories for Ethical Hacking

These directories are **critical** for penetration testers and forensic analysts:

| Directory | Purpose | Why Hackers Love It |
|-----------|---------|---------------------|
| `/etc` | System configuration files | Contains `/etc/passwd`, `/etc/shadow` – prime targets for privilege escalation |
| `/var/log` | System & application logs | Essential for forensic analysis and tracking attacker footprints |
| `/tmp` | Temporary files | Often used for storing exploit payloads and temporary scripts |
| `/proc` | Virtual filesystem for processes | Real-time kernel & process info – `/proc/cpuinfo`, `/proc/meminfo` |
| `/root` | Root user's home directory | Highly restricted – contains sensitive files and keys |
| `/home` | Regular users' home directories | Contains user data, SSH keys, and configuration files |
| `/bin` & `/sbin` | System binaries | Essential commands like `ls`, `cat`, `ifconfig` |
| `/usr` | User-installed programs | Where most applications and tools are installed |
| `/var/www` | Web server files | Common target for web application attacks and reverse shells |
| `/dev` | Device files | Contains device interfaces – can be used for low-level access |

---

## 🔥 Essential Linux Commands for Hackers

### 📂 File & Directory Management

| Command | Description | Example |
|---------|-------------|---------|
| `ls` | List directory contents | `ls -la` (show all files with details) |
| `cd` | Change directory | `cd /etc` |
| `pwd` | Print working directory | `pwd` |
| `mkdir` | Create a new directory | `mkdir hacking-tools` |
| `rm` | Remove files/directories | `rm -rf temp-folder` |
| `cp` | Copy files/directories | `cp file1.txt /backup/` |
| `mv` | Move or rename files | `mv oldname.txt newname.txt` |
| `touch` | Create an empty file or update timestamp | `touch newfile.txt` |

---

### 🔍 Searching & Filtering

| Command | Description | Example |
|---------|-------------|---------|
| `cat` | Display file content | `cat /etc/passwd` |
| `less` / `more` | View files page by page | `less /var/log/syslog` |
| `head` / `tail` | View first/last lines of a file | `tail -f /var/log/auth.log` |
| `grep` | Search for patterns in files | `grep "Failed" /var/log/auth.log` |
| `find` | Search for files/directories | `find / -name "*.conf" 2>/dev/null` |
| `locate` | Quickly find files using database | `locate nmap` |
| `sort` | Sort lines of text | `sort file.txt` |
| `uniq` | Report or omit repeated lines | `sort file.txt \| uniq -c` |

---

### 🔐 Permission Management

| Command | Description | Example |
|---------|-------------|---------|
| `chmod` | Change file permissions | `chmod 755 script.sh` |
| `chown` | Change file ownership | `chown user:group file.txt` |
| `umask` | Set default file permissions | `umask 022` |
| `ls -l` | View file permissions | `ls -l /etc/passwd` |

---

### 🌐 Networking & Reconnaissance

| Command | Description | Example |
|---------|-------------|---------|
| `ifconfig` | Configure network interfaces | `ifconfig eth0` |
| `ip` | Show/manipulate routing & devices | `ip a` |
| `netstat` | Display network connections | `netstat -tuln` |
| `ss` | Socket statistics (modern netstat) | `ss -tuln` |
| `nmap` | Network scanning tool | `nmap -sV 192.168.1.1` |
| `tcpdump` | Capture network traffic | `tcpdump -i eth0 -w capture.pcap` |
| `whois` | Domain ownership lookup | `whois example.com` |
| `dig` | DNS query tool | `dig google.com` |
| `nslookup` | Query DNS servers | `nslookup google.com` |
| `ping` | Test network connectivity | `ping -c 4 google.com` |
| `curl` | Transfer data from/to server | `curl -I https://example.com` |
| `wget` | Download files from the internet | `wget https://example.com/file.zip` |

---

### 🛡️ Remote Access & File Transfer

| Command | Description | Example |
|---------|-------------|---------|
| `ssh` | Secure remote access | `ssh user@192.168.1.10` |
| `scp` | Securely copy files over SSH | `scp file.txt user@server:/path/` |
| `rsync` | Synchronize files remotely | `rsync -av /local/ user@server:/remote/` |
| `sftp` | Secure file transfer protocol | `sftp user@192.168.1.10` |

---

### 🧠 Process & System Monitoring

| Command | Description | Example |
|---------|-------------|---------|
| `ps` | Show running processes | `ps aux` |
| `top` / `htop` | Real-time process monitoring | `htop` |
| `kill` | Terminate processes | `kill -9 PID` |
| `systemctl` | Manage system services | `systemctl status ssh` |
| `df` | Show disk usage | `df -h` |
| `du` | Show directory/file size | `du -sh /var/log` |
| `free` | Show memory usage | `free -h` |
| `uptime` | Show system uptime | `uptime` |

---

### 🛠️ Miscellaneous Useful Commands

| Command | Description | Example |
|---------|-------------|---------|
| `history` | Show command history | `history` |
| `alias` | Create command shortcuts | `alias ll='ls -la'` |
| `echo` | Print text to terminal | `echo "Hello World"` |
| `date` | Display current date/time | `date` |
| `whoami` | Show current username | `whoami` |
| `id` | Show user ID and group info | `id` |
| `uname` | Show system information | `uname -a` |

---

## 🛠️ Practical Tips for Ethical Hackers

### 💡 Pro Tips

1. **Explore Every Command**
   ```bash
   nmap --help
   man nmap
