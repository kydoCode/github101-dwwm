# Cours sur GitHub depuis mes notes :  

## DDL Git SCM

## Compte GitHub

- Créer un compte GitHub si vous n'en avez pas déjà un.

## Git : Repository Local, GitHub Repository Distant (Sync)

### Commandes Git

#### Les commandes de base GitHub

1. **Initialiser un repo sur GitHub :**

   - Aller sur GitHub > Nouveau dépôt
   - Nommer le dépôt, ajouter une description (optionnel), choisir la visibilité (public/privé), puis créer le dépôt.

2. **Connecter le repo distant à votre local :**

   - Utiliser le terminal ou VSCode.
   - Utiliser le terminal dans VSCode ou le terminal de votre choix.
   - Assurer que vous êtes dans le dossier du projet.

3. **Faire son premier commit :**

   - Choisir entre HTTPS / SSH (SSH nécessite une clé).
   - Utiliser HTTPS si vous débutez.
   - Initialiser GitHub sur votre machine :
     - Dans VSCode, ouvrir un nouveau terminal.
     - Utiliser `git init` pour initialiser Git dans le dossier.
   - Ajouter les fichiers à envoyer sur GitHub :
     - Utiliser `git add *` pour tous les fichiers.
     - Utiliser `git add .` pour tous les fichiers également.
     - Utiliser `git add nomdufichier` pour ajouter un fichier spécifique.

4. **Résumé des commandes :**

   - `git init` pour initialiser le repo local.
   - `git add` pour ajouter des fichiers.
   - `git add nomdufichier` pour ajouter un fichier spécifique.

## Faire la liaison avec le repo distant

Vous venez d'initialiser Git sur votre machine, mais il n'est pas encore lié avec votre repo distant. Pour cela, vous devez connecter l'origine à votre repo distant.

Commencez par ajouter un petit message qui précise les modifications/apports/suppressions effectués :

## Faire la liaison avec le repo distant

Vous venez d'initialiser Git sur votre machine, mais il n'est pas encore lié avec votre repo distant. Pour cela, vous devez connecter l'origine à votre repo distant.

Commencez par ajouter un petit message qui précise les modifications/apports/suppressions effectués :

git commit -m "Explication du commit"


Une fois le message de commit défini, choisissez la branche sur laquelle vous travaillez.

Lorsque vous souhaitez stocker vos fichiers sur GitHub, vous pouvez stocker différentes versions de vos fichiers en utilisant des branches.

### Résumé des commandes à lancer :

