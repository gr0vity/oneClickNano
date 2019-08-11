# OneClickNano : Run your nano node with monitor & stats
Setup a Nano Currency Monitor with graphics.
Example : 
- **Monitor** : http://95.216.228.244/monitor/
- **Stats** with graphics : http://95.216.228.244/stats/

The following docker containers are launched :
- **Nano** V18.0 >> https://hub.docker.com/r/nanocurrency/nano
- Forked **Netdata** with nano stats >> https://cloud.docker.com/u/gr0vity/repository/docker/gr0vity/nanonetdata
- Forked **nanonodemonitor** >> https://cloud.docker.com/u/gr0vity/repository/docker/gr0vity/nanonodemonitor
- **Nginx** https://hub.docker.com/_/nginx


## Run with Docker (Docker-compose)
- `Install Docker-CE` : https://docs.docker.com/install/linux/docker-ce/ubuntu/#set-up-the-repository
- `Install Docker-Compose` : https://docs.docker.com/compose/install/#install-compose
- Clone this repository : `git clone https://github.com/gr0vity/oneClickNano.git`
- Navigate into folder : `cd oneClickNano`
- Start Node monitor with docker-compose : `docker-compose up -d`
- Modify nanoNodeMonitor settings in config.php : `sudo vi nanoNodeMonitor/config.php` (Add your node address)
- Restart netdata docker-container : `docker restart $(docker ps -q --filter ancestor=gr0vity/nanonetdata:latest)`


## Nano Related
Check out other awesome nano projects: [NanoLinks](https://nanolinks.info)
