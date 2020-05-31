# hassio-rpi4-docker-compose

## Home Assistant with Portainer for Raspberry Pi 4 in the docker-compose

### 1. Install Docker 

    curl -sSL https://get.docker.com | sh

### 2. Add permission to Pi User to run Docker Commands

    sudo usermod -aG docker pi

Reboot here or run the next commands with a sudo

### 3. Change python alias to python3

    alias python=python3

### 4. Install dependencies for docker-compose

    sudo apt-get install libffi-dev libssl-dev

    sudo apt-get install -y python python3-pip

    sudo apt-get remove python-configparser

### 5. Install docker-compose

    sudo pip install docker-compose
    
### 6. Create directories for Hassio configuration files and scripts

    mkdir -p /home/pi/hassio/{scripts,data,portainer}
    
### 7. Run docker-compose and wait few minutes to start

    docker-compose up -d
    
Hassio will be available on port 8123, Portainer on 9000
