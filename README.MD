                            ###### DOCKER ######


  Une simple Dockerfile contenant un NGINX 1.19 pouvant accueillir un site web.

1) INSTALLATION DE DOCKER (DEBIAN 10):

  $ sudo apt-get update

  $ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
    
  $ curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
  
  $ echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

  $ sudo apt-get update

  $ sudo apt-get install docker-ce docker-ce-cli containerd.io
  
2) CONSTRUCTION DE L'IMAGE:
 
  $ docker build .
  
3) TAG DE L'IMAGE:

  $ 
  
4) TAG DEMARRER UN CONTENAIRE DE L'IMAGE EN Y MAPPANT LE PORT 80 DE LA MACHINE HÔTE:

  $
  
  
