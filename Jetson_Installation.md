**Jetson nano software installation**
*1. Write Jetbot image into micro SD card*
1. Micro SD card need more than 64GB empty space
2. Download JetBot image provided by NVIDIA and unzip it from https://drive.google.com/file/d/1G5nw0o3Q6E08xZM99ZfzQAe7-qAXxzHN/view
3. Connect the Micro SD card to PC via card reader
4. Download Etcher software from https://www.balena.io/etcher/
5. Install Etcher and follow promps to write the jetbot image from step "2" into the micro sd card
*2. Startup Jetson Nano Developer Kit*
1. Inseart the micro sd card into the slot on jetson nano board
2. Connect the keyboard and mouse through the USB ports on the jetson nano board
3. Connect the monitor throught HDMI port on the jetson nano board
4. Plug in micro usb power supply or 5V/4A 20W DC power supply
5. Turn on the jetson nano by using the on/off switch on the waveshare board
6. Using account neme: jetbot and password: jetbot if login required
7. Click Network icon on top-right of Desktop and connect WIFI
8. Turn off the jetson nano using the ubuntu graphic UI or using "sudo shutdown now" in terminal
*3. Access jetbot via web*
1. Now we could remove monitor, keyboard and mouse
2. Power on the jetbot
3. After booting, IP address of the jetbot will shows on OLED display
4. Open any web browser in the computer and type in http://<jetbot_ip_address>:8888 will open the jupyter notebook for jetbot access
*4. Update jetbot software, in the terminal using the following commands"
1. git clone https://github.com/NVIDIA-AI-IOT/jetbot
2. cd jetbot
3. sudo python3 setup.py install
*5. Replace the old notebooks with the new notebooks by entering*
1. sudo apt-get install rsync
2. rsync jetbot/notebooks ~/Notebooks
*6. Check jetbot power mode"
1. Set to 5W by using "sudo nvpmodel -m 1"
2. Set to 10W by using "sudo nvpmodel -m 0"
3. Check current power mode by using "sudo nvpmodel -q"
4. Choose the power mode base on your need
*7. Running features by excuted the jyputer notebook in notebook folder, the feature including"
1. Collision avoidance
2. Line following
3. Line following + stop when obstruct present, go when obstruct remove
4. Object following + stop when close to the object
