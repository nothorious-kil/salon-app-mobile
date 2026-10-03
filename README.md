# salon-app-mobile

Application mobile React Native Expo pour la gestion du salon, conçue pour Android et iOS.

## Stack
- React Native + TypeScript strict
- Expo SDK 51
- React Navigation
- Redux Toolkit + React Redux
- Axios
- expo-sqlite
- expo-secure-store
- expo-image-picker / expo-image-manipulator

## Prérequis
- Node 18+
- npm ou yarn
- Expo Go ou simulateur Xcode/Android Studio
- Backend exposé sur le réseau local ou une URL distante

## Configuration
Copier `.env.example` vers `.env` et renseigner l’URL du backend sans `/api` :

EXPO_PUBLIC_API_URL=http://192.168.1.25:3000

Le client ajoute automatiquement `/api` à cette base. Sur téléphone physique, utilise l’adresse IP du PC / serveur sur le réseau local. `localhost` ne pointe pas vers le PC.

## Lancement
1. npm install
2. npm start
3. scanne le QR code avec Expo Go ou choisis le simulateur

## Scripts
- npm run start
- npm run android
- npm run ios
- npm run typecheck
- npm run lint
- npx expo-doctor

## Fonctionnalités de base
- Authentification login/register
- Vue d’ensemble et rapports
- Clients, rendez-vous, catalogue, caisse, équipe
- Présences par date
- Paramètres avec thème et déconnexion
- Cache SQLite et file d’attente d’actions offline
- Gestion des photos et validation de fichiers

## Limites offline
- Les données peuvent être lues depuis le cache SQLite lorsque le réseau est absent.
- Les mutations non synchronisées restent visibles comme « en attente » et ne sont pas présentées comme confirmées par le serveur.
- La synchronisation explicite doit être déclenchée après restauration du réseau.
