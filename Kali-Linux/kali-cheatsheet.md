# 🐉 The Ultimate Kali Linux & SOC Command Vault

An exhaustive and professional cheat sheet covering essential to advanced Linux commands. Designed strictly for Penetration Testers, Ethical Hackers, and SOC Analysts for rapid enumeration, system administration, and exploitation.

---

## 🟢 1. System Navigation & Directory Operations
*The foundation of moving around the Linux file system seamlessly.*

```bash
pwd                     # Print Working Directory: Shows the absolute path of the current directory.
ls -lah                 # List All Human-Readable: Lists all files, hidden files, and exact sizes in KB/MB.
cd /var/www/html        # Change Directory: Moves to the default web server root directory.
cd ..                   # Move up one directory level.
cd -                    # Jump back to the previous working directory.
tree                    # Tree: Displays directories and files in a hierarchical tree format.
history                 # History: Shows the command history (useful to check what other users/attackers ran).
clear                   # Clear: Clears the terminal screen.

## ⌨️ 2. Essential Terminal Keyboard Shortcuts
*Speed is everything during a pentest or incident response. Master these to navigate the terminal like a pro.*

```text
Ctrl + L        # Clear: Clears the terminal screen (Same as typing 'clear').
Ctrl + C        # Interrupt/Kill: Stops the currently running foreground process instantly.
Ctrl + Z        # Background: Suspends the current process and sends it to the background (bring back with 'fg').
Ctrl + D        # EOF/Exit: Closes the current terminal session or logs out of an SSH connection.
Ctrl + R        # Reverse Search: Opens a search prompt to find previously typed commands in your history.
Ctrl + A        # Home: Moves the cursor to the very beginning of the current command line.
Ctrl + E        # End: Moves the cursor to the very end of the current command line.
Ctrl + U        # Clear Line: Deletes everything from the cursor to the beginning of the line.
Tab             # Autocomplete: Automatically completes file names, directory paths, or commands.
