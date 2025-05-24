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
![image](./images/a1.png)

### Extract the Hash from the ZIP File
![image](./images/a2.png)

![image](./images/a3.png)

### Crack the ZIP Password using John
![image](./images/a4.png)

### Show the Cracked Password
![image](./images/a5.png)

## RESULT:
The password hashes were successfully cracked using John the Ripper.

