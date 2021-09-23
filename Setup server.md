# minecraft-server
ubuntu how to setup a minecraft server

sudo apt update
sudo apt upgrade

sudo adduser minecraftuser

sudo usermod -aG sudo minecraftuser

su - minecraftuser

sudo apt install wget

sudo apt install openjdk-8-jdk -y

sudo java -version

sudo apt install screen

sudo mkdir minecraftdir

cd minecraftdir

sudo wget -O minecraft_server.jar https://s3.amazonaws.com/Minecraft.Download/versions/1.11.2/minecraft_server.1.11.2.jar

sudo chmod +x minecraft_server.jar

sudo vi eula.txt

sudo java -Xmx1024M -Xms1024M -jar minecraft_server.jar nogui

stop

sudo screen -S "Minecraft Server Screen"

sudo java -Xmx1024M -Xms1024M -jar minecraft_server.jar nogui

CTRL+A+D

sudo screen -r
