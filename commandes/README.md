# DOCKER COMMAND

## Commandes de bases
  * ```docker container run [Options] <Name Image> <COMMAND> ```  
  => _lance un containeur_  
  
  * ```docker container ls [Options]``` ou ```docker ps [Options]```   
  => _liste les containeurs en cours d'execution_
  
  * ```docker container start <Container ID>```  
  => _lance un containeur qui à été stoppé_
  
  * ```docker container exec [Options] <Container ID> <COMMAND> ```  
  => _execute une commande dans un container actif_
  
#### Types d'options :    
  * "-ti" : _TTY interactif du conteneur_
  * "-d" : _Le containeur est lancé en background_  
  * "-p" : _Publication des ports manuellement \[host]:\[containeur]_
  
##### Options specifique à **ls/ps** :
  * "-a" : _permet de voir tous les containeurs meme ceux inactif_
  * "-aq" : _permet de voir toutes les **ID** des containeurs meme ceux inactif_
  
#### Types de COMMAND : 
  * "Bash" : _lance un shell dans le containeur_
  * "Echo \<text>" : _affiche du texte à la fin du lancement du containeur_

## Commandes avancées
  * ```docker container rm -f $(docker container ls -aq)```  
  => _efface tous les containeurs meme ceux en cours d'exécution_
  
  * ```docker inspect --format '{{ .NetworkSettings.IPAddress }}' <Container ID>```  
  => _Permet de sortir l'ip d'un containeur via Json_
