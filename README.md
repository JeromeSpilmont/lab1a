definir nano comme editeur par defaut

```
git config --global core.editor "code --wait"
```

on va dans le dossier

```
cd /c/DevOps/git/self-study/lab1a/
```

on lance le script

```
./setup-repository.bash
```

```
cd repo-challenge
```

on effectue un rebase 

```
git rebase -i Head~10
```

dans nano je  :  
switch de la ligne 1 et 2 
reword la ligne 1
edit la ligne 4  
drop la ligne 5  
squash la ligne 7 et 8  
fixup la ligne 10

```
reword 2c9811f 03- StArrtid Helo Volrd feature
pick 05a4ab5 02- Finished Hello World feature
pick 71c7325 04- Really made the thingy done
edit 650e731 05- debugging
drop 3f3de04 06- important secret
pick 30fbde7 07- Add doc - step 1
squash 66c6a4f 08- Add doc - step 2
squash 4afe664 09- Add doc - step 3
pick 76eaaad 10- Test for feature hello world
fixup f27400c 11- I forgot a semicolon
```

Je sauvegarde le fichier nano  
  
premier prompt -> reword de 03- StArrtid Helo Volrd feature

```
03- Started Hello World Feature
```

deuxième prompt

```
git commit --amend --author="Me, the Challenger <challenger@challengeland.com>" --no-edit
git rebase --continue
```

troisième prompt (squash et modification du commentaire en Add doc)

```
Add doc
```

```
 git add .
```

```
git commit -m 'add Readme.md"
```
