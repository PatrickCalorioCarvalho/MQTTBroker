# MQTTBroker
Installation Mosquitto Rasberry Pi Zero W

sudo apt-get update
sudo apt-get upgrade

sudo apt-get install mosquitto -y
sudo apt-get install mosquitto-clients -y

sudo nano /etc/mosquitto/mosquitto.conf

#Dentro deste arquivo, localize a apague a seguinte linha:
include_dir /etc/mosquitto/conf.d

#Após isto, inclua estas linhas:
allow_anonymous false
password_file /etc/mosquitto/pwfile
listener 1883

sudo mosquitto_passwd -c /etc/mosquitto/pwfile pi
password:raspberry
reenter password:raspberry

sudo reboot
