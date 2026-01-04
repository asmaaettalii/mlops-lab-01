# Rapport de Lab : CI/CD avec GitHub Actions pour un pipeline MLOps
## Introduction

Ce laboratoire a pour objectif de mettre en place une chaîne CI/CD complète pour un projet MLOps en utilisant GitHub Actions.
Le pipeline prend en charge :

L’installation des dépendances Python et DVC

L’exécution automatique du pipeline ML via DVC

La vérification des métriques (Quality Gate F1-score)

L’upload des artefacts (modèles, rapports, registry)

La simulation de déploiement (CD) sur la branche principale



## Étape 1 : Créer le dépôt GitHub et connecter le remote

### Instructions réalisées :

Création du dépôt sur GitHub : mlops-lab-01

<img width="945" height="44" alt="image" src="https://github.com/user-attachments/assets/3482d48a-ba51-4fae-8d1f-b8e054b03303" />

Connexion du dépôt local à GitHub :

<img width="945" height="88" alt="image" src="https://github.com/user-attachments/assets/0d617806-afa7-45b3-b84b-fb04d5b254e7" />

<img width="945" height="349" alt="image" src="https://github.com/user-attachments/assets/160e8bb8-f889-4059-bffe-d54e2db292e2" />

Le projet local est connecté au dépôt GitHub et la branche principale est initialisée.

## Étape 2 : Définir les secrets GitHub

### Instructions réalisées :
Création des secrets et variables pour le workflow dans GitHub → Settings → Secrets and Variables → Actions :

<img width="1187" height="357" alt="image" src="https://github.com/user-attachments/assets/83836c9b-e87e-4754-b08d-3c93a7e38dab" />

<img width="1169" height="228" alt="image" src="https://github.com/user-attachments/assets/34367be0-9a9b-4c07-89fd-c9e11a5da9aa" />

Les secrets et variables sont disponibles pour le workflow GitHub Actions.

## Étape 3 : Créer le workflow CI/CD

Fichier du workflow : .github/workflows/ci-cd.yml

Configuration principale :

Déclencheurs : push sur main et pull request

Jobs CI : installation Python, cache pip/DVC, exécution pipeline, vérification métriques, upload artefacts

Jobs CD : uniquement sur main, simulation de déploiement via SSH

<img width="945" height="477" alt="image" src="https://github.com/user-attachments/assets/2e08a403-a424-4040-8619-a77d602f94d5" />

## Étape 4 : Commit et push
Instructions :
Aller dans : GitHub → Actions

<img width="736" height="302" alt="image" src="https://github.com/user-attachments/assets/9afdd966-c2c3-4de3-ba2a-61961d7425bc" />

<img width="945" height="494" alt="image" src="https://github.com/user-attachments/assets/28a8fb57-ba0a-4a16-9387-e77f750ef88e" />

