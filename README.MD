                                              ###### DOCKER ######



Une simple Dockerfile contenant un NGINX 1.19 pouvant accueillir un site web.

processus:

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

    $ docker tag <ID_de_l'image> <nom_de_votre_registre>/<nom_de_l'image>:<tag>
  
4) DEMARRER UN CONTENAIRE DE L'IMAGE EN Y MAPPANT LE PORT 80 DE LA MACHINE HÔTE:

    $ docker run -d -p 80:80 <nom_de_votre_registre>/<nom_de_l'image>:<tag>

5) VISITER SON NAVIGATEUR SUR LOCALHOST (127.0.0.1)
  
  
