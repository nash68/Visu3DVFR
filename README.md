# Visu3DVFR

Une application web interactive et légère permettant de rejouer et d'analyser des traces de vol VFR (Visual Flight Rules), conçue spécifiquement pour l'aviation générale . L'application s'exécute entièrement côté client dans le navigateur.

## 🚀 Fonctionnalités Clés

- **Carte Interactive 2D / 3D** : Intègre **MapLibre GL** pour afficher le tracé du vol. Basculez facilement entre une vue plate (2D) et une vue en perspective inclinée (3D) avec suivi en temps réel de la position de l'avion.
 ** Affichage du tracer à parcourir en rose clair. Affichage du tracé parcouru en rose foncé. Le trait doit tenir compte du relief. Des boutons permettent de choisir quel tracé on affiche ou non.
- **Instruments de Bord Réalistes** : Rendus dynamiquement à l'aide de l'API Canvas HTML5 :
  - **Indicateur de Vitesse (Badin)** : Calibré pour afficher la vitesse sol (GS) en nœuds.
  - **Conservateur de Cap (Gyro directionnel)** : Affiche le cap suivi par l'aéronef en degrés.
  - **Profil de Coupe Terrain** : Graphique en temps réel montrant le profil altimétrique (altitude de l'avion et relief du sol) sur une fenêtre glissante de 5 milles nautiques (NM).
- **Console de Télémétrie Complète** :
  - Altitude de l'avion (AMSL - *Above Mean Sea Level*) en pieds et mètres.
  - Hauteur par rapport au sol (AGL) avec alertes visuelles.
  - Altitude du sol (élévation du relief).
  - Indication de la marge de sécurité des 500 pieds (hauteur minimale réglementaire de survol).
  - Vitesse Sol (GS) et Cap exact.
- **Lecteur de Replay Style "YouTube"** : Contrôles de lecture fluides (Play/Pause), barre de progression interactive cliquable et curseur réglable pour la vitesse de lecture (1x, 2x, 4x, 8x, 16x).
- **Importation GPX** : Possibilité de charger vos propres fichiers GPX (`.gpx`, `.xml`) enregistrés en vol réel pour les rejouer instantanément dans l'interface.

## 📂 Structure du Projet

Le projet est entièrement autonome et structuré dans un fichier unique pour faciliter sa portabilité :

- **[index.html] ** : Contient la structure HTML5, les feuilles de style CSS (thème sombre premium), les données de vol préchargées pour le Cessna 152, et toute la logique JavaScript (moteur de rendu des instruments, traitement GPX, et gestion de la carte MapLibre).

## 🛠️ Technologies Utilisées

- **HTML5 / CSS3 / JavaScript (Vanilla)**
- **MapLibre GL JS** (chargé via CDN) pour le rendu cartographique WebGL.
- **HTML5 Canvas** pour le dessin vectoriel fluide des instruments aéronautiques.
- Autres si nécessaire selon les évolutions demandées

## 📖 Comment Utiliser l'Application

1. Ouvrez simplement le fichier `index.html` dans le navigateur web de votre choix (Chrome, Firefox, Edge, Safari...).
2. Utilisez le panneau inférieur pour démarrer, mettre en pause ou accélérer le replay.
3. Pour tester avec vos propres données de vol, cliquez sur le bouton de chargement de fichier (icône document avec flèche vers le haut) et sélectionnez un fichier GPX.
