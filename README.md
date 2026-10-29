# Messages CSV → HTML

## Qu'est-ce que c'est ? (What)

Messages CSV → HTML est un outil web en un seul fichier (`messages_csv_html.html`) qui transforme un export CSV de conversation SMS/Message au format `Date;Time;Sender;Message` en une vue de conversation claire, élégante et exportable.

## Pourquoi l'utiliser ? (Why)

- **Visualisation propre** : Affiche la conversation sous forme de bulles de discussion avec séparateurs de date.
- **Export multi-format** : Téléchargez en HTML, PNG ou PDF.
- **100% local** : Aucun fichier n'est envoyé vers un serveur. Tout se fait dans votre navigateur.
- **Thématisation** : Thème clair/sombre pour l'application, avec détection automatique du thème du navigateur.

## Comment l'utiliser ? (How)

### 1) Préparer le fichier

Votre export doit être un fichier `.CSV` avec le séparateur `;` et les colonnes :

```
Date;Time;Sender;Message
```

Exemple :

```
mercredi 10 décembre 2025;19:20;Laurent Ramon - (06 43 43 43 60 );bonjour
QUI EST CE ?
jeudi 11 décembre 2025;09:15;Maria RALAI;Bonjour...
```

Les lignes de continuation (sans date/heure/expéditeur) sont automatiquement rattachées au message précédent.

### 2) Ouvrir l'application

Ouvrez `messages_csv_html.html` dans votre navigateur web (Chrome, Firefox, Edge, etc.).

### 3) Charger le fichier

- **Glisser-déposer** : Déposez votre fichier CSV sur la zone "Déposez votre fichier CSV".
- **Sélectionner** : Cliquez sur "Sélectionner un fichier" et choisissez votre CSV.

### 4) Personnaliser l'affichage

- **Thème de l'application** : Utilisez le sélecteur "Thème" (Clair/Sombre). Par défaut, il suit le thème de votre navigateur s'il n'y a pas de préférence enregistrée. Sinon clair par défaut.

### 5) Exporter

Une fois la conversation chargée, vous pouvez exporter :

- **Télécharger HTML** : Génère un fichier HTML standalone en mode clair avec pied de page et lien GitHub.
- **Exporter en PNG** : Capture l'intégralité de la conversation (en-tête, messages, séparateurs de date, pied de page) au format image.
- **Exporter en PDF** : Génère un PDF multipages de l'intégralité de la conversation.

## Fonctionnalités

- Parsing CSV avec `;` et gestion des lignes de continuation
- Vue type messagerie avec bulles alignées par expéditeur
- Séparateurs de date automatiques
- Préservation des sauts de ligne et emojis
- Thème clair/sombre avec persistance
- Export PNG/PDF complet (capture intégrale)
- Export HTML autonome en mode clair
- Indicateurs de dépendances CDN (html2canvas, jsPDF)
- 100% client-side

## Dépendances

L'application utilise des CDN pour les exports PNG/PDF :

- [html2canvas](https://html2canvas.hertzen.com/)
- [jsPDF](https://github.com/parallax/jsPDF)

Si vous êtes hors ligne, seul le téléchargement HTML fonctionnera. Les indicateurs en bas de page vous indiquent l'état de ces dépendances.

## Compatibilité

Fonctionne dans les navigateurs modernes avec JavaScript activé. Testé avec le format CSV fourni dans le dossier `test/`.

## Crédits

© 2026 TheKingJoker18 • [GitHub](https://github.com/TheKingJoker18/)
