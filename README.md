🐧 Linux System Administration & Security Monitoring Project
📌 Overview

This project demonstrates practical Linux system administration and security fundamentals through a real-world, hands-on lab.

The project covers:

User & permission management

Log analysis

Backup & automation

Service & process monitoring

Network configuration & troubleshooting

Traffic analysis

Basic system hardening

It is designed to reflect real sysadmin tasks and offensive security mindset (CEH / OSCP preparation).

🧪 Environment

OS: Kali Linux (VMware)

User: analyst (non-root)

Shell: Bash

Focus: Linux Administration & Security

🗂️ Project Structure
project/
├── logs/
│   └── auth.log
├── scripts/
├── notes.txt
└── backups/

🔐 User & Permission Management

Created a non-root user to apply the Principle of Least Privilege

Restricted sensitive directories and files using permissions

adduser analyst
chmod 700 scripts/
chmod 600 notes.txt

📊 Log Analysis & Text Processing

Simulated authentication logs were analyzed using Linux CLI tools.

grep failed auth.log
sort auth.log | uniq -c


Use case:

Detect brute-force attempts

Identify abnormal behavior

💾 Backup & Archiving

Project data is archived using tar and gzip.

tar -czvf project_backup.tar.gz project/


A daily automated backup is scheduled using cron.

0 2 * * * tar -czf /home/analyst/project_backup_$(date +\%F).tar.gz /home/analyst/project

⚙️ Disk & Service Monitoring

Disk usage and services are continuously monitored.

df -h
du -sh project/
systemctl status ssh


This ensures system availability and stability.

🌐 Network Configuration & Troubleshooting

Network status and connectivity checks:

ip addr
ip route
ping 8.8.8.8


Open ports and services:

netstat -tulnp

📡 Traffic Analysis

Packet-level traffic inspection using tcpdump:

tcpdump -i eth0 -c 10


Observed:

ARP requests & replies

DNS queries

ICMP traffic

📈 System Monitoring

Resource usage monitoring:

htop
free -h
uptime

🌍 Web Tools

Basic web reconnaissance and testing:

curl -I http://localhost
wget http://example.com

🛡️ Security Hardening

Reduced attack surface by disabling root SSH login:

PermitRootLogin no

🎯 Skills Demonstrated

Linux system administration

Automation with cron

Log analysis

Network troubleshooting

Traffic inspection

Security hardening

OSCP-style thinking

🚀 Future Improvements

Linux privilege escalation labs

Advanced log monitoring

Bash scripting automation

SIEM integration

Attack & defense scenarios

📄 License

This project is for educational purposes.

👤 Author

Mohamed Yasser
Red Team Trainee | Network Security Student
Linux • Networking • Security Fundamentals

⭐ Notes

This project reflects hands-on practice and real-world scenarios rather than theoretical learning.
