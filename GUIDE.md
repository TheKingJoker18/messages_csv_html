# Guide d'utilisation - Messages CSV → HTML

Ce guide vous explique pas à pas comment utiliser l'application `messages_csv_html.html` pour transformer votre export de messages en une conversation propre et exportable.

## 1. Prérequis

- Un navigateur web moderne (Firefox, Chrome, Edge, Opera, etc.)
- Un fichier CSV au format `Date;Time;Sender;Message` (séparateur point-virgule)
- Connexion internet uniquement si vous souhaitez utiliser les exports PNG ou PDF (html2canvas/jsPDF via CDN)

## 2. Ouvrir l'application

1. Ouvrez le fichier `messages_csv_html.html` directement dans votre navigateur (double-clic ou glisser-déposer dans une fenêtre de navigateur).
2. L'application se charge localement, aucun fichier n'est envoyé sur internet.

## 3. Charger votre fichier CSV

### Méthode 1 : Glisser-déposer

1. Ouvrez votre explorateur de fichiers
2. Glissez votre fichier `.CSV` sur la zone "Déposez votre fichier CSV"
3. Relâchez le fichier

### Méthode 2 : Sélection manuelle

1. Cliquez sur le bouton "Sélectionner un fichier"
2. Parcourez vos fichiers et sélectionnez votre CSV
3. Validez

**Remarque** : Si Firefox essaie d'ouvrir le fichier au lieu de le charger, utilisez plutôt le bouton "Sélectionner un fichier".

## 4. Visualiser la conversation

Une fois le fichier chargé :

- La conversation s'affiche sous forme de bulles de discussion
- Les messages sont regroupés par expéditeur
- Un séparateur s'affiche à chaque changement de date
- Les sauts de ligne et emojis sont conservés
- Vous pouvez faire défiler la conversation

## 5. Changer le thème de l'application

En haut de la page, utilisez le sélecteur "Thème" :

- **Clair** : Thème clair
- **Sombre** : Thème sombre

Le thème choisi est sauvegardé dans votre navigateur. Par défaut, l'application suit le thème de votre navigateur (clair/sombre) s'il n'y a aucune préférence enregistrée, sinon clair.

## 6. Exporter la conversation

Après le chargement, trois boutons d'export apparaissent :

### Télécharger HTML

- Bouton "Télécharger HTML"
- Génère un fichier HTML autonome, en **mode clair**
- Peut être ouvert hors ligne sans l'application
- Comprend le pied de page avec copyright et lien GitHub
- Idéal pour partager ou archiver

### Exporter en PNG

- Bouton "Exporter en PNG"
- Capture **l'intégralité** de la conversation (en-tête, messages, séparateurs, pied de page)
- Image haute résolution (scale 2)
- Thème appliqué selon votre sélection "Thème d'export" (Sombre/Clair) sous les boutons d'export
- Nécessite une connexion internet pour charger html2canvas

### Exporter en PDF

- Bouton "Exporter en PDF"
- Génère un PDF multipages de **l'intégralité** de la conversation
- Mise en page A4 avec pagination automatique
- Thème appliqué selon votre sélection "Thème d'export" (Sombre/Clair)
- Nécessite une connexion internet pour charger html2canvas et jsPDF

## 7. Vérifier l'état des dépendances

En bas de la zone de conversation, vous voyez deux indicateurs :

- **html2canvas** : Vert si disponible, Orange si en attente, Rouge si indisponible
- **jsPDF** : Vert si disponible, Orange si en attente, Rouge si indisponible

Si vous êtes hors ligne, seul "Télécharger HTML" fonctionnera.

## 8. Dépannage

| Problème | Solution |
| ---------- | ---------- |
| Firefox ouvre le CSV au lieu de le charger | Utilisez le bouton "Sélectionner un fichier" au lieu du glisser-déposer |
| "Aucun message trouvé" | Vérifiez que votre fichier utilise bien `;` comme séparateur et le format `Date;Time;Sender;Message` |
| PNG/PDF ne se génèrent pas | Vérifiez votre connexion internet et que les indicateurs sont verts |
| Caractères mal affichés | Assurez-vous que votre CSV est encodé en UTF-8 |
| Bouton "Sélectionner un fichier" illisible en mode clair | C'est corrigé, le texte reste blanc sur le bouton bleu |

## 9. Astuces

- Le fichier HTML téléchargé est autonome - vous pouvez l'envoyer par email ou le partager sans avoir besoin de l'application
- Le thème de l'application et le thème d'export sont indépendants
- Tous les traitements sont locaux - vos conversations ne quittent jamais votre appareil
- Pour de très longues conversations, le PDF sera automatiquement paginé sur plusieurs pages A4
