## Check ticket dans trello
- List To Do
- Mettre dans List In Progress quand on le commence

## Creer branche avec un nom claire en se basant sur le ticket et feature a integrer
- Toujours s'assurer que tu cree une branche a partir de dev
- Ex: feature/add-login

## Avant de faire un pr
Toujours rebase avant pr :
- git stash push -u            # Sauvegarde tes changements non commités
- git checkout dev
- git pull origin dev    # Met à jour dev
- git checkout feat
- git rebase dev         # Rebase feat sur la nouvelle version de dev
GERER CONFICT : git rebase --continue
- git stash pop          # Récupère tes changements
- Après git stash pop, # Il pourrait y avoir des conflits, à résoudre comme d'habitude.

## Gestion de conflit
En cas de conflit:
- git checkout dev 
- git pull origin dev
- git checkout feature
- git rebase dev
- resolve conflits
- git add <fichier_conflit>
- git rebase --continue
- git push -f

## Faire le pr
- add et commit le code en suivant la convention de message commit
- push ton code 
- creer un pull request en s'assurant que le cible est **dev** mais pas **main**
- Indiquer le pull request dans le salon discord dedier
- Deplacer le ticket dans To Validate

## PR Dans le discord
backend: Nom ticket dans trello
pr: github.com/lien-repo/pull/numero-pull

- pr **accepted** and merged: ✅ 
- pr **refused** and merged: ❌ (conflit ou code qui ne suit pas les conventions)

## Marquer ticket comme fini
- Deplacer le ticket trello dans Finished and Approved