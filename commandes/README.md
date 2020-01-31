# DOCKER COMMAND

### Commandes de bases
  * ```docker container run [Options] <Name Image> <COMMAND> ```  
  => _lance un containeur_  
  
  * ```docker container ls [Options]```  
  => _liste les containeurs en cours d'execution _
  
  * ```docker container start <Container ID>```  
  => _lance un containeur qui à été stoppé_
  
  * ```docker container exec [Options] <Container ID> <COMMAND> ```  
  => _execute une commande dans un container actif_
  
##### Types d'options :    
  * "-ti" : _TTY interactif du conteneur_
  * "-d" : _le containeur est lancé en background_  
  
###### Options specifique à **ls**
  * "-a" : _permet de voir tous les containeurs meme ceux inactif_
  * "-aq" : _permet de voir tous les **ID** des containeurs meme ceux inactif_
  
##### Types de COMMAND : 
  * "Bash" : _lance un shell dans le containeur_
  * "Echo <text>" : _affiche du texte à la fin du lancement du containeur_

### Commandes avancées
  * ```docker container rm -f $(docker container ls -aq"```  
  => _efface tous les containeurs meme ceux en cours d'exécution_
