# Docker

  - sudo apt-get remove docker docker-engine docker.io containerd runc
  - sudo apt-get update
s- sudo apt-get install \ apt-transport-https \ ca-certificates \ curl \ gnupg-agent \ software-properties-common
  - curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

  - sudo apt-key fingerprint 0EBFCD88
  
  ```
  pub   rsa4096 2017-02-22 [SCEA]
        9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
  uid           [ unknown] Docker Release (CE deb) <docker@docker.com>
  sub   rsa4096 2017-02-22 [S]
  ```
  - sudo add-apt-repository \ "deb [arch=amd64] https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) \ stable"
  
  - sudo apt-get update
  - sudo apt-get install docker-ce docker-ce-cli containerd.io
  - sudo apt-get install docker-ce=5:19.03.5~3-0~ubuntu-bionic docker-ce-cli=5:19.03.5~3-0~ubuntu-bionic containerd.io
  
# Docker super-user

  - sudo groupadd docker
  - sudo usermod -aG docker $USER
  - newgrp docker
  
# Docker-compose

  - sudo curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
  - sudo chmod +x /usr/local/bin/docker-compose
  
# Check if every is ok

  - docker -v
  - docker-compose -v
  
# Basic command

  - docker container ps
  - docker-compose up -d
  - docker-compose down
  - docker-compose restart
  - docker-compose kill
  - docker exec -it <name container> bash
  - docker images
