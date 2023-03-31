# InduLo-TP2-CICD
TP2 du cours d'industrialisation logiciel (CI / CD)

--------------------
--------------------
**Etapes effectuées**

--------------------
--------------------

# Initialisation

Dans le dossier "cloné" 
```bash
# Installer les dépandances indiquée dans requirements.txt (avec pipenv)
pipenv install
```
> Exemple d'output :
> Successfully created virtual environment!
> `Virtualenv location: C:\Users\...\.virtualenvs\InduLo-TP2-CICD-rH-l5pIE`

**A chaque démarrage du projet (ex ouverture VSC), il faut activer l'environnement virtuel** :
```bash
# Activer l'environnement virtuel
pipenv shell
```

Les fichiers `pipfile` (généré avec `pipenv`) sont à push sur le repo git, mais pour ce TP, on utilisera explicitement le requirements pour le CI/CD. Ce n'est donc pas obligatoire de push le pipfile.

# Init Github Action

## A - Création repo sur GitHub

## B - Setup Github Action

### Quels étapes sont réalisées par le `yml` Python par défaut ?

Les étapes sont les "puces" dans la partie `steps`
1. **Checkout** : récupère le code source du projet
2. **Set up Python** : installe la version de python indiquée dans le `yml`
3. **Install dependencies** : installe les dépendances du projet (définies dans le `requirements.txt`)
4. **Lint with flake8** : linter pour vérifier la qualité du code
5. **Test with pytest** : execute les tests unitaires (CF TP1)

### Une étape est définie au minimum par 2 éléments, lesquels sont-ils et à quoi servent-ils ?

- `name` : nom de l'étape
- `run` : commande(s) à exécuter

### La première étape contient le mot-clé ‘with’, a quoi sert-il ?

Permet de transmettre des paramètres à l'étape.

## C - Modification du `yml`

Modification dans le `yml` avec le code fournis dans le TP.

### Création d'un token
> Pour permettre au runner d'avoir les droits d'accès au container `registry`.

Sur notre compte GitHub :
![](Screen/2023-03-31-10-56-56.png)

Copier le token généré (ne sera plus visible après coup)

Sur le repo du projet :
![](Screen/2023-03-31-11-08-37.png)

### Rendre notre image docker publique
!!! Attention
    Chaque choses que l'on push sur le registry est publique. Il faut donc faire attention à ce que l'on push. (ex : ne pas push des fichiers de config contenant des tokens)
