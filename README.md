# Snapped-Phish-ing-Line

Write-ups "Snapped Phish-ing Line" Tryhackme Chall | https://tryhackme.com/room/snappedphishingline

------------------------------------------------------------------------------------------------------

1. Who is the individual who received an email attachment containing a PDF?

  - Just open phish-emails folder and reviews all emails :)
    
![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/45053c56-5e0b-479a-a13e-b67e75418b89)

2. What email address was used by the adversary to send the phishing emails?

  - See the "FROM" line in the mail.

![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/ce1a4147-f09d-476e-ae7c-3694aaf11c1d)

3. What is the redirection URL to the phishing page for the individual Zoe Duncan? (defanged format)

  - Use CyberChef to defang the URL :

![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/162a0102-3f6d-46c7-b347-83a993b429e0)

You just need to see the code source of the .html phishing page and you got the URL redirection. 

![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/3c4aee74-90bd-4ead-a0b1-c28d0a815f39)

4. What is the URL to the .zip archive of the phishing kit? (defanged format)

  - Just enumerate the website :

![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/d2997044-eeaf-4fb3-9e8e-fcac05f3f7f1)

Use Cyberchef to defang the URL. 

4.What is the SHA256 hash of the phishing kit archive?

  - Download the .zip archive, open the terminal and use sha256sum on the file

![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/cae8bd2d-66f4-430d-a156-1a50d4687864)

5. When was the phishing kit archive first submitted? (format: YYYY-MM-DD HH:MM:SS UTC)

  - Use the famous site https://www.virustotal.com and put the hash of the .zip archive and go to the good place to get the answer ;) 

![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/854ef306-1d47-4343-98fa-1d47641f1d29)

6. When was the phishing domain that was used to host the phishing kit archive first registered? (format: YYYY-MM-DD)

  - Generally i use https://urlscan.io/ but i did not find the answer on this website. So use https://threatbook.io/

![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/b113f359-dc84-4822-9ab3-ac1dc0cbbda8)

7.  What was the email address of the user who submitted their password twice?

  - When you enumerate the website you can see a log.txt search into this file.

![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/0e7b64a1-d324-46df-a237-e43d7ffd5ede)

8. What was the email address used by the adversary to collect compromised credentials?

  - Open the .zip archive, and search the good file to get the answer. (clue is in the "Validation" folder and in .php file.

9. The adversary used other email addresses in the obtained phishing kit. What is the email address that ends in "@gmail.com"?

  - Unzip the .zip archive and get a simple grep command with -r  in this folder.

  ![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/1e40722e-7655-4cd5-8dd3-906860b7e041)

10.  What is the hidden flag?

  - When you enumerate the website you fond a flag.txt file.

![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/8590360c-7424-478c-8877-2a8687eb89f7)

Base64 ? Yeah juste decode him :) 

![image](https://github.com/MBAY-Clement/Snapped-Phish-ing-Line/assets/59869618/efe780a1-5329-44b5-8049-cecc509ae096)

 (; noitcerid thgir eht ni srettel eht tup 

-----------------------------------------------------------------


Thanks Orzykf and Tryhackme for this funny chall ! 








