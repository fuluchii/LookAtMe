###LOOK AT ME项目设计

look at me是和@dodowoo 一起参加hackathon的作品。

#####项目基本由python写成，包含部分coffeescript

####基本设计

![lookat me](https://github.com/fuluchii/JobPool/blob/master/image/lookatme-design.jpg?raw=true "")



- ####website
	
	web由bootle搭建。bottle是一个轻量级python web framework。
	
- ####websocket

	websocekt服务建立和客户端的websocket连接，接受消息并向客户端推送数据。
	主要基于wsgi的websocket服务。
	
- ####数据库

	使用mongodb作为数据库服务。
	
- ####hubot server

	基于github的hubot项目，搭建hubot机器人。
	
	使用基于xmpp协议的gtalk作为adapter，在服务端建立xmpp server，对web-server进行轮询。
	
	当获取数据时，向特定对象发送gtalk msg。
	
- ####SMS 短信server

	使用twilio作为短信服务商，用提供的python-api搭建短信服务器，接受socket-server的信息，触发短信服务。
	
	