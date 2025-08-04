# ⚔️ Pre-Security - Offensive Security Intro

## 🧠 What I learned

### Task 1 - What is Offensive Security
- To outsmark a hacker, we need to be able to think like them
- Offensive security involves hacking, exploiting bugs, and finding loopholes in applications to gain unauthorized access
- Being an "ethical hacker" will allow us to find vulnerabilities and help us improve our system against malicious attackers

### Task 2 - Hacking your first machine
- I started a virtual machine for a first time to simulate environment
- I used terminal which is very similar to command prompt and powershell in Windows
- Used command: gobuster -u http://fakebank.thm -w wordlist.txt dir
- to list down hidden pages in the "FakeBank's" website
- The argument -u requires the website
- The argument -w takes a list of words to iterate through and wordlist.txt file was passed
- /bank-transfer was found as a result and this page can be used to transfer money from one account to the other
- This allows unauthorized transaction to occur
- Successfully transferred $2000 to the test account

### Task 3 - Careers in cyber security
- There are lots of careers in cyber security but offensive security is also known as "Red Team"
- Mentioned roles are: Penetration Tester, Red Teamer, Security Engineer