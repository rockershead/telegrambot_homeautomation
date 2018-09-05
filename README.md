# telegrambot_homeautomation

Bots are now the future.It can helps us control devices in our homes or even give us weather/news updates.

Hence I have used telegram's own api to create a bot which communicates with the raspberry pi 3 to get readings from my temperature/humidity sensor,control led and also check if led is on or off. The plus point is that I was able to make a notification system when temperature exceeds 25 degrees Celsius and if motion sensor detects any movement;a notification message will be sent to my phone.

What is used?

Raspberry Pi 3 and the sensors
Telegram server (Installed on an ubuntu 16.04 LTS cloud server)
Mobile phone with telegram app installed


You can see that you dont need a lot of items but a lot of codeing has to be done(the code is not that long). 

How it works?

The message will be send from my telegram app and then sent to the ubuntu telegram server where my code processes the sent message.The message is then send to raspberry pi using network socket programming. The raspberry pi code processes the message and checks what needs to be done,say it needs temperature readings.The readings will be sent back to the ubuntu server and back to my phone.Please take note that that TCP protocol is being used in all data transfers.

All code is written in python.There will be 2 sets of code. One for notification and 1 for the user to query whatever they want.Plus I am using 2 different ports,one for notification and for client query/request. So lets look at the codes.

