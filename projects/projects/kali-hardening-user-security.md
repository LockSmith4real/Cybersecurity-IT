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
