# Services IA Cloud pour Robots et/ou Zoo
![Yolo](https://raw.githubusercontent.com/cpe-majeure-robotique/S9-Project-19-20/master/images/yolo_darknet.png)

## Objectifs
Développer un service de reconnaissance d'objets ou d’interprétations associées à de l'IA


## Résultats attendus
### Socle commun obligatoire :
- Un réseau de neurone dont vous avez fait l'apprentissage avec votre propre dataset (ou dataset existant augmenté par vous )
- Un serveur web (Flask) pour bénéficier du service sur une page web et depuis des Endpoints
- Une API python pour accéder aux endpoints du service
- Un exemple d'implémentation de l'API dans un noeud ROS
- Un exemple d'implémentation de l'API dans une App Naoqi
- Une version IPYNB (fichier Jupiter Notebook pour google Colab par ex) pour déployer la partie Serveur
- Une version IPYNB (fichier Jupiter Notebook pour google Colab par ex) pour déployer la partie Client (Exemples d'accès au service)

### Une option obligatoire au choix : 
- Service permettant de dénombrer une espèce animale et de donner des indications sur son comportement (immobile, agité, en groupe, isolés, ou autre critères à définir en fonction de l'espèce)
- Service permettant renseigner la composition de son frigo (Lait, Beurre, ...)
- Proposition libre à valider par le prof

### Optionnel mais recommandé :
- Un Dockerfile (et docker-compose en option) pour lancer votre serveur sur n'importe quelle machine 
- Intégration continue sur GitLab permettant que valider le fonctionnement des codes


## Technologies
* Python, Webservices, Flask
* Yolo/Darknet
* Mise en place d'un Dataset et Apprentissage
* Google Colab
* Docker
* ROS/Naoqi


## Aide
* [Exemple d'un serveur **Flask** sur Google Colab] (https://medium.com/@kshitijvijay271199/flask-on-google-colab-f6525986797b)
* [Excellent tuto sur Docker (suivre les 3 vidéos)](https://www.youtube.com/watch?v=SXB6KJ4u5vg)

