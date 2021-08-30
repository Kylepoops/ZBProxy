# ZBProxy 
🚀Easy proxy your data at the best privacy, giving you better experience enjoying Minecraft.  
Support multiplatform because of Golang\'s attributes.  
一键搭建Minecraft加速IP软件，作者[B站@贴吧蜡油](https://space.bilibili.com/404017926 "点我前往空间")。  
本项目遵守国际化理念，所以代码内注释以及README都将以英语编写，可借助翻译工具辅助阅读。
## What can it do?
In many situations you can use Nginx ```proxy_pass``` to easy proxy your Minecraft data.  
The complete code is as follows:
```
stream {
    server {
        listen 25565;
        proxy_pass TARGET_SERVER_ADDRESS;
    }
}
```
But start from 2020, Hypixel set up an authencation of the player login address.  
If you do not login from their official address as known as ```mc.hypixel.net:25565```, you will not be able to join the game.  
The original method is to cheat the server by modifying the ```hosts``` file.  
But that\'s too complicated for people who don\'t know the principle.  
We studied its working principle, and successfully bypassed the detection by modifying the sent data at the technical level.  
The product of the research is what you see now as ZBProxy.  
For players, just enter the address of your proxy server, you can join the game **directly** as usual.
### Is it safe?
There is no need to worry about privacy at all, because the connection to any Minecraft server which requires online verification is fully **encrypted**.  
Our code is completely open source, so you can freely check whether there is a backdoor.
## How to use it?
1. Download the compiled executable file at [releases page](https://github.com/layou233/ZBProxy/releases/ "releases").  
2. Run it, and your data proxy service is now established!  
For Linux system, you may need to give permissions to the executable file in order to solve problems that cannot run or run blocked. Just enter the following command:
```shell
chmod 777 PATH_OF_THE_FILE
```
3. Ensure the port **25565** is fully open on the server.
4. Enter your proxy server IP into your Minecraft client, and join it for game!  
(Since the listening port is **25565**, you don\'t need to input the port number in the client, and the client will complete it automatically)

## TODO List
1. Complete the function of modifying MOTD.  
2. Allows users to change settings directly through parameters.
