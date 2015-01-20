# ArduinoYunFactoryReset
A small write up on how to reset Arduino Yun when you think you might have messed up the configurations

Step 1 - Upload the Yun Serial Terminal Code in the Yun from examples in the IDE. If you are not able to upload it for various reasons, use the reset button for 324 and try again. Once this is done, open the serial termnial and select *NEWLINE* at the bottom right of the page. Remember, all the commands you want to write will be written using the small writing bar on top of the page. To enter the commands to the console, press enter.

Step 2- Wait for a few minutes, this is the time when your Linux is booting up, be patient. You will see a screen loading a few commands etc for bootup. Wait till you see Press f- for failsafe mode. There is a way to reset your arduino from here too, but I have tried a few times and failed to make it work from here. Wait till you seen *root@(none)/#*

Step 3- At this place, press *ls* and see all the files. 

Step 4 -Go to cd/usr/bin and execute a command using this ./reset-to-factory-anyway . Once the command is executed, you should reboot your Yun using reboot. 

At this point let me also remind you to go through the code for serial teminal, to log in as root and follow above commands when you see jff2 init , press 1 and enter. This will make your systems connect at 115200 baud.

If all the steps are executed , you will see that the above process will follow and finally you will be logging in as root@(Arduino)# . 
When you see that, check you Wifi network Manager, you will see Arduino Yun XXXX there. You can now set the password and start from scratch.


All the modules that you install are going to take up the 16MB space given on board, my advice is to insert an external memory card and start a file system on that to make things work.

In case things are not working out, just write to Arduino, the team is AMAZING, they will help you out :) 

This goes without saying , what I have written above is my own test, in case you can suggest any improvements, feel free to write back to me.
