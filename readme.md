# Demo 01 - Introduction au Github Action 

## Part 1 : Syntaxe 

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

## Part 2 : Variables 

### Mise en Place
- Nouveau fichier `workflow`
- Push sur Github
- Utilisation des variables & secrets: 
    - Definir une "Zone" `env` dans le workflow (attention is public!)
    - Definir dans le parametres du repo Github
    - Manipuler les variables d'event du workflow (Lié au declenchement)

### Syntaxe d'utilisation

### Variable d'env local: 
    - Sous Linux `$VAR_NAME`
    - Sous Powershell `$env:VAR_NAME`

### Variable et secrets dans Github
Aller à `Setting > Secrets and variables > Actions` pour configurer les variables.
Deux types de configuration : 
- Repository: Toujours accessible 
- Environment: Accessible si le job utilise `environment: env-name`

Utilisation
- variables: `${{ vars.VAR_NAME }}`
- secrets: `${{ secrets.VAR_NAME }}`
