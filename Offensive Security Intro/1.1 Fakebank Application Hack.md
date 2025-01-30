# Hacking a Machine

## Step 1: Opening a Terminal
 I used the terminal, also known as the command line, to interact with the computer without relying on a graphical user interface. I began by opening the terminal by clicking on the Terminal icon located on the right side of the screen. 
 
 ![Opening a Terminal](https://github.com/user-attachments/assets/1ec9f011-6186-47f1-a100-7402cb41dace)

 This step marked the starting point for executing commands and navigating the system efficiently.

## Step 2: Using Gobuster to Find Hidden Website Pages
In this part of the activity, I explored how companies often have admin portal pages to facilitate basic operations, such as transferring money between client accounts. However, due to human error or negligence, these pages might not be properly secured, leaving them accessible to attackers searching for hidden pages with admin controls or sensitive data.

To identify such hidden pages on FakeBank's website, I used Gobuster, a command-line security application. By typing the provided command into the terminal, I initiated a brute-force search to uncover potentially hidden resources, reinforcing the importance of securing admin portals against unauthorized access.

![Using Gobuster to Find Hidden Website Pages](https://github.com/user-attachments/assets/6084a664-0a9a-43a6-ba00-3bb66ae779e7)

After running the command `gobuster -u http://fakebank.thm -w wordlist.txt dir`, Gobuster began scanning the FakeBank website using the specified wordlist. The output displayed potential hidden directories and pages that existed on the site. This process demonstrated how attackers could use tools like Gobuster to identify unprotected resources, highlighting the critical need for securing web applications by restricting access to sensitive directories.

![image](https://github.com/user-attachments/assets/e0e7dc7f-a188-42db-90cd-b01019875048)

In the command above, the `-u` flag specifies the website we are scanning (in this case, `http://fakebank.thm`), while the `-w` flag takes a wordlist that Gobuster iterates through to find hidden pages or directories.

![image](https://github.com/user-attachments/assets/5a87da9e-a108-489d-8713-887c342a894f)

As Gobuster runs, it scans the website using each word from the list to identify resources that exist. Any pages or directories successfully found are indicated by a status code of `200`, which means the resource is accessible. This exercise demonstrated how tools like Gobuster can reveal unsecured areas of a website, emphasizing the importance of thorough security practices to mitigate such risks.

## Step 3: Hacking the Bank
In this scenario, after using Gobuster to identify the hidden /bank-transfer page on FakeBank's website. 

![Screenshot 2025-01-22 065805](https://github.com/user-attachments/assets/f9ae71ce-c25f-4f68-b2e5-4797ee3263fa)

I accessed it through the browser's address bar. Upon reaching this page, I realized that it allowed unauthorized access for transferring money between bank accounts. This vulnerability could potentially be exploited by an attacker to steal funds from bank accounts.

![/bank-transfer](https://github.com/user-attachments/assets/d56b0309-e0dd-49f6-88a6-68cb538c50d3)

As an ethical hacker, my role is to identify such vulnerabilities and report them to the bank so they can fix the issue before malicious hackers exploit it. For this exercise, my mission was to transfer $2000 from account number 2276 to my own account (number 8881). 

![Screenshot 2025-01-22 065934](https://github.com/user-attachments/assets/ea3e4b90-24dc-4210-ac04-b30a56270e8a)

![Screenshot 2025-01-22 065954](https://github.com/user-attachments/assets/17a7d34e-ff93-416f-83e6-2062bfdd2f75)

After successfully making the transfer, I navigated to my account page to confirm the balance update. I refreshed the page if necessary to ensure the changes were reflected.

![Account check](https://github.com/user-attachments/assets/26868ef5-e665-4591-b275-cd3b8aa9a7c7)