- `git init` pour initialiser le repo local (une seule fois par projet).
- `git add nomdufichier` ou `git add *` pour ajouter un fichier ou tous les fichiers.
- `git commit -m "Nom du commit"` pour ajouter une description de la modification ou de l'ajout.
- `git branch -m main` pour choisir la branche principale ou créer une nouvelle branche (à ne faire qu'une fois quand nécessaire).
- `git remote add origin URL_REPO_GITHUB` pour connecter le repo local et distant (à ne faire qu'une fois par projet).
- `git push -u origin main` pour publier les modifications sur GitHub.

### Informations supplémentaires :

- Pour pouvoir envoyer les fichiers sur GitHub, la première fois que vous réalisez les commandes, le système va vous demander de vous authentifier. Il faudra renseigner l'e-mail que vous avez utilisé pour créer votre compte GitHub.
- Pour configurer le compte GitHub, utilisez la commande `git config --global user.email "votreAdresse@mail.com"`.
- Les commandes `git init`, `git branch` et `git remote add origin` sont à lancer UNE SEULE fois au moment de l'initialisation du repo. Une fois exécutées, vous pouvez utiliser les commandes suivantes pendant le développement de votre projet :
  - `git add nomDuFichier` ou `git add *`
  - `git commit -m "message de commit"`
  - `git push` (une fois que vous avez spécifié le push vers origin main) ou le raccourci `git push`.
- Si vous avez déjà entré des commandes que vous devez relancer (par exemple `git add` et `git push`), vous pouvez reprendre les anciennes commandes exécutées dans le terminal en appuyant sur la flèche du haut du clavier.

# Écrire un bon message de commit

Écrire un bon message de commit est essentiel pour la maintenance et la compréhension d'un projet. Cela aide à suivre l'évolution du projet et à comprendre les raisons derrière chaque modification.

## Structure d'un message de commit

Un message de commit se compose généralement de 2 parties :
- Un titre (en-tête) : une brève description des modifications. Doit être concis et ne pas dépasser les 50 caractères. Commence par une majuscule.
- Un corps qui donne des détails supplémentaires sur les modifications. Il est séparé du titre par une ligne blanche.

Titre court et description

Corps du message; ici on explique en détail le pourquoi et le comment des changements si nécessaire. Essayer de garder chaque ligne à moins de 72 caractères pour la lisibilité.


Les backticks les font par deux pour Markdown.

## Conseils pour un bon message de commit

- Utiliser l'impératif : le titre doit être idéalement écrit à la voix impérative (ex: ajout, corrige, refactorise au lieu de ajouté, corrigé, refactorisé).
- Titre : clair et concis : doit être clair et descriptif.
- Séparer les sujets : si vous avez plusieurs modifications qui n'ont pas de rapport entre elles, envisagez de les séparer en plusieurs commits.
- Expliquer le pourquoi, pas le comment : le code lui-même montre comment une certaine chose a été faite. Ce qui n'est pas toujours clair, c'est pourquoi cette modification a été apportée. Assurez-vous d'expliquer les raisons dans le corps du message.
- Éviter les messages vagues : "Diverses corrections" ou "Mise à jour" ne sont pas des bons messages de commit. Soyez aussi descriptif que possible.
- Utiliser des références aux issues/tracker : si votre commit fait référence à une issue ou à un ticket, ajoutez cette référence dans le corps du message.

### Exemple d'un bon message de commit


Voici la suite de vos notes en format Markdown :

markdown
Copy code
# Écrire un bon message de commit

Écrire un bon message de commit est essentiel pour la maintenance et la compréhension d'un projet. Cela aide à suivre l'évolution du projet et à comprendre les raisons derrière chaque modification.

## Structure d'un message de commit

Un message de commit se compose généralement de 2 parties :
- Un titre (en-tête) : une brève description des modifications. Doit être concis et ne pas dépasser les 50 caractères. Commence par une majuscule.
- Un corps qui donne des détails supplémentaires sur les modifications. Il est séparé du titre par une ligne blanche.

Titre court et description

Corps du message; ici on explique en détail le pourquoi et le comment des changements si nécessaire. Essayer de garder chaque ligne à moins de 72 caractères pour la lisibilité.

vbnet
Copy code

Les backticks les font par deux pour Markdown.

## Conseils pour un bon message de commit

- Utiliser l'impératif : le titre doit être idéalement écrit à la voix impérative (ex: ajout, corrige, refactorise au lieu de ajouté, corrigé, refactorisé).
- Titre : clair et concis : doit être clair et descriptif.
- Séparer les sujets : si vous avez plusieurs modifications qui n'ont pas de rapport entre elles, envisagez de les séparer en plusieurs commits.
- Expliquer le pourquoi, pas le comment : le code lui-même montre comment une certaine chose a été faite. Ce qui n'est pas toujours clair, c'est pourquoi cette modification a été apportée. Assurez-vous d'expliquer les raisons dans le corps du message.
- Éviter les messages vagues : "Diverses corrections" ou "Mise à jour" ne sont pas des bons messages de commit. Soyez aussi descriptif que possible.
- Utiliser des références aux issues/tracker : si votre commit fait référence à une issue ou à un ticket, ajoutez cette référence dans le corps du message.

### Exemple d'un bon message de commit

Ajout d'une fonctionnalité de recherche

La page d'accueil avait besoin d'une fonction de recherche pour aider les utilisateurs à trouver des contenus spécifiques. Cette modification ajoute un moteur de recherche et utilise l'API de recherche pour récupérer les résultats. Relatif à l'issue #123


## En savoir plus sur le langage Markdown

Pour la rédaction de vos fichiers README, n'hésitez pas à vous pencher sur la documentation Markdown. Voici un lien pour vous aider :

[Lien pour apprendre le markdown](https://www.markdownguide.org/getting-started/)

# Éviter d'envoyer des fichiers/dossiers sur GitHub

Vous avez la possibilité de dire à GitHub qu'il y a certains fichiers et dossiers que vous ne souhaitez pas partager sur votre dépôt. Pour cela, vous allez devoir :

- Créer un fichier .gitignore à la racine de votre dossier.
- Dans le fichier .gitignore, vous devez ajouter ligne par ligne les fichiers/dossiers que vous ne souhaitez pas ajouter à votre dépôt.

## Exemple :

Fichier .gitignore :

.code.js
./css


Si vous supprimez Git comme si aucun `git init` n'a été fait alors tout l'historique de versioning.

`git remove` si déjà en ligne et qu'on a gitignore en local.

/!\ Supprimer de GitHub MAIS aussi de la machine donc avoir une copie. Si on veut forcer, utiliser `-f`.

https://github.com/Errante-Creation/coursgithub2024

### Exercice

- Dans l'un de vos dépôts, ajoutez un nouveau fichier (.js, .html, .autre, on s'en fiche).
- Une fois le fichier ajouté, publiez la modification sur GitHub (votre dépôt doit avoir le fichier).
- Débrouillez-vous ensuite pour supprimer le fichier que vous venez d'ajouter et répercuter la suppression sur votre dépôt GitHub.
