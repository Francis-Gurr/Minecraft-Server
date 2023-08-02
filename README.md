# Minecraft-Server

Initialise server and add docker config:
- Create env file

Start docker
- `sudo docker-compose up`

Create systemd service
- `sudo cp minecraft-docker.service /etc/systemd/system/minecraft-docker.service`
- `sudo systemctl daemon-reload`
- `sudo systemctl start minecraft-docker`
- `sudo systemctl status minecraft-docker`
- `sudo systemctl enable minecraft-docker`

Client instructions
- Pre-requisites: Java and Python3 
- Download `ourcraft-client-installer.py`
- Place inside an empty folder and run the script
