# /commit

> Sauvegarde le workspace dans Git avec un message de commit clair et automatique.

---

## Mission

Quand je lance `/commit`, execute la sequence suivante sans me demander de validation intermediaire, sauf exception.

### Etape 1 : Verifier que Git est initialise

Verifie si un depot Git existe a la racine du workspace.

- Si oui : continuer.
- Si non : initialiser avec `git init`, puis creer un premier commit initial.

### Etape 2 : Verifier le statut

Lance `git status` pour voir ce qui a change depuis le dernier commit.

- Si rien n'a change, annonce : "Rien a sauvegarder, le workspace est deja a jour."
- Si des fichiers ont change, continuer.

### Etape 3 : Ajouter les fichiers

Lance `git add .` pour tout stager.

Verifie immediatement apres que `.env` n'est PAS dans la liste des fichiers stagesn (protection critique).
- Si `.env` apparait quand meme dans `git status --short`, stoppe et annonce l'erreur avant de committer.

### Etape 4 : Generer un message de commit

Regarde les fichiers modifies pour rediger un message de commit court et descriptif en francais.

Format : `type: description courte`

Types disponibles :
- `ajout` — nouveau fichier ou nouvelle fonctionnalite
- `modif` — modification d'un fichier existant
- `livrable` — nouveau livrable produit dans `livrables/`
- `contexte` — mise a jour de CONTEXT.md, HISTORY.md ou CLAUDE.md
- `fix` — correction d'une erreur

Exemples :
- `ajout: structure livrables et fichiers gitignore/env`
- `livrable: script video youtube ep12`
- `contexte: mise a jour objectifs MedKit`
- `modif: commande commit ajoutee`

Si plusieurs types s'appliquent, prends le plus significatif.

### Etape 5 : Committer

Lance `git commit -m "message genere"`.

### Etape 6 : Confirmer

Annonce le resultat :

```
Sauvegarde effectuee.

Message : [message du commit]
Fichiers sauvegardes : [nombre] fichier(s)

Ton workspace est sauvegarde localement.
Pour pousser sur GitHub : lance /push (si configure).
```

---

## Regles importantes

- Ne jamais committer `.env` ou tout fichier contenant de vraies cles d'API
- Le `.gitignore` protege deja ces fichiers, mais toujours verifier
- Si Git n'est pas configure avec un nom/email, lancer : `git config user.name "Mohamed"` et `git config user.email "mohamederreou@gmail.com"` avant le commit
- Communication en francais systematique
- Pas de tirets longs (em dashes) dans les messages
