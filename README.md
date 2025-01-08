# :technologist: **Init the tools -> AI4Industry.**

## Intro.
Ce dépôt contient des infos sur les outils de base pour faire de l'IA.

Vu en cours, code CNAM `USRS6V`.

## :package: Logiciels requis.
`Docker` est nécessaire pour suivre ce tuto.

Pour l'installer [par ici !](https://www.docker.com/)

## :boom::boom: C'est parti, création du conteneur.
Pour le conteneur on ajouter le port `8888` pour pouvoir accéder au serveur `Jupyter` depuis la machine hôte.
```bash
docker run -it --name init_ai4industry -p 8888:8888 ubuntu
```

Le terminal que vous utilisez va automatiquement basculer sur le conteneur. A noter que vous entrez donc sur une image ubuntu, en mode `root`, donc la commande `sudo`est inutile ici !
```bash
apt update
apt upgrade
apt install software-properties-common
add-apt-repository ppa:deadsnakes/ppa
apt install python3.7 python3.7-venv
```
Nous venons de créer le conteneur, le mettre à jour, et installer la version 3.7 de python. On peut continuer.

### :memo: Création de notre environnement de travail.
Ici nous allons nous déplacer :
```bash
cd home/ubuntu
mkdir workspace_ia
cd workspace_ia
```

Dans ce dosier nous allons créer notre environement Python. Nous utilisons ici la version `3.7`.
```bash
python3.7 -m venv venv
source venv/bin/activate
```

Maintenant, installons les bibliothèques. (le téléchargement peut prendre un peu de temps).
```
pip install jupyter==1.0.0
```

## :rocket: Lancement de `Jupyter`.