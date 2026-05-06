📡 Communication avec un serveur Web (Ubuntu)

Ce projet consiste à créer un système complet permettant à un ESP32 de :

recevoir des commandes depuis une page web (LED, buzzer)
envoyer des données vers un serveur
afficher ces données en temps réel

🧭 Étapes à suivre

🖥️ 1. Installer une machine virtuelle Ubuntu

Installer un logiciel de virtualisation (VirtualBox ou VMware)
Télécharger une image ISO d’Ubuntu
Créer une machine virtuelle
Installer Ubuntu

➡️ Une fois terminé, ouvrir le terminal Ubuntu

🌐 2. Installer le serveur web (Apache + PHP)

Installer Apache (serveur web)
Installer PHP (traitement des données)

📁 Les fichiers du site seront accessibles dans :
/var/www/html

Créer un dossier pour le projet (ex : btsciel)

📁 3. Créer les fichiers du projet

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

📶 4. Configurer l’ESP32

Remplacer :
le nom du WiFi (SSID) par le vôtre
le mot de passe WiFi par le vôtre
Remplacer également :
l’adresse IP du serveur Ubuntu
l’adresse IP de l’ESP32 dans la page web

➡️ L’ESP32 :

envoie des données au serveur
reçoit des commandes depuis le navigateur

🔌 5. Brancher les composants

💡 LED

Connectée à une broche GPIO
Avec une résistance (~220Ω)

🔊 Buzzer

Connecté à une broche GPIO
Alimenté en 3.3V et GND

➡️ Ces composants permettent de tester les commandes

🔄 6. Comprendre le fonctionnement

👉 Depuis la page web

L’utilisateur clique sur un bouton
Une requête HTTP est envoyée à l’ESP32
L’ESP32 exécute l’action (LED ou buzzer)

👉 Depuis l’ESP32

Il génère une valeur (ex : nombre aléatoire)
Il l’envoie au serveur Ubuntu

👉 Côté serveur

La valeur est reçue
Elle est enregistrée dans des fichiers
Elle est affichée sur la page web

🚀 Résultat final

À la fin du projet, tu obtiens :

✅ Un ESP32 connecté au WiFi
✅ Une page web interactive
✅ Un contrôle à distance (LED + buzzer)
✅ Un envoi automatique de données
✅ Un affichage en temps réel

⚠️ Important

Avant de lancer le projet, penser à :

remplacer le nom du WiFi
remplacer le mot de passe
remplacer l’adresse IP de l’ESP32
remplacer l’adresse IP du serveur Ubuntu

🧠 Compétences acquises

Ce projet permet de comprendre :

la communication réseau entre appareils
le fonctionnement des requêtes HTTP (GET / POST)
l’interaction entre matériel (ESP32) et page web
le stockage et affichage de données dynamiques
