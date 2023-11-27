# Robot Decision Maker avec LLM pour robot domestique

![ontho](img/ontho.webp)

## Objectifs

Faire un PoC d'un Manager de scénario pour la robocup (épreuve GPSR[^1] ) basé sur un LLM. L'entrée sera un texte, la sortie est une suite d'actions élémentaires correspondant aux capacités du robot.

Des tests automatisés seront effectués avec pour données d'entrées des consignes issues de [ce générateur de commandes pour robots](https://github.com/kyordhel/GPSRCmdGen).

En sortie, il y aura une liste d'actions à afficher. Ces actions seront données selon les capacitées intrinsèque du robots. On pourra donc faire des tests automatiques pour différent robots avec différentes consignes.

[^1]: GPSR : General Purpose Service Robot --> Similar to a smart speaker, the robot is asked to execute arbitrary commands requested by an operator

Exemples de subdivision des tâches pour "Go to the kitchen and bring a banana" : 

- Identify "User" and "Command"
- Record Current "Location"
- Analyze Environment for Navigation
- Navigate to Semantic Location "Kitchen"
- Search for "Banana"
- Navigate to the Closest Reachable Position Near "Banana"
- Refine "Banana" Position
- Grasp "Banana" with Adaptive Gripper
- Verify Successful Grasp
- Return to "Original Location" with "Banana"
- Deliver "Banana" to "User"

On pourrait definir (ou pas) un fichier d'onthologie tel que celui-ci :

```yaml
Ontology:
  name: GenericServiceRobotOntology

Entities:
  - Robot
  - User
  - Location
  - Object
  - Task

Attributes:
  Robot:
    - CurrentLocation
    - TaskList
  User:
    - UserID
    - Location
  Location:
    - Name
    - Type
  Object:
    - ObjectType
    - Location
  Task:
    - Description
    - Status

Relations:
  - RobotAssignedToTask:
      from: Robot
      to: Task
  - ObjectLocatedIn:
      from: Object
      to: Location
  - UserInLocation:
      from: User
      to: Location

Tasks:
  - GenericTaskExample:
      Steps:
        - IdentifyUser
        - RecordCurrentLocation
        - AnalyzeEnvironment
        - NavigateToLocation
        - SearchForObject
        - NavigateToObject
        - GraspObject
        - VerifyGrasp
        - ReturnToUser
        - DeliverObject

```


Si le model peut fonctionner en local c'est un vrai plus.

:memo: Si votre travail est réutilisé pour une publication, votre nom y sera associé.

## Tecnhologies
- LLMs
- Dev moteur d'onthologie
- ROS2
- Recherche


## Ressources

### Articles 

- [Introspective Tips: Large Language Model for
In-Context Decision Making](https://arxiv.org/pdf/2305.11598.pdf)

- [Integrating ontologies with LLMs](https://ai.plainenglish.io/integrating-ontologies-with-large-language-models-for-decision-making-bb1c600ce5a3)

- [Decision makers exemples](https://medium.com/@kamaljp/meet-langchains-cutting-edge-agents-4-revolutionary-ai-llm-powered-decision-makers-8677045e8a69)

### Exemple de framework

- [ROS-LLM](https://github.com/Auromix/ROS-LLM)