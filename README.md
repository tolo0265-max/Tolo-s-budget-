# Tolo's Budget

Application Android de gestion de budget personnelle, 100 % hors ligne, sécurisée par code PIN et biométrie.

**Couleurs inspirées du drapeau du Mali** (vert, jaune, rouge).

## Fonctionnalités

- Protection par code PIN obligatoire
- Biométrie (empreinte / Face ID) si disponible
- Enregistrement des revenus, dépenses et épargne
- Objectif d'épargne avec barre de progression
- Tableau de bord clair (solde, totaux)
- Historique complet avec modification / suppression
- Statistiques simples par catégorie
- Sauvegarde / restauration / export JSON
- Stockage local chiffré (Room + EncryptedSharedPreferences)
- Fonctionnement entièrement hors ligne

## Comment obtenir l'APK (depuis un téléphone Android uniquement)

### Méthode recommandée : GitHub Actions (gratuit)

1. Créez un compte gratuit sur [github.com](https://github.com) depuis le navigateur de votre téléphone.
2. Créez un **nouveau dépôt** (repository) public nommé par exemple `TolosBudget`.
3. Dans le dépôt, cliquez sur **Add file → Upload files**.
4. Téléchargez le fichier ZIP de ce projet (voir ci-dessous), décompressez-le sur votre téléphone, puis uploadez **tous les fichiers et dossiers** dans le dépôt GitHub.
5. Une fois les fichiers poussés, allez dans l’onglet **Actions**.
6. Le workflow « Build APK » se lance automatiquement. Attendez 2–5 minutes.
7. Cliquez sur le build terminé → **Artifacts** → téléchargez **TolosBudget-APK**.
8. Ouvrez le fichier `.apk` téléchargé et installez-le (autorisez « sources inconnues » si demandé).

### Alternative

- Demandez à un ami ayant un PC d’ouvrir le projet avec Android Studio et de générer l’APK (Build → Build Bundle(s) / APK(s) → Build APK(s)).
- Ou utilisez un service CI gratuit (Codemagic, Bitrise…) en reliant le dépôt GitHub.

## Installation de l’APK

1. Téléchargez le fichier `app-debug.apk`.
2. Ouvrez-le avec le gestionnaire de fichiers.
3. Si un message « Pour des raisons de sécurité… » apparaît, allez dans Paramètres → Autoriser cette source.
4. Installez et ouvrez **Tolo's Budget**.
5. Créez votre code PIN (4 à 6 chiffres) au premier lancement.

## Notes techniques

- minSdk 26 (Android 8.0+)
- Jetpack Compose + Material 3
- Room (base de données SQLite)
- EncryptedSharedPreferences pour le PIN
- BiometricPrompt
- Package : `com.tolos.budget`

Développé pour être réellement utilisable au quotidien.
