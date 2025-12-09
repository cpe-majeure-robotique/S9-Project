# 🧸 Peluche audio

Dans le cadre d'une sollicitation d'une association a but non lucratif, un projet (un peu en marge des projets de la majeure) est proposé en électronique pour des contenus audio. L'idée est de faire un PoC d'une peluche audio très bas coût qui puisse avoir 2 cibles :
- Les enfants dans les zones du monde sous tension (guerre, situations précaires, ...), dans une version gratuites, avec des histoires dans leur langue, qui soient encouragentes et réconfortantes.
- Les enfants occidentaux, dans une version payante, pour financer les versions envoyées gratuitement, avec des contenus de livres audio classiques


Un premier proto a été pensé avec une puce ESP32a1s, mais celle-ci est en voie d'obsolescence.
L'idée est de partir sur une puce Ai-M61-32S ou autre option à proposer.

Un partenariat pourrait être fait pour commencer avec la peluche mouton de [Kulumi](https://kulumi.org/wp-content/uploads/2023/05/KULUMI-Sheep-brochure.pdf) en remplacant leur boitier par un nouveau boitier qui répond mieux au besoin (leur modèle est cher, et ils ne veulent pas investir dans un nouveau hardware)

Il s'agit de refaire le boitier noir du player audio en étant rétro-compatible dans le mouton (par la suite d'autres peluches pourront être envisagées).
Le mouton doit donc contenir toutes les fonctionnalités et spécifications (puissance, interface utilisateur, autonomie, reprise de la lecture au démarrage, ...) du mouton initial... tout en embarquant les fonctionnalités suivantes :
- Connectivité pour transférer des contenus audio depuis une application mobile (BLE/wifi)

Le travail consiste donc à :
- Designer et tester une carte électronique répondant au besoin
- Designer un nouveau boitier (ou designer la carte de sorte à pouvoir reprendre le boitier actuel)
- Ecrire un firmware permettant de "donner vie" à la peluche
- Ecrire un PoC d'appli mobile permettant de mettre en évidence un transfer de fichier aussi simple que possible depuis nimporte quel smartphone

## 📝 Cahier des Charges

Fonctionnalités identiques... et plus...

1. Physique
   - Encombrement identique au boitier actuel. Peut être environ 3-4mm plus épais que le boitier actuel. Encombrement HP + Batteries + Carte + Boitier < 18mm*63mm*44mm 
   - Le positionnement du connecteur doit permettre l'insertion du boitier dans la peluche mouton.
   - Le boitier doit pouvoir être inséré et enlevé facilement par un utilisateur.

2. Coût
   - Le design (boitier complet hors peluche) doit être pensé pour ne pas dépasser idéalement 10$ par carte pour 1000 cartes 
   - Le cout ne doit pas être au détriment de la qualité audio qui doit être perçue comme bonne pour un publique non audiophile

3. Connectivité
   - Lorsqu'on allume la peluche (appuie long nez), la peluche cherche à se connecter à un réseau et à une appli. Après 45 secondes sans connection de la part de l'utilisateur depuis une appli, la peluche coupe le wifi/BLE
   - Du côté de l'appli, la connexion à la peluche necessite au préalable de demander à l'utilisateur d'éteindre puis rallumer la peluche.
   - Que l'utilisateur soit connecté sur une box wifi ou en données mobiles, il doit pouvoir se connecter en wifi à la peluche facilement (à la box dans le premier cas, à un point d'accès wifi du téléphone dans le second cas) sans connaissances techniques. Le BLE peut-être ou non un intermédiaire, à condition d'être facilitant.
   - Si cela peut aider à l'appairage, la peluche peut donner des indications vocales
   - La peluche doit fournir un ID unique 

## 📝 Objectifs pour le projet de majeure

Réaliser un PoC logiciel (firmware + App) avec les fonctionanalités suivantes :
- Player MP3
- Connectivité wifi/BLE tel que décrit plus haut

Réaliser une maquette informatique du matériel avec un PCB, un boitier et une intégration de ces composants qui réponde au cachier des charges


![](img/S8c97ed3c2c3a4406b142b44b1b4da4f4Z.avif)



## 🛠️ Outils et Ressources

- **Matériel** : 
  - [AiPi-Eyes](https://docs.ai-thinker.com/en/eyes/)
  - Mouton de Kulumi, carte de développement 
  
- **Logiciels** :
  - Kicad 
  - language C
  - Fusion 360

