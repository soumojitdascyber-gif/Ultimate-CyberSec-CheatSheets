# ⚙️ 01. Core Flags & Syntax Anatomy

**Basic Syntax:** `hydra [Options] <TARGET_IP or TARGET_DOMAIN> [Protocol]`

## The Flags That Matter
* `-l [username]` : (Lowercase L) Target a specific known user (e.g., `-l admin`).
* `-L [path/to/users.txt]` : (Uppercase L) Feed a dictionary of usernames (e.g., `-L /usr/share/wordlists/seclists/Usernames/top-usernames-shortlist.txt`).
* `-p [password]` : (Lowercase P) Test one specific password across multiple users (Password Spraying).
* `-P [path/to/passwords.txt]` : (Uppercase P) Feed a password dictionary (e.g., `-P /usr/share/wordlists/rockyou.txt`).
* `-C [path/to/combo.txt]` : (Uppercase C) Use for leaked `username:password` combo lists.
* `-t [tasks/threads]` : Defines the speed (Default 16). Use 4 for SSH/RDP to avoid connection resets.
* `-f` : **CRITICAL!** Exit on first valid find.
* `-vV` : Verbose mode. Shows exactly which `user:pass` is being tested.
* `-s [port_number]` : Specify a custom port (e.g., `-s 2222` for hidden SSH).
*
