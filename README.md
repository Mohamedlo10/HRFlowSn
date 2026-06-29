# HRFlowSn - Système de Gestion des Ressources Humaines

HRFlowSn est une application web complète de gestion des ressources humaines, développée en PHP avec une architecture MVC, sans utiliser de framework lourd. Elle propose une interface moderne, fluide et réactive (inspirée du Claymorphism), adaptée aux besoins de gestion du personnel.

---

## 🛠 Stack Technique

- **Backend** : PHP 8 (Architecture MVC native)
- **Base de données** : MySQL 5.7+
- **Serveur Web** : Apache (Recommandé via XAMPP)
- **Frontend** : HTML5, CSS3 (Custom), Bootstrap 5 (Grille et composants basiques)
- **Graphiques** : Chart.js
- **Export PDF** : DOMPDF
- **Export Excel** : PhpSpreadsheet

---

## 📋 Prérequis

Avant de commencer l'installation, assurez-vous de disposer des éléments suivants sur votre machine :

1. **Serveur Local (XAMPP / WAMP / MAMP)**
   - PHP version 8.0 ou supérieure.
   - MySQL version 5.7 ou supérieure (ou MariaDB).
   - Module Apache activé.
2. **Extensions PHP requises** (à vérifier dans votre `php.ini`) :
   - `pdo_mysql`
   - `mbstring`
   - `gd`
   - `zip`
3. **Navigateur Web Moderne** (Chrome, Firefox, Safari, Edge).

---

## 🚀 Installation Étape par Étape

### 1. Déploiement des fichiers

**Si vous utilisez XAMPP sous Windows :**
1. Téléchargez ou clonez le projet.
2. Copiez le dossier `HRFlowSn` dans votre répertoire web : `C:\xampp\htdocs\`.
   *Le chemin final devrait être : `C:\xampp\htdocs\HRFlowSn`.*

**Si vous utilisez XAMPP sous Mac :**
1. Copiez le dossier dans `/Applications/XAMPP/xamppfiles/htdocs/`.
   *Le chemin final devrait être : `/Applications/XAMPP/xamppfiles/htdocs/HRFlowSn`.*

**Si vous utilisez Linux :**
1. Copiez le dossier dans `/var/www/html/` ou `/opt/lampp/htdocs/`.
2. Assurez-vous des bonnes permissions : `sudo chown -R www-data:www-data /var/www/html/HRFlowSn`.

### 2. Création de la Base de Données

1. Lancez **XAMPP** et démarrez les services **Apache** et **MySQL**.
2. Ouvrez votre navigateur et accédez à **phpMyAdmin** : `http://localhost/phpmyadmin`
3. Cliquez sur **Nouvelle base de données** dans le menu de gauche.
4. Nommez la base : `hrflowsn_db` (Encodage recommandé : `utf8mb4_unicode_ci`).
5. Cliquez sur le bouton **Créer**.

### 3. Importation des Données (2 options)

Rendez-vous dans votre nouvelle base de données `hrflowsn_db` sur phpMyAdmin, puis allez dans l'onglet **Importer**.
Vous avez le choix entre deux fichiers SQL situés à la racine du projet :

- **Option A (Base vierge)** : Importez `hrflowsn.sql`. Cela va créer la structure de la base et ajouter uniquement les rôles, départements, et paramètres de base de l'entreprise.
- **Option B (Avec Données de Démonstration)** : Importez `hrflowsn_demo.sql`. Cela va générer des dizaines d'employés, de contrats, de congés, d'évaluations et de formations pour vous permettre de tester immédiatement l'application.

> **Identifiants de Démonstration (Si Option B choisie) :**
> - **Administrateur** : `admin@hrflowsn.sn` / Mot de passe : `password`
> - **RH** : `rh@hrflowsn.sn` / Mot de passe : `password`
> - **Manager** : `manager@hrflowsn.sn` / Mot de passe : `password`
> - **Employé** : `employe@hrflowsn.sn` / Mot de passe : `password`

### 4. Configuration de la Base de Données

Ouvrez le fichier `config/database.php` avec votre éditeur de code. Vérifiez et modifiez si besoin les informations de connexion :

```php
private $host = "localhost";
private $db_name = "hrflowsn_db";
private $username = "root";
private $password = ""; // Sous XAMPP Windows/Mac, le mot de passe est vide par défaut
```

---

## 💻 Démarrage et Utilisation

Une fois l'installation terminée, ouvrez votre navigateur et tapez l'adresse suivante :
👉 **http://localhost/HRFlowSn**

Vous arriverez sur la page de connexion. Connectez-vous avec un compte existant (ou un des comptes de démonstration).

### Résolution des Problèmes Courants (FAQ)

- **Erreur (HY000/2002) - No such file or directory** :
  Cela signifie que PHP n'arrive pas à se connecter au socket MySQL (très fréquent sur Mac). Dans `config/database.php`, essayez de remplacer `localhost` par `127.0.0.1`.
- **Page blanche ou erreurs 404** :
  Vérifiez que le nom de votre dossier dans `htdocs` s'appelle bien exactement `HRFlowSn`. Si vous l'avez nommé autrement, vous devez adapter les liens internes dans le code (notamment les redirections header).

---

## 📚 Documentation Supplémentaire
Pour apprendre à utiliser chaque module de l'application (Tableau de bord, Collaborateurs, Contrats, Congés, Paie...), veuillez consulter le document `MANUEL_UTILISATEUR.md` disponible à la racine du projet. Ce manuel vous guidera visuellement à travers toutes les fonctionnalités de HRFlowSn.
