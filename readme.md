# Demo 01 - Introduction au Github Action 

## Mise en Place
- Initializer le repo git
- Mettre le dossier sur github 
- Créer une action: `.github > workflows < first-action.yaml` 

## Syntaxe de base 
Fichier `yaml` -> Fichier structuré par tabulation 

```yaml
# Nom du workflow
name: example_syntaxe

# Triggers
on: 
  workflow_dispatch:
  push : <[branch-name]>


# Travaux à réaliser
jobs: 
  job_names:
    ...


```

### Triggers 
Ensemble des events écoutés
- Manuellement -> Bouton pour lancer le traitement 
- Push d'un branche 
- Etc...

### Travaux a realiser
L'ensemble d'action a faire 
- Runner -> Machine virtuel "prêtee par Github"
- Action à faire: 
    - Script _(Syntaxe qui depend du terminal)_
    -Utilisation d'action _(Ca sera vue plus tard)_