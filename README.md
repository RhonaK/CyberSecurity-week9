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
    - Using SQL injection to the id attribute of each section (Blue, Green and Red), we can see from above that trying to break by ' OR       1=1'-in the Blue section we receive the message "Database query failed."But for the Red and Green sections the SQL injection             statement redirected the screen and it cannot do any change to them

Vulnerability #2: Session Hijacking/Fixation
  - [x] GIF Walkthrough: 
    <img src='week9(blue_2).gif' title='Session Hijacking/Fixation' width='' alt='' />
  - [x] Steps to recreate:
     - Login in to the Blue section, and once logged in change the url to public/hacktools/change_session_id.php (provided in week 9-          hints). Also, from this the session ID is retreived
     - The attacker changes the session ID using the provided change_session_id.php.
     - The attacker is now able to access the victims session.
     - This hacking method demonstrates that the session can be hijacked and user informations can be stolen
## Green

Vulnerability #1: __________________

Vulnerability #2: __________________


## Red

Vulnerability #1: __________________

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work

