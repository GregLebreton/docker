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

        $ sudo apt-get install docker-ce docker-ce-cli containerd.io -y
        
2) CREER UN COMPTE SUR DOCKER HUB:

        https://hub.docker.com
        
 * clonage du repo Docker:

        $ sudo git clone https://github.com/GregLebreton/docker.git
        
  
3) CONSTRUCTION DE L'IMAGE:
 
        $ docker build .
  
4) TAG DE L'IMAGE:

        $ docker tag <ID_de_l'image> <nom_de_votre_registre>/<nom_de_l'image>:<tag>
        
  * ou on peux tagger l'image lors du docker run:

        $ docker run -d -p 80:80 -t <nom_de_l_image_docker>:<tag_de_l_image>
  
5) DEMARRER UN CONTENAIRE DE L'IMAGE EN Y MAPPANT LE PORT 80 DE LA MACHINE HÔTE:

        $ docker run -d -p 7000:80 <nom_de_votre_registre>/<nom_de_l'image>:<tag>

6) VISITER SON NAVIGATEUR A L'ADRESSE:

        0.0.0.0:7000


Autres commandes utiles:

   - push un conteneur sur son registre DockerHub:

          $ docker push
          
   - afficher les images docker:

          $ docker ps
          
   - afficher les containers docker:

          $ docker ls
    
   - Effacer une image:

          $ docker rmi

   - Effacer un conteneur:

          $ docker rm

      
   

  
  
