# 📰 Studiiz News Data

Bienvenue sur le dépôt de données des actualités de l'application **Studiiz** ! 🎓

Ce dépôt a un rôle central : il héberge le fichier `news.json` qui agit comme une base de données statique. L'application mobile Studiiz vient interroger (fetch) ce fichier en temps réel pour afficher les dernières annonces, mises à jour et notifications aux utilisateurs, sans nécessiter de mise à jour de l'application elle-même.

## 🛠️ Comment ça marche ?

1. Une nouvelle annonce doit être faite (ex: mise à jour, lien Instagram, message de maintenance).
2. On ajoute un nouvel objet JSON dans le fichier `news.json` de ce dépôt.
3. Les utilisateurs ouvrent l'application Studiiz.
4. L'application récupère la version brute (raw) du `news.json` et affiche l'actualité selon les paramètres définis.

## 📄 Structure du fichier `news.json`

Pour ajouter une actualité, il faut respecter la structure suivante pour chaque objet du tableau JSON :

```json
{
  "id": 1789925324574,           // Identifiant unique (recommandé : timestamp en millisecondes)
  "title": "Titre de la news",   // Le titre affiché en gras
  "content": "Texte explicatif", // Le corps du message (supporte les retours à la ligne \n)
  "date": "20/09/2026",          // Date de publication
  "importance": "Urgent",        // Niveau d'importance ("Urgent", "Normal", etc.) pour la couleur/l'icône
  "targetClasses": ["all"],      // Cibles ("all" pour tout le monde, ou ciblage spécifique)
  "hasRedirect": true,           // true si la news contient un bouton/lien cliquable
  "redirectUrl": "https://...",  // Le lien à ouvrir si hasRedirect est true
  "showOnOpen": true,            // true pour forcer l'affichage en pop-up à l'ouverture de l'app
  "maxShowCount": 1              // Nombre maximum d'affichages de la pop-up par utilisateur
}
```

## 📱 Liens Utiles Studiiz

* **Télécharger l'application :** [Google Play Store](https://play.google.com/store/apps/details?id=com.locyzz.Studiz)
* **Nous suivre sur Instagram :** [@studiizapp](https://www.instagram.com/studiizapp)
* **Développeur :** [locyzz](https://locyzz.fr/)

---
*Ce dépôt est exclusivement réservé au fonctionnement interne de l'application Studiiz.*