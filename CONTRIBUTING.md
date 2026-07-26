# Guide de contribution — tryandrun

Bienvenue ! Ce repo sert à tester et exécuter du code d'équipe et de stagiaires. Merci de suivre ces quelques règles pour que tout le monde puisse travailler sans se marcher dessus.

## Organisation des dossiers

Chaque contributeur travaille dans son propre dossier :

```
tryandrun/
  README.md
  .gitignore
  CONTRIBUTING.md
  /votre-nom/
  /shared/          ← code commun réutilisable par tous
```

Créez votre dossier avec votre prénom ou pseudo GitHub, et ne modifiez que le vôtre (sauf `/shared/`, qui peut être modifié par tous mais avec une pull request).

## Workflow pour pousser du code

1. Récupérer les derniers changements :
   ```
   git checkout main
   git pull origin main
   ```

2. Créer une branche pour votre travail (ne jamais push directement sur `main`) :
   ```
   git checkout -b votre-nom/nom-de-la-tache
   ```

3. Coder, puis commiter :
   ```
   git add .
   git commit -m "description claire du changement"
   ```

4. Pousser votre branche :
   ```
   git push origin votre-nom/nom-de-la-tache
   ```

5. Ouvrir une **Pull Request** sur GitHub vers `main`, et attendre une revue/validation avant de merger.

## Règles

- Jamais de push direct sur `main` — toujours passer par une pull request.
- Un nom de branche clair : `votre-nom/ce-que-vous-faites`.
- Des messages de commit descriptifs (pas juste "fix" ou "update").
- Ne pas commiter de secrets, clés API, mots de passe, ou fichiers `.env` (déjà exclus par `.gitignore`).
- Si vous touchez à `/shared/`, prévenez l'équipe avant de merger.

## Environnement Python

Utilisez un environnement virtuel pour isoler vos dépendances :
```
python -m venv venv
source venv/bin/activate   # ou venv\Scripts\activate sous Windows
pip install -r requirements.txt
```

Bon code à tous !
