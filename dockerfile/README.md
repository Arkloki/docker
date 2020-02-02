# Dockerfile

## Image

### Base

Racine de la commande :  
```docker image [COMMAND]``` 

#### COMMAND

* ls : _voir les images déjà crée_
* rm : _effacer une ou plusieurs image(s)_
* prune : _retirer les images non utilisées_

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
