### Zerotier-One ARM Docker
This is a modified docker file from zyclonite (which can be found here https://hub.docker.com/r/zyclonite/zerotier/) to support ARM devices. Included is also a docker-compose file to run the docker container.

## How To Use
1. Clone and cd into the root directory
2. Build the docker container ```docker build -t zerotier .```
3. Modify the docker-compose file and replace NETWORK_ID with the id of your zerotier.
4. Create a folder path to /var/lib/zerotier-one/networks.d/ ```mkdir -p /var/lib/zerotier-one/networks.d/```
5. Create a conf file with the network id in /var/lib/zerotier-one/networks.d/ ```touch NETWORK_ID.conf```
    * You can find your network id on your zerotier-one account.
6. Cd back into the cloned repo and run ```docker-compose up -d``` to start the zerotier docker container.
7. Go to your Zerotier-one account and add the device to your allow list.
