# MQTTBroker
Installation Mosquitto Rasberry Pi Zero W

# Atualizar Pacotes
+ sudo apt-get update
+ sudo apt-get upgrade

# Instalar mosquitto
+ sudo apt-get install mosquitto -y
+ sudo apt-get install mosquitto-clients -y

# Configurar mosquitto
+ sudo nano /etc/mosquitto/mosquitto.conf

* Dentro deste arquivo, localize a apague a seguinte linha:
+ include_dir /etc/mosquitto/conf.d

* Após isto, inclua estas linhas:
+ allow_anonymous false
+ password_file /etc/mosquitto/pwfile
+ listener 1883

# Adicionar Usuario e Senha
+ sudo mosquitto_passwd -c /etc/mosquitto/pwfile pi
+ password:raspberry
+ reenter password:raspberry

# Reniciar Servidor
+ sudo reboot
