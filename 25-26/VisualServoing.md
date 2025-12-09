# Préhension d'Objets avec le bras xArm7 : Du Visual Servoing Classique aux Modèles de Fondation Robotique

## 🎯 Objectif du Projet

Ce projet explore deux approches complémentaires pour la préhension d'objets avec le bras robotique xArm7 :

1. **Visual Servoing Classique** : Mise en œuvre d'une approche traditionnelle de commande asservie par vision pour établir une base de référence
2. **Modèle de Fondation avec LeRobot** : Utilisation d'un modèle pré-entraîné via la plateforme LeRobot de Hugging Face pour généraliser les compétences de manipulation

L'objectif est de comparer ces deux paradigmes et d'affiner les performances du modèle de fondation sur des objets spécifiques.  

Chaque expérimentation se fera **d'abord en simulation**, avant de se faire en réel

---

## 📝 Cahier des Charges et Tâches Principales

### **Partie 1 : Visual Servoing Classique (Base de Référence)**

#### 1.1 Étude Théorique
- Comprendre les principes du visual servoing (IBVS - Image-Based VS ou PBVS - Position-Based VS)
- Étudier la cinématique du xArm7 
- Définir une stratégie de préhension basée sur la détection de primitives visuelles (points, contours, marqueurs ArUco, etc.)

#### 1.2 Implémentation
- Créer l'environnement de travail et faire un Hello World de déplacement du bras en simulation (gazebo), puis en réel. 
- Mettre en place la boucle de commande asservie : acquisition d'image → extraction de caractéristiques → calcul de l'erreur → commande articulaire
- Implémenter la détection et la localisation d'objets (vision par ordinateur classique : OpenCV, détection de contours, segmentation)
- Réaliser des tâches de pick-and-place simples avec contrôle de la position et de l'orientation

#### 1.3 Évaluation
- Mesurer le taux de succès de préhension sur un ensemble d'objets de test
- Analyser les limites : sensibilité aux variations d'éclairage, robustesse face à l'occlusion, généralisation à de nouveaux objets

---

### **Partie 2 : Modèle de Fondation avec LeRobot**

#### 2.1 Recherche et Sélection du Modèle
- Explorer la plateforme **LeRobot** (https://github.com/huggingface/lerobot) développée par Hugging Face
- Étudier les modèles de fondation/VLA disponibles (ex: ACT, Diffusion Policy, VQ-BeT, OpenVLA via LeRobot)
- Sélectionner un modèle adapté à la préhension et compatible avec l'architecture du xArm7

#### 2.2 Intégration et Déploiement
- Installer l'environnement LeRobot et ses dépendances
- Configurer l'interface entre LeRobot et l'API Python du xArm7
- Adapter le pipeline de perception (caméra) pour correspondre au format d'entrée du modèle
- Générer des commandes d'action (trajectoires articulaires, commande du préhenseur) à partir des observations visuelles

#### 2.3 Collecte de Données avec LeRobot
- Identifier une classe d'objets "difficiles" ou spécifiques à l'environnement du laboratoire
- Utiliser les outils de télé-opération de LeRobot pour collecter des démonstrations
- Constituer un dataset au format LeRobot (observations + actions) pour le fine-tuning
- Documenter le protocole de collecte et les métadonnées des épisodes

#### 2.4 Affinement (Fine-Tuning)
- Configurer l'entraînement du modèle sur le dataset collecté
- Ajuster les hyperparamètres (learning rate, batch size, nombre d'époques)
- Affiner le modèle de fondation pour améliorer le taux de succès sur les objets ciblés


---

## 🛠️ Outils et Ressources

- **Matériel** : 
  - Bras robotique xArm7
  - caméra RGB(-D)
  - objets de test ([dataset YCB](https://www.ycbbenchmarks.com/object-models/))
- **Logiciels** : 
  - Python, OpenCV (pour visual servoing classique)
  - LeRobot (Hugging Face) pour les modèles de fondation
  - API xArm Python SDK
  - ROS2 (optionnel, selon l'architecture)

