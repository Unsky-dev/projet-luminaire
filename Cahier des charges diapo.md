---
marp: true
paginate: true
header: "Projet Luminaire"
theme: default
---

# Projet Luminaire : Cahier des charges

## Objectif

- Conception d'un système d'éclairage contrôlable via une application mobile.
- Lumières variables automatiquement selon l'heure de la journée.
- Ajustement manuel de l'intensité et de la couleur (chaude ou froide).
- Utilisation de domotique (Home Assistant) et protocole Zigbee.
- Connexion via QR codes ou badges NFC.

---

## Matériel

- **Microcontrôleur** : ESP32 ou ESP8266
- **LED** : Bande LED
- **Capteurs** : Présence et lumière
- **Connectivité** : Module Zigbee
- **Interaction** : Tags NFC ou QR codes
- **Alimentation** : Adaptée au microcontrôleur et à la bande LED
- **Structure** : Support (châssis ou boîtier adaptable)
- **Appareil mobile** : Smartphone ou tablette

---

## Fonctionnalités prévues

### Contrôle manuel

- Modification de l'intensité via l'application mobile.
- Choix de la couleur et température (chaude/froide).
- Préréglages de couleurs appliquables via un "interrupteur".

### Automatisation

- Éclairage variable selon l'heure de la journée.

---

### Interaction utilisateur

- Connexion facile via QR code ou badge NFC.
- Activation de préréglages lumineux via NFC.

### Domotique et connectivité

- Intégration à Home Assistant.
- Communication Zigbee (faible consommation, fiabilité).

---

## Contraintes

- Faible consommation énergétique.
- Compatibilité avec Home Assistant et Zigbee.
- Ajustement des paramètres lumineux.
- Composants durables et adaptés.
- Interface utilisateur claire et intuitive.
- Mise en place rapide via QR code ou NFC.

---

## Informatique

### Microcontrôleur

- **WeMos D1 Pro Mini V3.0** : Prise en charge du firmware WLED.

### Firmware

- **WLED** : Open-source, contrôle précis des LED, compatibilité Home Assistant.

---

### Application

- Développement en **TypeScript** avec **React Native**.
- Multiplateforme avec une version web.
- Motivation : "Je crois en mes talents de développeur !"
