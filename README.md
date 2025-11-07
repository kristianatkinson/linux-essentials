This project demonstrates my ability to analyze system logs, troubleshoot errors, review boot messages, check disk, and network configurations, and work with journalctl, grep, networking tools, and system utilities on UBUNTU.
All screenshots were taken during my hands-on lab session.


journalctl -p 4

Shows warnings and errors in yellow/red.

<img width="1280" height="800" alt="RemotePC2025-11-05 001129" src="https://github.com/user-attachments/assets/38ab887e-f21b-424f-8fec-a026644cc9e1" />

journalctl -n 50 > SysLogReport.txt

Shows the last 50 logs entered from the system journal AND puts them in a sys log report file.

<img width="1280" height="800" alt="RemotePC2025-11-05 004407" src="https://github.com/user-attachments/assets/1bfb9079-3aff-463a-8087-484e04de12af" />

journalctl -b

Shows logs, CPU info, RAM, booting steps from the most recent boot.

<img width="1280" height="800" alt="RemotePC2025-11-05 004724" src="https://github.com/user-attachments/assets/94c57456-f7cc-44b1-9104-c033745ace0a" />

journalctl -u NetworkManager

Shows us networking logs/events, configs.

<img width="1280" height="800" alt="RemotePC2025-11-05 005056" src="https://github.com/user-attachments/assets/1bbf63c5-0206-4ec1-ad65-e837a53ee5be" />

ping 8.8.8.8

Shows network connectivity (I got 0% packet loss).

<img width="1280" height="800" alt="RemotePC2025-11-05 010721" src="https://github.com/user-attachments/assets/dcae0290-5a12-4d9f-9abf-653e1e800988" />

ip addr

Shows network interface and IP configs.

<img width="1280" height="800" alt="RemotePC2025-11-05 011104" src="https://github.com/user-attachments/assets/5cf7c371-b541-44f5-9568-accffa42f347" />

df -h

Shows disk usage and verifies mounted locations.

(Essentially, I was asked to check my disk space and empty it, which makes sense because it was at 100%).

<img width="1280" height="800" alt="RemotePC2025-11-05 012059" src="https://github.com/user-attachments/assets/e6bafb38-cc71-41a9-a1f6-be598d425185" />

sudo journalctl --vacuum-time=100d

Shows that I vacuumed/emptied 100 days worth of logs on my disk.

<img width="1280" height="800" alt="RemotePC2025-11-05 012735" src="https://github.com/user-attachments/assets/f15b01f3-68f8-4c01-9a0e-80963077f410" />

journalctl -k | grep -i permission

I made a mistake writing out the command initially.  

Shows only kernel messages related to permission issues.

<img width="1280" height="800" alt="RemotePC2025-11-05 013446" src="https://github.com/user-attachments/assets/b9e5391e-47c2-473a-97e6-c24d5fbff221" />

cat log_analysis_report | grep -c -i "errors"

Shows counts of errors in the saved report.

cat log_analysis_report | grep -c -i "warnings"

Shows counts of warnings in the saved report.

<img width="1280" height="800" alt="RemotePC2025-11-05 015303" src="https://github.com/user-attachments/assets/81635989-309c-4ef9-92fd-46a92dcf7bde" />


