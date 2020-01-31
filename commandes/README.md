# DOCKER COMMAND

### Commandes de bases
  * ```docker container run [Options] <Name Image> ```  
  => _lance un containeur_
  
  * ```docker container start <Container ID>```  
  => _lance un containeur qui à été stoppé_
  
  * ```docker container exec [Options] <Container ID> <COMMAND> ```  
  => _execute une commande dans un container actif_
  
##### Types d'options :    
  * "-ti" : _TTY interactif du conteneur_
  * "-d" : _le containeur est lancé en background_
