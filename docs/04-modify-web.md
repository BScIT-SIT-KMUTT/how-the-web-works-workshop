# 04 Modify Web
\# How the Web Works Workshop  
\# SIT@KMUTT


## Modify Web Page Source
The main page of this web page is `index.html`. We will modify this file using `VS Code` on the local machine and upload to the server.

1. Open `CMD`. You should be in `C:\Users\Student`.

2. Clone git repository of the web on your local machine.  
`git clone https://github.com/BScIT-SIT-KMUTT/how-the-web-works-workshop.git`  

3. Change working directory to `src` directory. Note that pressing `TAB` key will auto-complete the directory name.   
`cd how-the-web-works-workshop\s` `press TAB`  

4. Open the `src` directory in `VS Code`.  
`code .`  
Click `Yes, I trust the authors`.  

5. Open `index.html` and `style.css` file.  

6. Make the following changes. (May use `Live Preview` extension to see changes.)  
6.1 Change `เข้าระบบสมัครเรียน` in line 35 to `Apply`  
6.2 Change `Database` in line 73 to `Database Admin`  
6.3 Swap card 2 and card 3  
6.4 Change `grid-item.background-color` to red in `style.css`

7. Save changes and upload to the server.  
`scp -r * devYY@htwwXX.sit.kmutt.ac.th:how-the-web-works-workshop/src/`  

8. Refresh your web page on the browser.  
<br>

---
[RETURN TO HOME](/README.md)