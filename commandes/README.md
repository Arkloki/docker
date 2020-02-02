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
  
## Image

### Base

Racine de la commande :  
```docker image [COMMAND]``` 

#### COMMAND

* ls : _voir les images déjà crée_
* rm : _effacer une ou plusieurs image(s)_
* prune : _retirer les images non utilisées **dangling**_
* pull : _Download une image depuis le registry_
* inspect : _permet d'inspecter une image , fonction aussi avec le format go_

### Build

Racine de la commande :  
```docker image build [Option] <PATH>``` 

On utilise en regle general la commande de cette maniere:    
```docker image build -t <nom>:<version> .``` 
* -t : un tag
* . : le chemin par defaut soit le fichier Dockerfile ce situant directement à l'emplacement ou on ce situe  
  
On peux specifier le chemin du Dockerfile et le renommer:  
```docker image build -t <nom>:<version> -f <nom du dockerfile> <chemin absolue>```  
* -t : un tag
* -f : pour preciser qu'on utilise un autre fichier

## Commandes avancées
  * ```docker container rm -f $(docker container ls -aq)```  
  => _efface tous les containeurs meme ceux en cours d'exécution_
  
  * ```docker inspect --format '{{ .NetworkSettings.IPAddress }}' <Container ID>```  
  => _Permet de sortir l'ip d'un containeur via Json_
