## Exercice

Dans cet exercice, vous allez créer un Deployment et l'exposer à l'extérieur du cluster via un service de type NodePort.

### 1. Création d'un Deployment

Créez un fichier *ghost_deployment.yaml* définissant un Deployment ayant les propriétés suivantes:
- nom: *ghost*
- nombre de replicas: 3
- définition d'un selector sur le label *app: ghost*
- spécification du Pod:
  * label *app: ghost*
  * un container nommé *ghost* basé sur l'image *ghost:4* et exposant le port *2368*

Créez ensuite la ressource spécifiée.

### 2. Status du Deployment

A l'aide de *kubectl*, examinez le status du Deployment *ghost*.

- kubectl get deployment ghost

A partir de ces informations, que pouvez-vous dire par rapport au nombre de Pods gérés par ce Deployment ?

- 3 pods ont été générés

### 3. Status des Pods associés

A l'aide de *kubectl*, lister les Pods associés à ce Deployment.

- kubectl get pods -l app=ghost

### 4. Exposition des Pods du Deployment

Créez un Service permettant d'exposer les Pods du Deployment à l'extérieur du cluster