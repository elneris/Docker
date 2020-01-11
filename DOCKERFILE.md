# Dockerfile

### FROM

  - Définit l'image de base
  
### MAINTAINER

  - Utilisateur <email>
  
### ENV

  - Définit les variables d'environnement
  - Valeur qui peut être utiliser dans les instructions suivantes du build
  
### COPY

  - Copie des fichiers ou répertoires du système local, dans le système de fichier de l'image
  
### RUN

  - Execute une commande lors du build ( RUN apt-get update && apt-get install ... )
  
### EXPOSE

  - Information sur le port utilisé par l'application
  - Peut être défini dans le docker-compose ou modifié au lancement du container avec l'option -p
  
### VOLUME

  - Détache les données du cycle de vie d'un container ( afin de garder les données )
  
### USER

  - Utilisateur utilisé pour lancer le process du container
  - Par défaut root dans le container <=> root de la machine hôte
  
### ENTRYPOINT/CMD

  - Commande a executer dans le container
  - ENTRYPOINT : Binaire de l'application
  - CMD : argument
  
Un exemple de dockerfile est disponible sur le repo
