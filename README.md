# HomeLink Premium - Immobilier Côte d'Ivoire

## Description du Projet
HomeLink Premium est une Progressive Web App (PWA) conçue pour simplifier et sécuriser le marché immobilier en Côte d'Ivoire. Elle met en relation propriétaires et locataires, offrant une plateforme fiable pour la publication et la recherche d'annonces immobilières. L'application intègre des fonctionnalités modernes, une interface utilisateur intuitive inspirée d'iOS, et un système de gestion robuste pour assurer la confiance et la transparence des transactions.

## Fonctionnalités
- **Publication d'Annonces** : Les propriétaires peuvent publier facilement des annonces détaillées avec photos.
- **Recherche et Filtrage** : Les locataires peuvent rechercher des biens par commune, type et mots-clés.
- **Authentification Sécurisée** : Connexion via Google pour une expérience utilisateur fluide et sécurisée.
- **Système de Messagerie** : Communication directe et sécurisée entre utilisateurs.
- **Signalement d'Annonces** : Mécanisme intégré pour signaler les annonces suspectes et lutter contre les arnaques.
- **Monétisation** : Packs d'annonces payants pour les professionnels, avec intégration du paiement mobile Wave.
- **Panneau d'Administration** : Interface dédiée pour la gestion des paiements, la modération des annonces et le suivi.
- **Exportation de Données (Nouveau)** : Fonctionnalité permettant aux administrateurs d'exporter les données des annonces au format CSV pour analyse.

## Technologies Utilisées
- **Frontend** : HTML5, CSS3, JavaScript (Vanilla JS)
- **Base de Données & Backend** : Google Firebase (Firestore pour la base de données, Authentication pour l'authentification, Storage pour le stockage des images)
- **PWA** : Manifest Web App pour une expérience utilisateur installable et hors ligne.
- **Icônes** : Font Awesome

## Installation et Lancement Local
Pour lancer l'application en local, suivez les étapes ci-dessous :

1.  **Cloner le dépôt GitHub** :
    ```bash
    git clone [URL_DE_VOTRE_DEPOT]
    cd homelink-premium
    ```

2.  **Configuration Firebase** :
    HomeLink Premium utilise Firebase pour la base de données, l'authentification et le stockage. Vous devez créer un projet Firebase et y ajouter votre configuration.
    -   Allez sur la [console Firebase](https://console.firebase.google.com/).
    -   Créez un nouveau projet.
    -   Ajoutez une application web à votre projet et copiez votre `firebaseConfig`.
    -   Ouvrez le fichier `index.html` et remplacez le placeholder `YOUR_FIREBASE_CONFIG_HERE` par votre configuration Firebase. La section à modifier se trouve généralement au début du script JavaScript, vers la ligne 831 :
        ```javascript
        const firebaseConfig = {
            apiKey: "YOUR_API_KEY",
            authDomain: "YOUR_AUTH_DOMAIN",
            projectId: "YOUR_PROJECT_ID",
            storageBucket: "YOUR_STORAGE_BUCKET",
            messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
            appId: "YOUR_APP_ID"
        };
        ```
    -   **Activer Firestore** : Dans la console Firebase, allez dans `Firestore Database` et créez une base de données en mode production ou test.
    -   **Activer l'Authentification Google** : Dans la console Firebase, allez dans `Authentication`, puis `Sign-in method` et activez `Google`.
    -   **Activer Cloud Storage** : Dans la console Firebase, allez dans `Storage` et configurez les règles de sécurité si nécessaire.

3.  **Lancer l'application** :
    Étant donné que c'est une application web statique, vous pouvez l'ouvrir directement dans votre navigateur en double-cliquant sur `index.html`. Cependant, pour une meilleure expérience de développement (notamment pour les PWA et les requêtes HTTP), il est recommandé d'utiliser un serveur web local. Vous pouvez utiliser `http-server` (Node.js) ou un serveur Python simple :

    -   **Avec `http-server` (Node.js)** :
        ```bash
        npm install -g http-server
        http-server .
        ```
        Ensuite, ouvrez `http://localhost:8080` (ou le port indiqué) dans votre navigateur.

    -   **Avec Python** :
        ```bash
        python3 -m http.server
        ```
        Ensuite, ouvrez `http://localhost:8000` dans votre navigateur.

## Déploiement sur GitHub Pages
1.  Assurez-vous que votre dépôt contient les fichiers `index.html` et `manifest.json` à la racine.
2.  Dans les paramètres de votre dépôt GitHub, allez dans la section `Pages`.
3.  Sélectionnez la branche `main` (ou `master`) et le dossier `/ (root)` comme source de déploiement.
4.  Enregistrez les modifications. Votre application sera déployée à l'adresse `https://[appci6648].github.io/[HomLink-premium]/`.

## Structure du Projet
```
.github/
├── workflows/
│   └── deploy.yml  (Exemple de workflow pour GitHub Pages)
├── index.html      (Page principale de l'application)
├── manifest.json   (Manifest de la Progressive Web App)
└── README.md       (Ce fichier)
```

## Contribution
Les contributions sont les bienvenues ! Si vous souhaitez améliorer ce projet, n'hésitez pas à ouvrir une issue ou à soumettre une pull request.

## Licence
Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.
