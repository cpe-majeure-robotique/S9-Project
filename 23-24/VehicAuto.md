# [Autonomous Crawler Fleet] Electronique de commande

![Crawler](img/Crawler.png)

## Objectifs

Créer l'électronique pour la flotte de véhicules autonomes. Il s'agit de créer une carte la plus compacte possible, que l'on puisse instancier à différents endroits de chaque véhicule, afin d'interfacer les différents organes (feux, clignotant, moteur direction, moteur boite de vitesse, moteur déplacement, ...) au travers d'un bus CAN-FD.


## Tâches attendues
- Proto sur carte Nucléo / Bread board (STM32G431xB)
- Design compact / Assemblage / Test du PCB
- Firmware générique
- Boîtier en impression 3D
- Développement du "Hardware Interface" ROS

## Techno
- Design de carte électronique
- Firmware C
- bus CAN-FD
- impression 3D
- ROS (hardware_interface)

```mermaid
flowchart LR

    Pwr{{"9-18V"}}
    sensors{{"sensor inputs x 2"}}
    CAN{{"CAN bus"}}
    UART{{"UART bus"}}
    SWD{{"SWD bus"}}

    servo{{"servos PWM out x 3"}}
    gpios{{"half bridge GPIOs x 4"}}

    Board["carte
            -
            -
            stm32G431xB"]


    Pwr --x Board
    UART <--> Board
    CAN <--> Board
    SWD <--> Board
    sensors --> Board

    Board--> servo
    Board--> gpios
```


