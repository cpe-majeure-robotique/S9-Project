# 🚗 Navigation MPPI pour Véhicule Autonome de Type Crawler

![Crawler](img/Crawler.png)

---

## 🎯 Objectifs

Continuer le développement du véhicule autonome de type "Crawler" en intégrant des fonctionnalités avancées de navigation et de perception.

---

## 📋 Tâches Attendues

### **1. Côté Jetson / ROS2**

#### Tâches Principales

- Installer Jetson en Ubuntu 24.04 avec ROS2 Jazzy
- Faire rouler le Crawler dans Gazebo Harmonic avec Nav2 (peut être fait sur PC école)
- Prendre en compte la caméra 3D dans Nav2 (peut être fait sur PC école)
- Utiliser le local planner MPPI dans Nav2 (peut être fait sur PC école)
- Communiquer en bus CAN avec la carte moteur (peut être fait sur PC école)
- Écrire le driver ros2_control de la partie motorisation/direction du véhicule (peut être fait sur PC école)

#### Tâches Optionnelles

- Intégrer l'IMU dans Nav2

---

### **2. Côté Embarqué**

#### Tâches Principales

- Finaliser le firmware du pare-chocs arrière
- Écrire le firmware de la carte moteur

#### Tâches Optionnelles

- Intégrer la carte radar
- Finaliser et intégrer la carte IO pour les lumières
- Finaliser et intégrer la carte BMS pour la gestion des batteries à chaud

---

## 🛠️ Technologies Utilisées

### Matériel

- **Jetson Xavier Orin** : Plateforme de calcul embarquée
- **STM32** : Microcontrôleurs pour les fonctions embarquées
- **Bus CAN** : Communication entre les cartes électroniques

### Logiciels

- **ROS2 Jazzy** : Framework robotique
- **Nav2** : Stack de navigation autonome
- **Gazebo Harmonic** : Simulateur robotique
- **Python, C, C++** : Langages de programmation

---

