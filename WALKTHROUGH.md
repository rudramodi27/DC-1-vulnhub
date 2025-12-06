# Step 1
-     sudo netdiscover
  to find ip address

# Step 2 

-     nmap -A 192.168.1.1(ip Address)

-A meaning (Aggressive scan)
- Aggressive scan chalata hai jisme Nmap automatically ye sab detect karta hai:
- OS detection (system kaun sa chal raha hai)
- Service & version detection (ports pe kya software chal raha hai)
- Default NSE scripts (basic vulnerability checks)
- Traceroute (target tak ka network path)
