invite.me
============

# What are you looking at?
Invite me is a project made for prom night in my tech high school. The main point was to create application able to :
- create invitation and declaration
- send invitation and declaration to the users with e-mail
- get data from participants usefull for organizators of event (e.g. cars, and divisions)
- record the entrance and exits of participants with qrcodes

To fulfill above requirements I have created three projects:
- invite.me -  webpage to import, send and manage participants
- invite.me-reader - qr code reader which send attendance checkup to the invite.me
- invite.me-scraper - webscraper of MS Teams email addresses from first and last name

## Invite.me 
Main challange of this project and the biggest piece of cake to eat. Web application written in flask framework. I had thought it would be only a few hundred lines of code (LMAO) so flask was a natural winner. Unfortunately a project became biger than I thought, but finally I managed to make it as cute as it was able to.

first view of program
![image](https://user-images.githubusercontent.com/64653975/217074019-6ea1eda7-94c0-46c1-93f3-9da94f2101d6.png)

## Invite.me-reader
Tkinter, the most classical choice to create GUI application. Program just scans QR codes and sends information to invite.me api endpoints.
beta version on my friends surface:
![Untitled](https://user-images.githubusercontent.com/64653975/217072533-8b331774-d992-47a5-a8f6-9370fcafe99b.png)



## Invite.me-scraper
Selenium-based webscraper. The last time when I wrote bots with selenium, I found it easy and really powerful. That was 4 years ago.... and selenium is even more powerful. But my coding skills aren't.
I have wrote this app to run it once so I hope you won't have to use it anyway.

Before a Prom night I was in charge of technical side. I wasn't organiser and I really didn't want to play "a big Mr. manager" role so finding and organising teachers' and students' emails was a minior problem. I have had only first and last names of participants and I have used MS Teams feature to scrap emails. When you type first and last name of user in Teams' organization, you will get a dropdown list with user object. That object contains email addres "ID" attached to the micrsoft domain. I have used this hack to get all participants organization e-mail addreses.

example of fetching data

![image](https://user-images.githubusercontent.com/64653975/217073040-02277e91-2928-4daf-9668-0e5c9f0d1d06.png)


