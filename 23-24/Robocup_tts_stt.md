# \[Robocup\] Brique conversationnelle

![trappe](img/convers_2.png)

## Objectifs

Développer une brique ROS2 de conversation en langage naturel : Un paquet pour le STT[^1], un paquet pour le TTS[^2], un paquet pour le NLP[^3] dans le cas du GPSR[^4]. 
  
[^1]: STT : Speech To Text  
[^2]: TTS : Text To Speech  
[^3]: NLP : Natural Language Processing  
[^4]: GPSR : Global Purpose Service Robot (Épreuve de robot de service générique à la Robocup)



## Tâches attendues
- Intégration d'un STT[^1] à partir d'un flux audio de microphone en fenêtre glissante. 
    - Requêter avec des actions. Exemple "sale" mais fonctionnel [ici](https://github.com/m0rph03nix/stt_nlu_ros), avec messages documentés.
    - Noeud avec entrée permettant de mute le micro (allumé par défaut). Exemple [ici](https://github.com/m0rph03nix/mic_manager)
- Intégration d'un TTS[^2]  
- Intégration d'un NLP[^3] 



## Contraintes
- Un petit état de l'art des technos doit être documenté
- Les fichiers d'algo sont à séparer des fichiers de noeud ROS.



## Technologies
- ROS2
- python
- LLM