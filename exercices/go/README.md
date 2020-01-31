# Multistage  

Exercice de multistage avec Dockerfile  

### Dockerfile  

C'est le dockerfile basique , on remarque qu'il fait 276 Mb  

=> ```docker image build -t who:1.0 .```  

### DockerfileV2  

C'est sa fome multistage , on remaques qu'elle ne fait plus que 6Mb  

=> ```docker image build -t who:2.0 -f <chemin_absolu>/DockerfileV2```  

_methode pour lancer un build sur un dockerfile renommé_