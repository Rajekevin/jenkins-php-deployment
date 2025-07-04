# jenkins-php-deployment
Automated Jenkins pipeline to deploy a basic PHP application.   The pipeline clones the code from GitHub, performs a PHP syntax check, and deploys the application to a web server directory.   It showcases best practices for continuous integration and continuous deployment (CI/CD) using Jenkins, Git, and a local or remote server.


## Contenu du dépôt

- `index.php` : application PHP simple affichant un message.
- `Jenkinsfile` : script pipeline Jenkins pour automatiser le build, test et déploiement.
- `README.md` : ce fichier.

---

## Prérequis

- Serveur Jenkins installé et configuré (https://www.jenkins.io/doc/book/installing/)
- Serveur web (Apache, Nginx, etc.) accessible (local ou distant)
- Accès SSH configuré si déploiement sur serveur distant
- Plugin Jenkins Git installé
- Accès au dépôt GitHub

---

## Étapes de mise en place

### 1. Créer le dépôt GitHub

- Initialiser un repo nommé par exemple `jenkins-php-deployment`.
- Ajouter un fichier `index.php` minimal :

```php
<?php
echo "Hello World from Jenkins Deployment!";
?>
