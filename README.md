# LexImpact prix carburants

Agrège les prix des carburants TTC par mois, par ans et par régions ou France entière dans des fichiers CSV.

Démonstration, exemple d'utilisation : TODO: Lien vers les notebooks

## Notebook_INSEE

Recupère l'integralité des prix du carburant TTC disponible (SP 95, SP 98, super plombé, gasoil, SP E10) sur le site de l'INSEE.

Créer 2 fichiers CSV, des prix par an des carburants, en litre et en héctolitre.

Créer 2 fichiers CSV, des prix par mois des carburants, en litre et en héctolitre.


## Notebook_gouv

Recupère l'integralité des prix du carburant TTC disponible, par station service, type de carburant (SP 95, SP 98, E85, gasoil, SP E10, GPLc) et par jour, sur le site [prix-carburant.gouv.fr](https://www.prix-carburants.gouv.fr/).

Retrouve le code région de chaque station service (à l'aide d'API, et partant de la latitude et la longitude et/ou du code postal).

Créer 1 fichier CSV, des prix par région et par an des carburants, en litre.

Créer 1 fichier CSV, des prix par région et par mois des carburants, en litre.

## Installation

### Clonage

```shell
git clone https://git.leximpact.dev/leximpact/prix-carburants.git
cd prix-carburants
```

### Création de l'environnement virtuel et installation des packages

Ces scripts nécessitent Python3, Jupyter et Pandas.

```shell
python3 -m venv .venv
source .venv/bin/activate
pip install jupyter notebook
pip install pandas
```

### Lancement

```shell
jupyter notebook
```

### Utilisation

Pour les prix par mois et par années de l'INSEE, ouvrir [notebook_insee.prix_carburant.ipynb](./notebook_INSEE/prix_carburant.ipynb).

Pour les prix agrégé par régions mois et années de , ouvrir [notebook_gouv.prix_carburant.ipyn]()

**ATTENTION:** Il faut on créer un compte sur le site du catalogue des APIs de l'INSEE, et créer un token pour utiliser l'API "[Métadonnées - V1](https://api.insee.fr/catalogue/site/themes/wso2/subthemes/insee/pages/item-info.jag?name=M%C3%A9tadonn%C3%A9es&version=V1&provider=insee)" (Le token fonctionne 7 jours). Le token devra étre intégré dans le notebook.


## Copyright

LexImpact Prix carburants est un logiciel libre sous [licence GNU Affero General Public License](./LICENSE.md).

Copyright (c) 2022 Assemblée nationale

Auteur : Kendrick <herzbergkendrick@gmail.com>