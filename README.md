# Using-tools-like-John-the-Ripper-for-password-cracking
# Name: Kavi Keerthana R 
# Reg No: 212222100022
## AIM:
To crack password hashes using John the Ripper in Kali Linux.

## DESIGN STEPS:
### Step 1:
Install John the Ripper using the command:

### Step 2:
Prepare the password hash file (e.g., using unshadow for Linux password and shadow files).

### Step 3:
Use John the Ripper to crack the hashes:

## PROGRAM:

- **Install the John Ripper**
  ```bash
  sudo apt install john
  ```
- **Create a Password-Protected ZIP File**
   Archive a normal file (secret.txt) into a password-protected ZIP file
   ```bash
   zip --password 123abc tred.txt.zip tred.txt
   ```
 - **Extract the Hash from the ZIP File**
   ```bash
   zip2john /home/user/Desktop/tred.txt.zip > hash.txt
   ```
- **Crack the ZIP Password using John**
  ```bash
  john --format=zip /home/user/Desktop/hash.txt
  ```
- **Show the Cracked Password**
  ```bash
  john --show /home/user/Desktop/hash.txt
  ```

## OUTPUT:
### Create a Password-Protected ZIP File
![image](https://github.com/user-attachments/assets/8dcedd1c-a384-4def-9c41-94baafbe6687)


### Extract the Hash from the ZIP File
![image](https://github.com/user-attachments/assets/7a04dc39-feca-46fa-9387-ef03cca9f31e)


![image](https://github.com/user-attachments/assets/6e94118e-a671-4d56-84c9-550f0bbca886)


### Crack the ZIP Password using John
![image](https://github.com/user-attachments/assets/4cdb2e8a-6eb6-42a5-afdf-d17d5a867ca2)


### Show the Cracked Password
![image](https://github.com/user-attachments/assets/bf5719c7-471d-4a40-ab7d-1f603cb9333b)


## RESULT:
The password hashes were successfully cracked using John the Ripper.

