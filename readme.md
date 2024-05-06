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


# Écrire un bon message de commit

Écrire un bon message de commit est essentiel pour la maintenance et la compréhension d'un projet. Cela aide à suivre l'évolution du projet et à comprendre les raisons derrière chaque modification.

## Structure d'un message de commit

Un message de commit se compose généralement de 2 parties :
- Un titre (en-tête) : une brève description des modifications. Doit être concis et ne pas dépasser les 50 caractères. Commence par une majuscule.
- Un corps qui donne des détails supplémentaires sur les modifications. Il est séparé du titre par une ligne blanche.

### Exercice

- Dans l'un de vos dépôts, ajoutez un nouveau fichier (.js, .html, .autre, on s'en fiche).
- Une fois le fichier ajouté, publiez la modification sur GitHub (votre dépôt doit avoir le fichier).
- Débrouillez-vous ensuite pour supprimer le fichier que vous venez d'ajouter et répercuter la suppression sur votre dépôt GitHub.

# CAS DE FIGURES

Machine nomade (portable) et un desktop.
Changement de machine.

Il faut avoir accès à la dernière version du code, récupérer, cloner, et ensuite modifier et envoyer.

# Récupérer votre travail

Pour récupérer votre travail sur une autre machine, ou simplement récupérer la dernière version en date, vous devez utiliser la commande git clone URL_DU_REPO.

Par exemple : git clone https://github.com/Errante-Creation/coursgithub2024.git

# PR (Pull Request)

C'est une fonctionnalité clé des systèmes de gestion de version basés sur git comme GitHub, GitLab, Bitbucket. Elle représente une demande de fusion de modifications (commits) d'une branche vers une autre, généralement de la branche d'une fonctionnalité vers la branche principale d'un projet.

Les recruteurs sont habitués à GitHub, GitLab.

## Concept de la Pull Request (PR)

**Collaboration et revue de code**

La PR n'est pas seulement un mécanisme de fusion de code : c'est aussi un outil de collaboration. Lorsqu'un dev soumet une PR, d'autres membres de l'équipe peuvent la consulter, laisser des commentaires, suggérer des modifs, et même proposer des commits pour améliorer la PR avant qu'elle ne soit fusionnée.

**Point de contrôle**

Avant la fusion, la PR fournit un point de contrôle pour s'assurer que le code respecte les qualités, passe tous les tests, et n'introduit pas de régressions.

**Intégration avec CI/CD (Continuous Integration/Continuous Deployment)**

Les PR sont souvent intégrées avec des outils d'intégration continue (CI) et de déploiement continu (CD). Lorsqu'une PR est soumise, des tests automatisés peuvent être déclenchés et le résultat de ces tests est souvent signalé directement dans l'interface de la PR. Automatiser le déploiement et respecter la qualité du code efficacement.

## Faire une PR

### Fork du repository

Avant de pouvoir soumettre une PR, vous devez avoir une copie du repository sur votre compte : si ce n'est pas déjà fait :
1. Allez sur la page GitHub du projet auquel vous voulez contribuer.
2. Cliquez sur "fork" pour créer un fork sur votre page personnelle, cela fera une copie du projet sur votre compte GitHub.

### Cloner le fork

Après avoir fait un fork, vous allez pouvoir travailler dessus. Pour cela, vous allez devoir cloner sur votre propre machine.

```bash
git clone URL_DU_DEPOT (attention, c'est VOTRE repo)

Par exemple :

bash
Copy code
git clone https://github.com/Errante-Creation/coursgithub2024.git
Créer une nouvelle branche
Il est conseillé de créer une nouvelle branche pour chaque fonctionnalité ou correction. Cela vous permet de garder le travail organisé et séparé.

Pour créer une nouvelle branche, vous devez utiliser la commande :

bash
Copy code
git checkout -b nomDeLaNouvelleBranche
Par exemple :

bash
Copy code
git checkout -b interfaceGUI
ou

bash
Copy code
git checkout -b search
Apporter les modifications
Modifiez le ou les fichiers nécessaires et ajoutez-les à l'index (avec git add nom_du_fichier ou git add *).

Ensuite, faites un commit de vos modifications :

bash
Copy code
git commit -m "descdesmodifications"
Pousser la branche vers le fork
bash
Copy code
git push origin nom_de_la_branche
Par exemple :

bash
Copy code
git push origin search
Créer la PR
Allez sur la page GitHub de votre fork.
Cliquez sur le bouton "New PR".
Sélectionnez votre nouvelle branche dans le menu déroulant "compare".
Assurez-vous que la branche de base (main) est celle du projet ORIGINAL et non celle de votre fork.
Vérifiez les modifications et cliquez sur "Create Pull Request".
Donnez un titre à votre PR et décrivez les modifications ou les raisons de votre PR.
Cliquez sur "Create PR" pour soumettre votre PR.
Exercice PR
Rendez-vous sur ce repo :
Fork du repo
Faites un clone du repo
Ajoutez un fichier votreprenom.md
Envoyez le fichier sur votre repo
Faites une PR
