# LexImpact prix carburants

Agrège les prix des carburants TTC par mois, par an et par région ou France entière dans des fichiers CSV.

## Notebook_INSEE

Recupère l'integralité des prix du carburant TTC disponible (SP 95, SP 98, super plombé, gasoil, SP E10) sur le site de l'INSEE.

Crée 2 fichiers CSV, des prix des carburants par an, en litre et en héctolitre.

Crée 2 fichiers CSV, des prix des carburants par mois, en litre et en héctolitre.


## Notebook_gouv

Recupère l'integralité des prix du carburant TTC disponible, par station service, type de carburant (SP 95, SP 98, E85, gasoil, SP E10, GPLc) et par jour, sur le site [prix-carburant.gouv.fr](https://www.prix-carburants.gouv.fr/).

Retrouve le code région de chaque station service (à l'aide d'APIs, et partant de la latitude et la longitude et/ou du code postal, pour retrouver le citycode, puis le code departement, puis le code région).

Crée 1 fichier CSV, des prix agrégé des carburants par région et par an, en litre.

Crée 1 fichier CSV, des prix des carburants par région et par mois, en litre.

Crée 2 fichiers de prix agrégés au niveau national afin de pouvoir vérifier l'exactitude par rapport aux données de l'INSEE

## Installation

### Clonage

```shell
git clone https://git.leximpact.dev/leximpact/prix-carburants.git
cd prix-carburants
```

### Création de l'environnement virtuel et installation des packages (Linux)

Ces scripts nécessitent Python3, Jupyterlab, Pandas et requests.

```shell
python3 -m venv .venv
source .venv/bin/activate
pip install jupyterlab
pip install pandas
pip install requests
```

### Lancement

```shell
jupyter-lab
```

### Utilisation

Pour les prix par mois et par année de l'INSEE, ouvrir [notebook_insee.prix_carburant.ipynb](./notebook_INSEE/prix_carburant.ipynb).

Pour les prix agrégé par région, par moi et par année, ouvrir [notebook_gouv.prix_carburant.ipyn]().

**ATTENTION:** Il faut créer un compte sur le site du catalogue des APIs de l'INSEE, et créer un token pour utiliser l'API "[Métadonnées - V1](https://api.insee.fr/catalogue/site/themes/wso2/subthemes/insee/pages/item-info.jag?name=M%C3%A9tadonn%C3%A9es&version=V1&provider=insee)" (Le token fonctionne 7 jours). Le token devra étre intégré directement dans le notebook.

**REMARQUE:** Les fichiers CSV sont disponible directement sans utiliser le code.

## Copyright

LexImpact Prix carburants est un logiciel libre sous [licence GNU Affero General Public License](./LICENSE.md).

Copyright (c) 2022 Assemblée nationale

Auteur : Kendrick Herzberg, <herzbergkendrick@gmail.com>