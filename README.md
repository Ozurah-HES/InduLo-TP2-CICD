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
> `Virtualenv location: C:\Users\Jonas\.virtualenvs\InduLo-TP2-CICD-rH-l5pIE`

**A chaque démarrage du projet (ex ouverture VSC), il faut activer l'environnement virtuel** :
```bash
# Activer l'environnement virtuel
pipenv shell
```

Les fichiers `pipfile` (généré avec `pipenv`) sont à push sur le repo git, mais pour ce TP, on utilisera explicitement le requirements pour le CI/CD. Ce n'est donc pas obligatoire de push le pipfile.