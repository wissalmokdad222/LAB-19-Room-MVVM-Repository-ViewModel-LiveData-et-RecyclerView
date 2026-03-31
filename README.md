# RoomMVVMDemo

Une application de gestion de notes simple et robuste démontrant l'utilisation de l'architecture MVVM recommandée par Android, avec une base de données locale persistante.

## Architecture du Projet

Le projet suit une organisation rigoureuse en packages pour assurer la maintenabilité et la séparation des responsabilités.

- **com.example.roommvvmdemo.data.local** : Contient l'entité Room (Note), le DAO (NoteDao) pour les requêtes SQLite, et la classe singleton NoteDatabase.
- **com.example.roommvvmdemo.data** : Contient le Repository (NoteRepository), qui sert de médiateur entre le ViewModel et les sources de données.
- **com.example.roommvvmdemo.viewmodel** : Contient le NoteViewModel, qui survit aux changements de configuration et fournit les données à l'interface utilisateur.
- **com.example.roommvvmdemo.ui** : Contient les composants de l'interface utilisateur, notamment la MainActivity et l'Adapter pour le RecyclerView.

## Composants Techniques Utilisés

- **Room Persistence Library** : Fournit une couche d'abstraction sur SQLite pour permettre une gestion fluide et sécurisée des données locales.
- **LiveData** : Utilisé pour observer les changements de données dans la base et mettre à jour l'interface utilisateur automatiquement de manière réactive.
- **ViewModel** : Permet de stocker et de gérer les données liées à l'interface de manière consciente du cycle de vie des activités.
- **RecyclerView & CardView** : Utilisés pour afficher une liste performante et moderne des notes enregistrées.

## Fonctionnalités Principales

- Ajout de notes avec un titre et une description.
- Suppression individuelle d'une note via un clic long sur l'élément.
- Suppression globale de toutes les notes enregistrées.
- Persistance des données : les notes restent enregistrées même après la fermeture et la réouverture de l'application.
- Résistance aux changements de configuration (comme la rotation de l'écran) grâce au ViewModel.

## Prérequis de Compilation

- Android Studio Flamingo ou version ultérieure.
- Java 11 ou version ultérieure.
- SDK Android Minimum : API 24 (Android 7.0).
- Dépendances principales incluses : Room 2.8.4 et Lifecycle 2.9.3.

## Instructions de Test

1. Lancer l'application sur un émulateur ou un appareil physique.
2. Saisir un titre et une description, puis cliquer sur Ajouter une Note.
3. Vérifier que la note apparaît immédiatement dans la liste.
4. Effectuer un clic long sur une note pour la supprimer.
5. Utiliser le bouton de suppression globale pour vider la liste.
6. Tourner l'écran pour vérifier que l'état de la liste est préservé.
