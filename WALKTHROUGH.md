# Step 1
-     sudo netdiscover
  to find ip address

# Step 2 

-     nmap -A 192.168.1.7(ip Address)

-A meaning (Aggressive scan)
- Aggressive scan chalata hai jisme Nmap automatically ye sab detect karta hai:
- OS detection (system kaun sa chal raha hai)
- Service & version detection (ports pe kya software chal raha hai)
- Default NSE scripts (basic vulnerability checks)
- Traceroute (target tak ka network path)

---The NMAP scan indicates that three ports are open: 22 (SSH), 80 (HTTP), and 111 (RPC).
---Discovering that port 80 is running HTTP, we proceed to open the IP address in our web browser.
![1_2Kwm-x_URC1htqpofvbB3g](https://github.com/user-attachments/assets/4abe3213-2297-474e-9f36-7472a6043ed4)
-Gaining access through Metasploit
