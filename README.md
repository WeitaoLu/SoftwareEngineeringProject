# SJTU Meow Wang Communication Platform

1. Based on Websocket, front-end using vue, back-end using Node.js

2. It supports multi person and multi room chat, and the front end adapts to the PC and mobile terminals

3. To access devices in the same IP, you need to modify the IP (localhost) in chatroom.vue to the local IP.

4. Customized and random login names are implemented, and each name will be bound with a random avatar, and the same name and avatar will be entered again.

5. Try the optimization and mobile terminal design technology learned in the course as much as possible, and use more flex and percentage height width to adapt the page to the scenarios such as iPad and mobile phone.

6.5.13 Update: [deployed on Alibaba Cloud, click the link]（ http://47.107.111.88:8080/ )

7. 5.18 Update: fixed the problem of css and avatars, adopted a more beautiful page design, added customized avatars, adapted this group project on the ECS to Jiaotong University Meowang Chat Room, and used admin as the nickname to use personalized avatars.

8. Please contact me if the trial server is unavailable at the expiration.
# Instructions:

1. Install the npm

2. Execute node server.js in the root directory to start the server

3. Open index.html in the dist directory and directly use the packaged file

4. Split the terminal and execute npm run serve in the root project to achieve hot update

5. Use npm run build to package (the load path may be missing "./" after the build, and you can modify the publicpath in vue.config.js to "./" in advance)

# development process
* 开发中的整体框架学习了GitHub上的好几个开源代码，最终仿制出一个比较粗糙的版本，实现了基本聊天功能，[见链接](https://github.com/sjtuLLWWTT/Chatroom-vue)  
* 继续开发，把一些开源代码中的功能结合到自己的代码中，成功加入了多房间选择、随机名称，聊天头像等功能。  
* 在多机器问题上，开源代码中基本都只实现本地本机登录，或者ipv6协议（看不懂），因此我学习了一些vue项目部署到局域网、服务器的博客和视频，尝试了将dist部署到华为云（但服务器有点贵，且弹性公网ip不太会设置），并且熟练掌握了在vue2，vue3框架下修改ip使得局域网内设备都可以访问的技术。集群和房间人数过多的问题不太会编程解决，我想到的思路是部署在多台服务器做总服务器，将原先的一台服务器以遍历的形式分发给所有客户端的任务根据性能分配到不同服务器上，在聊天平台设计中，对于一个大房间而言，接受任务是远小于发送任务的，因此可以用少量服务器接受，多台服务器发送，即一台服务器负责接受客户端信息并发送给所有发送用服务器，发送用的服务器分发给自己负责的客户端。另外长连接占用服务器资源较多，对于人数较多时应采取短链接。采用心跳周期断开长时间未响应或发送消息的用户是一种合理的设计。
* 开发过程中遇到了很多奇怪的bug，修bug的同时也更加熟悉了websocket、npm各种指令的原理，熟练了vue框架和路由，一开始用socket.io库，后来学习了使用原生websocket的代码，于是借用了他的设计，50行左右实现了服务端的基本操作，但是没有成功迁移他的心跳时钟（自动断线）设计。  此外很多开源设计中用数据库记录用户信息、消息等，时间所限，我并没有学习数据库的使用。
* 总之在开发的过程中，我从零开始探索vue框架，巩固了之前学到的前端知识，也锻炼了自己的编程能力（极大锻炼了debug能力），对于不熟悉的计网知识有了一些了解。虽然在debug和css布局上“浪费”了很多时间，但我感觉这次大作业还是让我收获很多的。  
* 经过探索，成功将项目部署在了阿里云，使用tmux挂载server进程和client进程，将打包好的文件用live-storage运行。
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
