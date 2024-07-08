



# Déploiement d'un Site WordPress avec MySQL en On-Premise

## Description

Ce projet déploie un site WordPress couplé à une base de données MySQL dans un environnement on-premise. Les éléments clés de l'infrastructure comprennent l'utilisation de volumes persistants pour la persistance des données, des secrets pour sécuriser les informations sensibles, un contrôleur Ingress NGINX pour la gestion des entrées HTTP(S) et MetalLB pour fournir des adresses IP Load Balancer dans un cluster Kubernetes.

## Prérequis

Avant de commencer, assurez-vous d'avoir les éléments suivants installés et configurés :

- Un cluster Kubernetes (version 1.18+)
- Kubectl (version 1.18+)
- Helm (version 3+)
- MetalLB (pour le load balancing)
- Ingress Controller NGINX

## Valeur Ajoutée

- **Sécurité des données** : Utilisation de secrets Kubernetes pour protéger les informations sensibles telles que les mots de passe de la base de données.
- **Persistance des données** : Implémentation de volumes persistants pour garantir que les données de WordPress et MySQL ne sont pas perdues lors des redémarrages des pods.
- **Scalabilité et gestion du trafic** : Utilisation d'Ingress NGINX et de MetalLB pour la gestion du trafic et la mise en place de solutions de load balancing efficaces.
- **Déploiement automatisé** : Scripts de déploiement automatisés pour simplifier et accélérer la mise en place de l'infrastructure.

## Déploiement

### Étape 1: Cloner le dépôt

Clonez ce dépôt sur votre machine locale :

```bash
git clone https://github.com/votre-utilisateur/votre-repo.git
cd votre-repo
```

### Étape 2: Déploiement de MetalLB

Suivez les instructions du dépôt [MetalLB](https://metallb.universe.tf/installation/) pour installer et configurer MetalLB dans votre cluster Kubernetes.

### Étape 3: Déploiement d'Ingress NGINX

Suivez les instructions du dépôt [NGINX Ingress Controller](https://kubernetes.github.io/ingress-nginx/deploy/) pour installer le contrôleur Ingress NGINX.

### Étape 4: Déploiement de WordPress et MySQL

Appliquez les fichiers de configuration Kubernetes présents dans le dépôt pour déployer les volumes persistants, les secrets, ainsi que les déploiements et services pour WordPress et MySQL.

```bash
kubectl apply -f .

```

## Accès au Site

Une fois les déploiements terminés, vous pouvez accéder à votre site WordPress en ouvrant un navigateur et en allant à l'adresse `http://<votre-domaine>`.

## Auteurs

- [Votre Nom](https://github.com/votre-utilisateur)

