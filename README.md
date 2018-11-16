# IST-590-Week-8-Project
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

<img src="https://github.com/vaidehirana/IST-590-Week-8-Project/blob/master/Blue%201.gif" widtch="800">

When I opened Red, Green and Blue target and clicked salesperson info on each page, I noticed one pattern in url where each salesperson had an ID assigned. I tried manipulating the url by adding comment ' after the ID number. In Green and Red page there was no error, it simply redirected but in the blue target page there was a SQL error “Database query failed”. This error gave away SQL injection vulnerability on Blue target page, which was tasted by replacing id number with the SQL syntax ``` ' OR SLEEP(5)=0--' ```as shown in the video. This SQL syntax changes to ``` %27%20OR%20SLEEP(5)=0--%27 ``` when encoded in the url. This paused the site for 4-5 seconds confirming a successful SQL injection.

Vulnerability #2: Session Hijacking/Fixation

<img src="https://github.com/vaidehirana/IST-590-Week-8-Project/blob/master/Blue%202.gif" widtch="800">

## Green

Vulnerability #1: Cross-Site Scripting (XSS)

<img src="https://github.com/vaidehirana/IST-590-Week-8-Project/blob/master/Green%201.gif" widtch="800">

Vulnerability #2: Username Enumeration

<img src="https://github.com/vaidehirana/IST-590-Week-8-Project/blob/master/Green%202.gif" widtch="800">

## Red

Vulnerability #1: Cross-Site Request Forgery (CSRF)

<img src="https://github.com/vaidehirana/IST-590-Week-8-Project/blob/master/Red%201.gif" widtch="800">

Vulnerability #2: Insecure Direct Object Reference (IDOR)

<img src="https://github.com/vaidehirana/IST-590-Week-8-Project/blob/master/Red%202.gif" widtch="800">

## Notes

It was difficult to access the website, it showed error everytime I was trying to open it
