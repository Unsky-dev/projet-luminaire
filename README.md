# Projet Luminaire : Cahier des charges

## 1. Objectif

Notre projet consiste à concevoir un système d’éclairage contrôlable via une application mobile. Les lumières pourront varier automatiquement selon l’heure de la journée, et l’utilisateur pourra ajuster l’intensité ou la couleur des luminaires (plus ou moins chaud ou froid).

Le luminaire utilisera une application de domotique telle que Home Assistant et communiquera avec le protocole Zigbee. Nous prévoyons également d’intégrer des QR codes ou des badges NFC permettant une connexion directe au réseau local et l’accès au panneau de contrôle.

## 2. Matériel

- Microcontrôleur (ESP32 ou ESP8266)
- Bande LED
- Capteur de présence
- Capteur de lumière
- Module Zigbee
- Tags NFC ou QR codes
- Alimentation (adaptée au microcontrôleur et à la bande LED)
- Support pour le luminaire (châssis ou boîtier adaptable)
- Smartphone ou tablette pour le contrôle via l’application mobile

## 3. Fonctionnalités prévues

### 1. Contrôle manuel

- Modification de l’intensité lumineuse via l’application mobile.
- Choix de la couleur et de la température de la lumière (chaude ou froide).
- Création de préréglages de couleur appliquables via un « interrupteur ».

### 2. Automatisation

- Variation automatique de l’éclairage en fonction de l’heure de la journée (nécessite un capteur compatible avec Home Assistant).

### 3. Interaction avec l’utilisateur

- Connexion facile grâce à un QR code ou un badge NFC pour accéder au panneau de contrôle.
- Activation des préréglages lumineux prédéfinis via l’approche d’un smartphone sur un tag NFC configuré.

### 4. Domotique et connectivité

- Intégration au système Home Assistant.
- Communication via le protocole Zigbee pour une faible consommation énergétique et une connexion fiable.

## 4. Contraintes

- Assurer une faible consommation d’énergie.
- Garantir la compatibilité avec Home Assistant et le protocole Zigbee.
- Permettre l’ajustement des paramètres lumineux.
- Utiliser des composants durables et adaptés.
- Proposer une interface utilisateur claire et intuitive pour l’application mobile.
- Assurer une mise en place rapide du panneau de contrôle via QR code ou badge NFC, en respectant les contraintes techniques et d’accessibilité du projet.

## 5. Informatique

### 1. Microcontrôleur

Le microcontrôleur prévu est le WeMos D1 Pro Mini V3.0. Celui-ci permet l’installation du firmware WLED.

### 2. Firmware

Nous allons utiliser le firmware WLED (car pourquoi réinventer la roue ?). WLED est un firmware open-source qui permet de contrôler précisément les LED et d’assurer une compatibilité avec Home Assistant.

### 3. Application

L’application sera développée en TypeScript avec la librairie React Native, ce qui permettra de la rendre multiplateforme et même d’avoir une version web. Bien que je ne connais ni le langage, ni le framework, j’ai des bases en JavaScript et je crois en mes talents de développeur.


## 6. Construction détails

### 1. Alimentation

Pour alimenter ce type de micro-contrôleur, il y a deux moyen. Soit par son port USB, soit par sa broche 5V. C'est ceci que nous allons utilisé afin de pouvoir alimenter et le processeur et la bande led en même temps sans devoir rajouter un module. Donc nous devons connecter un cable a un bloc chargeur.

### 2. Connexion entre la bande led et le micro-contrôleur

La seul connexion qu'il y a entre ces deux appareils est le data. Celui ci est branché sur le pin D1.