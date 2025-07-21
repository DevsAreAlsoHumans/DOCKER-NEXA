**SYLLABUS – COURS COMPLET DOCKER ORIENTÉ JAVA + CI/CD GITHUB ACTIONS + VPS**

**Objectifs pédagogiques** :
À l’issue de la formation, l’apprenant sera capable de :

* Comprendre et utiliser Docker avec des projets Java
* Écrire des Dockerfiles efficaces pour des applications Spring Boot ou Java SE
* Implémenter une pipeline CI/CD avec exécution de tests, création d’image, et déploiement automatique
* Gérer le cycle de vie d’une application Java conteneurisée jusqu’à sa mise en production sur un VPS Linux
* Mettre en œuvre des bonnes pratiques de sécurité et d’automatisation

---

### **CHAPITRE 1 – Introduction à Docker et à la conteneurisation**

**1.1. Virtualisation vs Conteneurisation**
**1.2. Architecture Docker (daemon, CLI, registry)**
**1.3. Installation Docker sur Linux / Windows / Mac**
**1.4. Premier conteneur : `docker run hello-world`**

---

### **CHAPITRE 2 – Bases de manipulation des conteneurs**

**2.1. Lancer, arrêter, supprimer un conteneur**
**2.2. Travailler en mode interactif et détaché**
**2.3. Accéder aux logs, entrer dans le shell (`exec`, `logs`)**
**2.4. Introduction aux images (`pull`, `rmi`, `inspect`)**

---

### **CHAPITRE 3 – Création d’images personnalisées pour Java**

**3.1. Structure du Dockerfile pour une app Java (avec JAR)**

* Exemple : projet Maven ou Gradle
* `FROM eclipse-temurin:17`, `COPY`, `CMD`, etc.
  **3.2. Optimisation du Dockerfile (couche de build vs runtime)**
  **3.3. Gestion de `.dockerignore` et des artefacts**

---

### **CHAPITRE 4 – Tests unitaires et intégration continue (CI)**

**4.1. Écriture de tests unitaires JUnit / Mockito dans un projet Java**
**4.2. Exécution automatique des tests dans la pipeline**
**4.3. Déclenchement du build uniquement si les tests passent**
**4.4. Exemple avec GitLab CI / GitHub Actions :**

* Étapes : checkout, test, build image, push

---

### **CHAPITRE 5 – Docker Compose et environnement multi-conteneurs**

**5.1. `docker-compose.yml` pour Java + PostgreSQL ou MySQL**
**5.2. Configuration des volumes et des réseaux**
**5.3. Variables d’environnement pour la BDD**
**5.4. Déploiement local complet : `docker-compose up -d`**

---

### **CHAPITRE 6 – Configuration d’un VPS pour hébergement**

**6.1. Préparation d’un VPS Linux (Debian/Ubuntu)**

* Création utilisateur, sécurisation SSH, pare-feu (UFW)
  **6.2. Installation de Docker et Docker Compose sur le VPS**
  **6.3. Configuration du nom de domaine et du reverse proxy (NGINX ou Traefik)**
  **6.4. Sécurisation TLS avec Let's Encrypt (Certbot)**

---

### **CHAPITRE 7 – CI/CD avec déploiement sur VPS**

**7.1. Pipeline CI/CD complète :**

* Étapes : test → build → push image → SSH ou webhook vers VPS
  **7.2. Configuration d’un runner GitLab auto-hébergé (ou GitHub Actions)**
  **7.3. Script de déploiement automatique via SSH :**
* `scp` ou `rsync` des fichiers, puis `docker-compose up -d`
  **7.4. Gestion des secrets et accès sécurisés**
* `.env`, `vault`, GitHub secrets, GitLab variables

---

### **CHAPITRE 8 – Sécurité et bonnes pratiques**

**8.1. Exécution sous utilisateur non-root**
**8.2. Analyse des vulnérabilités avec Trivy / Docker Scout**
**8.3. Limiter les permissions, ports, ressources**
**8.4. Bonnes pratiques Dockerfile et compose (labels, healthcheck)**

---

### **CHAPITRE 9 – Monitoring et logs en production**

**9.1. `docker logs`, `docker stats`, `docker top`**
**9.2. Centralisation des logs via Fluentd ou journald**
**9.3. Mise en place de Prometheus + Grafana (optionnel)**

---

### **CHAPITRE 10 – Projet final Java + Docker + CI/CD + VPS**

**Objectif du projet :**
Conteneuriser une API REST Java (Spring Boot) avec base de données, tests automatisés, pipeline CI/CD, et déploiement automatique sur un VPS.

**Livrables attendus :**

* `Dockerfile` optimisé
* `docker-compose.yml` fonctionnel
* Pipeline GitHub Actions ou GitLab CI avec :

  * Tests JUnit
  * Build image Docker
  * Push sur Docker Hub ou registry privé
  * Déploiement sur VPS via SSH
* Rapport décrivant l’architecture, le pipeline, la sécurisation du VPS et la supervision

