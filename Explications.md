# Exercise 1
## Objectifs
Comprendre comment :
- créer un dépôt (repo) GitHub depuis le terminal,  
- y effectuer des changements,  
- et suivre l’historique des versions avec Git.
## Étapes du projet
### 1. Création et clonage du dépôt

```bash
gh repo create git-learning-1 --public --clone
````
**Explication :**

* `gh repo create` permet de créer un dépôt sur GitHub.
* `git-learning-1` est le nom du dépôt.
* `--public` rend le dépôt accessible à tous.
* `--clone` télécharge automatiquement le dépôt sur l’ordinateur local.

Cette commande permet donc de créer et de cloner le dépôt sans passer par l’interface web.

### 2. Entrer dans le dossier du projet

```bash
cd git-learning-1
```
**Explication :**

* `cd` (change directory) permet de se déplacer dans le dossier du dépôt.

### 3. créer la branche main
```bash
git checkout -b main
```
**Explication :**
Cette commande sert à créer une nouvelle branche nommée main et à se déplacer immédiatement dessus.

* `git checkout` : permet de changer de branche.
* `-b` : indique à Git de créer une nouvelle branche avant de s’y rendre.
* `main` : est le nom de la nouvelle branche.

### 4. Créer un fichier README.md

```bash
echo "Mon premier projet Git" > README.md
```
**Explication :**

* `echo` écrit une ligne de texte.
* Le symbole `>` crée un fichier et y place le texte indiqué.
* Ici, le fichier `README.md` est créé et contient la phrase « Mon premier projet Git ».

Le fichier `README.md` sert à décrire le projet sur GitHub.

### 5. Ajouter le fichier au suivi Git

```bash
git add README.md
```
**Explication :**

* `git add` indique à Git de suivre ce fichier pour le prochain enregistrement (commit).

### 6. Faire le premier commit

```bash
git commit -m "Initial commit with README"
```

**Explication :**

* `git commit` enregistre les changements localement.
* L’option `-m` permet d’ajouter un message clair décrivant le changement.

Un commit représente une version du projet.

### 7. Envoyer les changements sur GitHub

```bash
git push origin main
```

**Explication :**

* `git push` envoie les commits vers GitHub.
* `origin` représente le dépôt distant.
* `main` est la branche principale du projet.

Après cette étape, le fichier `README.md` est disponible sur GitHub.

---

### 8. Ajouter le nom et l’adresse MAC

```bash
echo "Boureima Issa Adamou Razak" >> README.md
echo "Mac N*2" >> README.md
```

**Explication :**

* `echo` ajoute une nouvelle ligne dans le fichier.
* `>>` ajoute le texte à la fin du fichier sans supprimer le contenu précédent.

### 8. Enregistrer et envoyer la mise à jour

```bash
git add README.md
git commit -m "Ajout nom et MAC"
git push origin main
```

**Explication :**

* `git add` ajoute à nouveau le fichier modifié.
* `git commit` crée une nouvelle version avec un message clair.
* `git push` envoie la mise à jour sur GitHub.

## Difficultés rencontrées

1. **Installation de GitHub CLI sur Windows**
   L’installation peut être compliquée sur certains systèmes Windows.
   Il faut télécharger l’outil depuis [https://cli.github.com/](https://cli.github.com/), puis vérifier que la commande `gh` fonctionne dans le terminal.
   Si ce n’est pas le cas, il faut vérifier les variables d’environnement (PATH) ou redémarrer le terminal.
   ou bien faire :  `winget install --id GitHub.cli` depuis **PowerShell**

2. **Authentification GitHub**
   Lors de la première utilisation de `gh repo create`, il faut se connecter à GitHub depuis le navigateur pour autoriser la CLI à accéder au compte.

## Résultat final

À la fin du projet, le fichier `README.md` contient :

```
Mon premier projet Git Boureima Issa Adamou Razak Mac N*2
```

Ce fichier est ensuite visible directement dans le dépôt GitHub.

## Bilan

Ce projet m’a permis de :

* créer un dépôt GitHub depuis le terminal,
* faire mes premiers commits,
* envoyer mes modifications sur GitHub,
* comprendre le fonctionnement du suivi de version,
* et apprendre à résoudre les problèmes liés à l’environnement Windows.

**Outil utilisé :** GitHub CLI
**Système :** Windows
**Langage :** Bash
**Type de projet :** Initiation à Git et GitHub
