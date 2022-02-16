# Minecraft-Server

NB:
In order for secrets not to be uploaded to git: `git update-index --assume-unchanged config/essentials_discord_config.yml`
To undo: `git update-index --no-assume-unchanged config/essentials_discord_config.yml`

Initialise server and add docker config:
- Create env file

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

Configure sorting permissions
- `lp group default permission set chestcleaner.clicksort true`

Backups:
- tbc