# 03 Deploy Web
\# ONE DAY with me IT BANGMOD  
\# How the Web Works Workshop  
\# SIT@KMUTT


## Your Designated URL
Each participant is given an account on the school Virtual Machine (VM). The URL for each account is as follows.  
* hostname : `onedayXX.sit.kmutt.ac.th`  
* private URL : `http://onedayXX.sit.kmutt.ac.th/devYY`  
* public URL : `http://oneday24.sit.kmutt.ac.th/teamXX/devYY`  

Replace ***XX*** with your team number and ***YY*** with your user number. For example, the private URL for dev01 in team 07 is http://oneday07.sit.kmutt.ac.th/dev01  

### Exercise
1. Can you view your web page?
2. What is the IP address of your team server?
3. What is the IP address of *public* URL?


---
## Deploy Your Web Pages
In order to deploy your web pages on the server, you need to remote (login) to your server, download your web pages, and config the web server. In this workshop, you will deploy the web pages in *src* directory on this repository.

1. Remote to your server using your user account. Enter the password announced in the workshop.  
``ssh devYY@onedayXX.sit.kmutt.ac.th``  
2. Clone git repository of the web.  
`git clone https://github.com/BScIT-SIT-KMUTT/oneday-web-workshop.git`  
3. Change working directory to _src_ directory. View files in the directory. **Make sure that you are in 'src'.**  
`cd oneday-web-workshop/` `TAB`  
`ls -R`  


```bash

 ```

```bash
docker run --name devYY-nginx -d -p 500YY:80 --restart unless-stopped --mount type=bind,source=.,target=/usr/share/nginx/html nginx:alpine
```