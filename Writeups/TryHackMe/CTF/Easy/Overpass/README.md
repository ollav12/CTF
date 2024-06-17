# Overpass

- Mode: CTF
- Difficulty: Easy
- URL: <a href="https://tryhackme.com/r/room/overpass" target="_blank">link</a>

## Skills Learned

- 
- 
- 

## Tools Used

- 
- 
- 


## CTF Information

What happens when a group of broke Computer Science students try to make a password manager?
Obviously a perfect commercial success!


## Writeup:

**Question 1: Hack the machine and get the flag in user.txt**

1. NMap

NMap run

![alt text](image-8.png)

2. Recon on website

Front page

![alt text](image-1.png)

Downloads page

![alt text](image-2.png)

About Us page

![alt text](image-3.png)

3. Testing binaries for overpass

Running binary files for linux overpass

![alt text](image.png)

4. Running "nikto" and testing injection in login

Running nikto

![alt text](image-7.png)

5. Reading login.js

Front page login

![alt text](image-5.png)

Code login

![alt text](image-6.png)

6. Testing cookie editing for admin access

We set the "SessionToken" value to be "test" to see if any sessiontoken value will give admin access

![alt text](image-9.png)

After refresh of website we see that we are given admin access.

![alt text](image-10.png)

7. Adding id_rsa to a file

![alt text](image-11.png)

8. Testing ssh for user james with id_rsa

Did not work we dont have passsword

![alt text](image-12.png)

9. Password cracking using john the ripper

Running john the ripper on id_rsa file

![alt text](image-13.png)

By entering james13 in the passphrase for key "id_rsa" we are logged in.

![alt text](image-14.png)

We take a look in the machine and locate the first flag

![alt text](image-15.png)

**Question 2: Escalate your privileges and get the flag in root.txt**

We look more into the machine

![alt text](image-16.png)

Looking for hidden direcotriies

![alt text](image-17.png)

Decrypt using rot37 decoder on web.

![alt text](image-18.png)



## Conclusion