# Sem-PI-Main
## Work log
### Raspberry Pi
* OS flashed was Lubuntu (https://lubuntu.net/downloads/)
  Documentation on how to flash the OS is on the same website
  
* Run code without login/entering password
(https://askubuntu.com/questions/967837/how-to-enable-autologin-on-lubuntu-16-04-lts-lightdm)
* Modified the .bashrc to run any script on opening terminal ( Method 2 of https://www.dexterindustries.com/howto/run-a-program-on-your-raspberry-pi-at-startup/)
* Run terminal without password (https://vitux.com/always-launch-terminal-as-root-user-sudo-in-ubuntu/)
* Installed tkinter: (    `sudo apt-get install python-tk`) 
* Run terminal on boot (https://stackoverflow.com/questions/36466500/on-raspberry-pi-auto-start-terminal-after-login)

    `sudo nano ~/.config/lxsession/Lubuntu/autostart`
  Type @lxterminal in the file
* To use putty we need t o enable SSH on the pi (    `sudo systemctl enable ssh`) (    `sudo systemctl start ssh`)
* To set up any computer as a monitor for the raspberry pi, follow the linked video and download the program (does not require installation) https://youtu.be/AJ7skYS5bjI

### Open GUI and code into raspberry pi using any monitor.
* Install puTTy and Install Xming for windows (Xquartz for mac)
* Open both puTTy and Xming applications 
* Find the IP Address from raspberrypi by typing sudo ifconfig
* Write the IP address on puTTy and go and expand SSH tab >> expand X11 >>Enable x11 forward>> localhost: 0.0 (127.0.0.1:0.0) >>Xauthority → point to xming.exe file. (https://superuser.com/questions/592185/how-do-i-get-x11-forwarding-to-work-on-windows-with-putty-and-xming)
* Open and type in username/pass


### MPU6050
Can use  sudo i2cdetect -y 1 to check whether there is an I2C connection
    `sudo apt install python3-smbus`
     `pip install mpu6050-raspberrypi`

https://pypi.org/project/mpu6050-raspberrypi/



### TmodTC1
https://designspark-pmod.readthedocs.io/en/latest/installation.html
`sudo apt-get install python-pip python-dev libfreetype6-dev libjpeg-dev build-essential`
`sudo pip install designspark.pmod`

Pin    ->   PI Connection
* 3    ->      21
* 4    ->      23
* 1    ->      26

