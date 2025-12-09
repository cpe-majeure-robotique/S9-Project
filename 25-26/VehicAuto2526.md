# Navigation MPPI Véhicule autonome

![Crawler](img/Crawler.png)

## Objectifs

Continuez le développement du véhicule autonome de type "Crawler"


## Tâches attendues

**1. Côté Jetson / ROS : **
- Installer Jetson en Ubuntu 24.04 avec ROS2 Jazzy
- Faire rouler le Crawler dans Gazebo Harmonic avec Nav2 (peut-être fait sur PC école)
- Prendre en compte la caméra 3D dans Nav2 (peut-être fait sur PC école)
- Utilisez le local planner MPPI dans Nav2 (peut-être fait sur PC école)
- Communiquer en bus CAN avec la carte moteur (peut-être fait sur PC école)
- Ecrire driver ros2_control de la partie motorisation / direction du véhicule (peut-être fait sur PC école)
- [Optionnel] Intégrer IMU dans Nav2


**2. Côté embarqué : **
- Finaliser firmware du pare-chocs arrière
- Ecrire firmware de la carte moteur
- [Optionnel] Intégrer carte radar
- [Optionnel] Finaliser et intégrer carte IO pour lumières
- [Optionnel] Finaliser et intégrer carte BMS pour gestion batteries à chaud



## Techno

- Jetson Xavier Orin
- ROS2 (Nav2, Gazebo, ...)
- Python, C, C++
- STM32 et Bus CAN




