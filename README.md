# ContactsListView — Application Android Kotlin

Une application Android simple et intuitive développée en **Kotlin** qui illustre l'utilisation d'une **ListView**, d'un **ArrayAdapter** et la modification dynamique de données en temps réel.

---

## 📱 Fonctionnalités

1. **Affichage de la liste de contacts** :
   - Affiche une liste initiale de contacts dans un composant `ListView`.
   - Utilise un `ArrayAdapter` configuré avec le layout système `simple_list_item_activated_1` pour la mise en surbrillance de l'élément sélectionné.

2. **Sélection d'un contact** :
   - Un clic sur un contact remplit automatiquement le champ de texte `EditText` avec son nom.
   - Le curseur se positionne automatiquement à la fin du texte pour faciliter l'édition.

3. **Modification d'un contact** :
   - Clic sur le bouton **Modifier** ou validation via la touche "Terminé" du clavier virtuel (`IME_ACTION_DONE`).
   - Mise à jour instantanée de l'affichage dans la `ListView` grâce à la méthode `adapter.notifyDataSetChanged()`.

4. **Contrôles et validations** :
   - Vérifie qu'un contact a été préalablement sélectionné (affichage d'un message `Toast` le cas échéant).
   - Bloque la modification si le champ de texte est vide avec un message d'erreur d'avertissement.

---

## 🛠️ Notions Android abordées

* **`ListView`** : Composant graphique d'affichage défilant d'une liste d'éléments.
* **`ArrayAdapter`** : Liaison entre les données Kotlin (`MutableList<String>`) et la vue (`ListView`).
* **`mutableListOf`** : Liste modifiable en mémoire.
* **`setOnItemClickListener`** : Détection et traitement du clic sur un élément de la liste.
* **`notifyDataSetChanged()`** : Notification de l'adaptateur pour rafraîchir la vue après modification de la liste source.

---

## 📁 Structure du projet

```
ContactsListView/
├── app/
│   └── src/main/
│       ├── java/com/example/contactslistview/
│       │   └── MainActivity.kt       # Logique applicative et gestion des événements
│       ├── res/
│       │   ├── layout/
│       │   │   └── activity_main.xml # Layout XML en LinearLayout
│       │   └── values/
│       │       └── strings.xml       # Textes de l'application
│       └── AndroidManifest.xml
├── build.gradle.kts
└── settings.gradle.kts
```

---

## 🚀 Prérequis et Lancement

1. **Prérequis** :
   - Android Studio (version récente)
   - Android SDK (API 24 minimum, Android 7.0+)
   - JDK 17

2. **Lancement** :
   - Cloner le projet :
     ```bash
     git clone https://github.com/<votre-username>/ContactsListView.git
     ```
   - Ouvrir le projet dans **Android Studio**.
   - Lancer l'application sur un émulateur ou un appareil Android physique (`Run` / `Shift+F10`).
