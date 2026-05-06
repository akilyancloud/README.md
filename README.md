📡 Communication avec un serveur Web (Ubuntu)

- Tous les fichiers cité ci-dessous sont à télécharger sont mise à dispositions mise appart les fichiers Iso ainsi que la Machine virtuelle !!


Ce projet consiste à créer un système complet permettant à un ESP32 de recevoir des commandes depuis une page web (LED, buzzer), envoyer des données vers un serveur et d'afficher ces données en temps réel


 *Étapes à suivre*

1. Installer une machine virtuelle Ubuntu

Installer un logiciel de virtualisation (VirtualBox ou VMware)
Télécharger une image ISO d’Ubuntu
Créer une machine virtuelle
Installer Ubuntu

Une fois terminé, ouvrir le terminal Ubuntu puis installer le serveur web (Apache + PHP)

**Les fichiers du site seront accessibles dans :
/var/www/html**

2. Créer un dossier pour le projet ( NOM.DU.FICHIER)
( Pour se rendre dans les fichiers var ou autre vous devez taper la commande " su - " pour passer en mode administrateur et pour continuer le projet )


3.Créer les fichiers du projet

🔹 data.php

Sert à recevoir les données envoyées par l’ESP32
Enregistre la valeur dans :
un fichier .txt → dernière valeur
un fichier .csv → historique avec date et heure

🔹 index.php

Affiche la valeur reçue
Contient des boutons pour contrôler :
une LED
un buzzer
Se met à jour automatiquement toutes les quelques secondes

Configuration de votre **ESP32**.

Remplacer :
le nom du WiFi (SSID) par le vôtre
le mot de passe WiFi par le vôtre
Remplacer également :
l’adresse IP du serveur Ubuntu
l’adresse IP de l’ESP32 dans la page web

L’ESP32 qui envoie des données au serveur et qui reçoit des commandes depuis le navigateur.

*Brancher les composants sur une breadboard.*

💡 LED

Connectée à une broche GPIO
Avec une résistance (~220Ω)

🔊 Buzzer

Connecté à une broche GPIO
Alimenté en 3.3V et GND

- Depuis la page web

L’utilisateur clique sur un bouton
Une requête HTTP est envoyée à l’ESP32
L’ESP32 exécute l’action (LED ou buzzer)

- Depuis l’ESP32

Il génère une valeur (ex : nombre aléatoire)
Il l’envoie au serveur Ubuntu

- Côté serveur

La valeur est reçue
Elle est enregistrée dans des fichiers
Elle est affichée sur la page web

**Résultat final**

- Un ESP32 connecté au WiFi
- Une page web interactive
- Un contrôle à distance (LED + buzzer)
- Un envoi automatique de données
- Un affichage en temps réel

**Important**

Avant de lancer le projet, penser à remplacer le nom du WiFi, le mot de passe, l’adresse IP de l’ESP32 ainsi que l’adresse IP du serveur Ubuntu.


