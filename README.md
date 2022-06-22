# LexImpact fuel prices

Aggregates fuel prices including TVA per month, per year and per region or France in CSV files.

## notebook_INSEE

Retrieves all available fuel prices (SP 95, SP 98, super leaded, gasoil, SP E10) on the INSEE website.

Creates 2 CSV files, fuel prices per year, in liter and in hectoliter.

Create 2 CSV files, of the prices of fuels per month, in liter and in hectoliter.

## notebook_gouv

Retrieves all available fuel prices, including VAT, by service station, fuel type (SP 95, SP 98, E85, diesel, SP E10, GPLc) and by day, on the site website [prix-carburant.gouv.fr](https://www.prix-carburants.gouv.fr/).

Finds the region code of each gas station (using APIs, and starting from the latitude and longitude and/or the postal code, to find the citycode, then the departement code, then the region code).

Creates 2 CSV file, of the aggregated fuel prices by region and by year, in liter and in hectoliter.

Create 2 CSV file, of the fuel prices by region and by month, in liter and in hectoliter.

Create 2 files of aggregated prices at the national level to be able to check the accuracy compared to the data of the INSEE.
## Installation
###  cloning

```shell
git clone https://git.leximpact.dev/leximpact/prix-carburants.git
cd prix-carburants
```
### Creation of the virtual environment and installation of packages (Linux)

These scripts require Python3, Jupyterlab and Pandas and requests.

```shell
python3 -m venv .venv
source .venv/bin/activate
pip install jupyterlab
pip install pandas
pip install requests
```

### Application

```shell
jupyter-lab
```

For prices by month and year from INSEE, open [notebook_insee.prix_carburant.ipynb](./notebook_INSEE/prix_carburant.ipynb).

For aggregate prices by region, month, and year, open [notebook_gouv.fuel_price.ipyn]().

**WARNING:** It is necessary to create an account on the INSEE APIs catalog website, and create a token to use the API "[Metadata - V1](https://api.insee.fr/catalogue/site/themes/wso2/subthemes/insee/pages/item-info.jag?name=M%C3%A9tadonn%C3%A9es&version=V1&provider=insee)" (The token works for 7 days). The token will have to be integrated directly in the notebook.

**REMARK:** CSV files are available directly without using the code.

## Copyright

LexImpact Fuel Prices is a free software under [licence GNU Affero General Public License](./LICENSE.md).

Copyright (c) 2022 French National Assembly

Author : Kendrick Herzberg, <herzbergkendrick@gmail.com>