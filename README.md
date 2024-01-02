# SJTU Meow Wang Communication Platform

1. Based on Websocket, front-end using vue, back-end using Node.js,achieved 96 in this course.

2. It supports multi person and multi room chat, and the front end adapts to the PC and mobile terminals

3. To access devices in the same IP, you need to modify the IP (localhost) in chatroom.vue to the local IP.
 
4. Customized and random login names are implemented, and each name will be bound with a random avatar, and the same name and avatar will be entered again.

5. Try the optimization and mobile terminal design technology learned in the course as much as possible, and use more flex and percentage height width to adapt the page to the scenarios such as iPad and mobile phone.

 6.5.13 Update: [deployed on Alibaba Cloud, sadly,the server is expired，you can see the outcome pictures below]( http://47.107.111.88:8080/ )

7. 5.18 Update: fixed the problem of css and avatars, adopted a more beautiful page design, added customized avatars, adapted this group project on the ECS to Jiaotong University Meowang Chat Room, and used admin as the nickname to use personalized avatars.

8. Please contact me if the trial server is unavailable at the expiration.
# Instructions:

1. Install the npm

2. Execute node server.js in the root directory to start the server

3. Open index.html in the dist directory and directly use the packaged file

4. Split the terminal and execute npm run serve in the root project to achieve hot update

5. Use npm run build to package (the load path may be missing "./" after the build, and you can modify the publicpath in vue.config.js to "./" in advance)

# Login 
![](https://github.com/sjtuLLWWTT/SoftwareEngineeringProject/blob/main/preview/pcfront.png)
# PC
![](https://github.com/sjtuLLWWTT/SoftwareEngineeringProject/blob/main/preview/聊天.png)
# Iphone
![](https://github.com/sjtuLLWWTT/SoftwareEngineeringProject/blob/main/preview/移动端.png)
# Updated Login
![](https://github.com/sjtuLLWWTT/SoftwareEngineeringProject/blob/main/preview/pcfrontt.png)
# Chatroom 
![](./preview/聊天2.png)
