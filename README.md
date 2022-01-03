# Minecraft-Server

Initialise server and add docker config:
- Create env file
- `docker-compose up`
- `cp config/essentials_discord_config.yml data/plugins/EssentialsDiscord/config.yml`
- `docker-compose down`

Reload world gen with terralith
- `docker-compose up`
- login to server
- leave server
- `rm -r data/world/region`

Create systemd service
- `cp config/minecraft-docker.service /etc/systemd/system/minecraft-docker.service`
- `sudo systemctl daemon-reload`
- `sudo systemctl start minecraft-docker`
- `sudo systemctl status minecraft-docker`
- `sudo sytemctl enable minecraft-docker`

Configure firewall
- `sudo ufw allow 25565/tcp`
- `sudo ufw allow 25575/tcp`

Backups:
- tbc