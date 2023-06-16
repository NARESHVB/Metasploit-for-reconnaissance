# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## PROGRAM

Find out the ip address of the attackers system

## OUTPUT:

![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/43bec90a-b378-4565-ab01-6743aca3f2cb)


![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/4e43ade1-bd17-40a1-83bc-2205cf1ab30f)

## OUTPUT:

![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/2c460c3a-aa8a-44d1-b3dd-1c6ca510a27d)
ort Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000

## OUTPUT:
![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/39d885ee-0e7d-4ad8-8948-8c6e7cdc706b)

Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l

## OUTPUT:

![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/bf595857-53f0-4f66-af1c-3c2a4eca4b5f)

Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit


![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/589b55cb-8a46-4fa5-ac66-339858183cbb)

The info command provides information regarding a module or platform,

## OUTPUT:

![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/d0688c3b-5a94-4190-bc97-10a450445363)

Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init

## MYSQL ENUMERATION:

Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>

![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/52ac84d2-1454-4d82-b9d0-88769a5ff457)

Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql

![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/78692796-4bd0-4cb4-bdb9-9f15da85f6d6)

Use the set rhosts command to set the parameter and run the module, as follows:


![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/f1d9efaf-3d12-4db5-87d8-82bbb249bdf0)

After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.

\![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/983c2144-0dd8-495b-b4dc-a08a8813ad70)

set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true

![image](https://github.com/NARESHVB/Metasploit-for-reconnaissance/assets/119393642/4c9ec90b-341b-40ba-9261-8ac03c03b9f9)

## RESULT:
The Metasploit framework for reconnaissance is examined successfully
