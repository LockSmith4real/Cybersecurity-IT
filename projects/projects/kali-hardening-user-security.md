# Kali Linux Hardening & Secure User Setup

## Summary
Created a new secure user account on Kali Linux, removed the default user, added proper privileges, and applied basic hardening steps to improve system security with some trouble-shooting needed. This prevents predictable usernames, reduces privilege abuse risks, and follows penetration tester best practices.

---

## Steps Taken

### 🔐 1. Created a New Secure User
```bash
sudo adduser lock

sudo usermod -aG sudo lock
sudo apt update


First confirmed no active processes:
ps -u kali
sudo pkill -u kali

Then removed the user and their home directory:
sudo deluser --remove-home kali

Updated Hostname for Anonymity

### 🔐 8. Enforced Strong Password Policy with PAM

Updated `/etc/pam.d/common-password` to use `pam_pwquality`:

- Minimum length: 12 characters
- At least 1 uppercase, 1 lowercase, 1 digit, and 1 special character
- Used `pam-auth-update` to regenerate a valid PAM config
- Tested with the `passwd` command to confirm weak passwords are rejected
