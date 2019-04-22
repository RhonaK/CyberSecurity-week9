# CyberSecurity-week9
WELCOME 
# Project 8 - Pentesting Live Targets

Time spent: **10** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection (SQLi)
  - [x] GIF Walkthrough: 
    <img src='week9(blue_1).gif' title='SQL Injection' width='' alt='' />
  - [x] Steps to recreate:
    - The exploit exists in the salesperson.php page.
    - The exploit is done via the url.
    - Using SQL injection to the id attribute of each section (Blue, Green and Red), we can see from above that trying to break by 
       ```' OR 1=1'--  ```in the Blue section we receive the message "Database query failed."But for the Red and Green sections the SQL       injection statement redirected the screen and it cannot do any change to them

Vulnerability #2: Session Hijacking/Fixation
  - [x] GIF Walkthrough: 
    <img src='week9(blue_2).gif' title='Session Hijacking/Fixation' width='' alt='' />
  - [x] Steps to recreate:
     - Login in to the Blue section, and once logged in change the url to ```public/hacktools/change_session_id.php``` (provided in week        9- hints). Also, from this the session ID is retreived
     - The attacker changes the session ID using the provided change_session_id.php.
     - The attacker is now able to access the victims session.
     - This hacking method demonstrates that the session can be hijacked and user informations can be stolen
## Green

Vulnerability #1: Username Enumeration
  - [x] GIF Walkthrough: 
    <img src='week9(green_1).gif' title='Username Enumeration' width='' alt='' />
  - [x] Steps to recreate:
     - The GIF illustrates that when you enter in a username that exisits in the system/database along with a random password and you          inspect the page the class of the span HTML attribute is ```failure ``` Also, when a wrong username/ a username that isn't in the              system is entered with a random password, inspect will display ```failed```
     - Also,using the given username "jmonroe99" we can see that a valid username shows a bold error.
     - An incorrect username shows a not-bolded error
        
  
  
Vulnerability #2: Cross-Site Scripting
  - [x] GIF Walkthrough: 
    <img src='week9(green_2).gif' title='Cross-Site Scripting' width='' alt='' />
  - [x] Steps to recreate:
  - In the Green section, click on Contact Us and enter into the form, where in the Feedback textbook write an alert script such as         ```<script>alert('RONA found the XSS!')</script>```. Then login and from there, click on Feedback on the dashboard and you will          encounter your Feedback lssert pop-up.

## Red

Vulnerability #1: __________________

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work

