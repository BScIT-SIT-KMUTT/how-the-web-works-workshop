# 03 Deploy Web
\# ONE DAY with me IT BANGMOD  
\# How the Web Works Workshop  
\# SIT@KMUTT


## Your Designated URL
Each participant is given an account on the school Virtual Machine (VM). The URL for each account is as follows.  
* hostname : `onedayXX.sit.kmutt.ac.th`  
* username : `devYY`
* password : *given in the workshop*
* private URL : `http://onedayXX.sit.kmutt.ac.th/devYY`  
* public URL : `http://oneday24.sit.kmutt.ac.th/teamXX/devYY`  

Replace ***XX*** with your team number and ***YY*** with your user number. For example, the private URL for dev01 in team 07 is http://oneday07.sit.kmutt.ac.th/dev01  

### Exercise
1. Can you view your web page?
2. What is the IP address of your team server?
3. What is the IP address of *public* URL?


---
## Deploy Your Web Pages
In order to deploy your web pages on the server, you need to remote (login) to your server, fetch your web pages, and config the web server. In this workshop, you will deploy the web pages in `src` directory on this repository.  

1. Remote to your server using your user account. In `CMD` program, run the following command. Make sure to replace _XX_ with your team number and _YY_ with your dev number. Nothing is shown when enter the password!   
``ssh devYY@onedayXX.sit.kmutt.ac.th``  

2. Clone git repository of the web.  
`git clone https://github.com/BScIT-SIT-KMUTT/oneday-web-workshop.git`  

3. Change working directory to `src` directory. Note that pressing `TAB` key will auto-complete the directory name.   
`cd oneday-web-workshop/s` `press TAB`  

4. View files in the `src` directory. Option R is used to show files and sub-directories.   
`ls -R`  

5. Create and run a `container` with `nginx` as Web Server, set the name of the container to `devYY-nginx`, serve the web page on port `500YY`. For example, if you are `dev03`, create a container with the name `dev03-nginx` listening on port `50003`.  
**Make sure that you are in `src`.**  
```bash
docker run --name devYY-nginx -d -p 500YY:80 --restart unless-stopped --mount type=bind,source=.,target=/usr/share/nginx/html nginx:alpine
```

6. View that your container is running. Check that the container's name and published port are correct.  
`docker ps`

7. On the browser, open your private URL on port `500YY` .  
`http://onedayXX.sit.kmutt.ac.th:500YY`

8. Open `Inspector` / `Network tab`. You may need to refresh your page. Look at Request URL, Remote Address, and the Port.

9. View your web page again using `http://onedayXX.sit.kmutt.ac.th/devYY` instead.

10. *Congratuation!!* You have deployed your web page successfully. Exit the server with `exit` or `logout` or `CTRL+D`.