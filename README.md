### SYLLABUS – FORMATION DOCKER, JAVA, CI/CD & DÉPLOIEMENT SUR VPS

---

### Objectifs pédagogiques

À l’issue de la formation, l’apprenant saura :

* Utiliser Docker avec un projet Java (Spring Boot)
* Conteneuriser une application Java
* Gérer les réseaux, volumes et logs Docker
* Mettre en place une CI/CD avec tests et déploiement automatisé
* Configurer un VPS Linux sécurisé pour héberger l’application
* Déployer et superviser un projet en production

---

## **CHAPITRE 1 – Introduction à Docker et aux conteneurs**

### 1.1. Virtualisation vs Conteneurisation

* VM vs Conteneur
* Architecture Docker

### 1.2. Composants Docker

* Daemon, client, images, conteneurs, volumes, réseaux

### 1.3. Installation

* Docker Engine (Linux)
* Docker Desktop (Mac/Windows)
* Vérifications (`docker info`, `docker version`)

---

## **CHAPITRE 2 – Manipulations de base**

### 2.1. Démarrage et gestion des conteneurs

* `docker run`, `ps`, `stop`, `rm`, `exec`, `logs`

### 2.2. Gestion des images

* `docker pull`, `docker build`, `docker tag`, `rmi`

### 2.3. Travaux pratiques

* Exécuter une image Java officielle
* Containeriser une application HelloWorld

---

## **CHAPITRE 3 – Dockerisation d'une application Java**

### 3.1. Dockerfile pour Java

* Application JAR (`FROM eclipse-temurin`, `COPY`, `CMD`)
* Structure et bonnes pratiques

### 3.2. Build multi-stage pour Java

* Séparer build (Maven/Gradle) et exécution

### 3.3. .dockerignore et optimisation

* Réduire le contexte de build

---

## **CHAPITRE 4 – Tests unitaires et Intégration continue (CI)**

### 4.1. Introduction aux tests unitaires Java

* JUnit, Mockito, Spring Test

### 4.2. Exécution automatisée des tests

* Script Maven/Gradle

### 4.3. CI avec GitHub Actions ou GitLab CI

* Étapes : test → build → push image

### 4.4. Exemple de pipeline CI complet

* Dockerfile + `.github/workflows/docker-deploy.yml`
* Variables de secrets (Docker Hub, SSH...)

---

## **CHAPITRE 5 – Docker Compose pour une stack complète**

### 5.1. Présentation de `docker-compose.yml`

* Services, volumes, réseaux

### 5.2. Projet Java + PostgreSQL/MySQL

* API REST Java + BDD persistante

### 5.3. Gestion des variables d’environnement

* `.env` + `docker-compose.yml`

---

## **CHAPITRE 6 – Configuration d’un VPS Linux (Debian/Ubuntu)**

### 6.1. Prérequis de sécurité

* Création utilisateur
* Configuration SSH (clé privée, port, fail2ban, ufw)

### 6.2. Installation des composants

* `docker`, `docker-compose`, `certbot`, `nginx`

### 6.3. Déploiement manuel d’un conteneur

* `scp` ou `git clone` + `docker-compose up -d`

---

## **CHAPITRE 7 – Déploiement automatique (CI/CD sur VPS)**

### 7.1. Pipeline CI/CD complète

* Test → Build → Push → Déploiement

### 7.2. SSH ou Webhook pour déploiement automatique

* `appleboy/ssh-action` (GitHub)
* GitLab Runner (auto-hébergé possible)

### 7.3. Variables secrètes (Docker Hub, SSH, DB\_PASS)

### 7.4. Notifications (Slack, Discord, email – optionnel)

---

## **CHAPITRE 8 – Registry privé Docker**

### 8.1. Options de registry privé

* Docker Hub, GitHub Container Registry, GitLab Registry
* Registry privé auto-hébergé (`registry:2`, sécurisé par NGINX)

### 8.2. Push/Pull d’image depuis un registry privé

* `docker login`, `docker tag`, `docker push`

---

## **CHAPITRE 9 – Sécurité & bonnes pratiques Docker**

### 9.1. Sécurité Dockerfile et runtime

* Pas de root, user dédié, pas de `latest`, `HEALTHCHECK`

### 9.2. Scanning et audit d’image

* Trivy, Docker Scout

### 9.3. Sécuriser le VPS et le déploiement

* TLS/HTTPS, UFW, certificats, authentification forte

---

## **CHAPITRE 10 – Supervision et logs**

### 10.1. Logs des conteneurs

* `docker logs`, redirection vers fichiers, syslog

### 10.2. Monitoring simple

* `docker stats`, `prometheus`, `grafana` (optionnel)

---

## **PROJET FINAL – API REST Java + CI/CD + VPS**

### Objectifs :

* Développer une API REST Java Spring Boot
* Dockeriser l'application + BDD
* Écrire des tests unitaires
* Mettre en place une pipeline CI/CD complète
* Déployer sur un VPS via SSH automatique
* Suivi du build et des logs

### Livrables :

* `Dockerfile` + `docker-compose.yml`
* Pipeline CI/CD complet
* Script de configuration du VPS
* Rapport d’audit de sécurité et de supervision
* Schéma d’architecture et documentation technique
