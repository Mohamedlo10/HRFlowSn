# HRFlowSn - Système de Gestion des Ressources Humaines

HRFlowSn est une application web de gestion des ressources humaines développée en PHP avec une architecture MVC et un design moderne Claymorphism.

## Stack Technique

- **PHP 8**
- **MySQL**
- **Apache (XAMPP)**
- **Bootstrap 5**
- **Chart.js**
- **DOMPDF** (pour les exports PDF)
- **PhpSpreadsheet** (pour les exports Excel)

## Installation

### Prérequis

- PHP 8 ou supérieur
- MySQL 5.7 ou supérieur
- Apache Server (XAMPP recommandé)
- Composer (pour les dépendances)

### Étapes d'installation

1. **Cloner le repository**
   ```bash
   git clone <repository-url>
   cd HRFlowSn
   ```

2. **Importer la base de données**
   - Ouvrir phpMyAdmin
   - Créer une nouvelle base de données nommée `hrflowsn_db`
   - Importer le fichier `hrflowsn.sql`

3. **Configurer la base de données**
   - Éditer le fichier `config/database.php`
   - Modifier les paramètres de connexion si nécessaire (hôte, utilisateur, mot de passe)

4. **Installer les dépendances**
   ```bash
   composer require dompdf/dompdf
   composer require phpoffice/phpspreadsheet
   ```

5. **Configurer les permissions**
   - Assurez-vous que les dossiers suivants sont en écriture :
     - `uploads/documents/`
     - `uploads/photos/`
     - `uploads/exports/`

6. **Démarrer le serveur**
   - Si vous utilisez XAMPP, placez le projet dans `htdocs`
   - Accédez à `http://localhost/HRFlowSn`

## Structure du Projet

```
HRFlowSn/
├── assets/
│   ├── css/          # Styles CSS
│   ├── js/           # Scripts JavaScript
│   └── images/       # Images
├── config/
│   └── database.php  # Configuration de la base de données
├── controllers/      # Contrôleurs MVC
├── models/           # Modèles MVC
├── views/
│   ├── auth/         # Vues d'authentification
│   ├── dashboard/    # Vues du dashboard
│   ├── employees/    # Vues des employés
│   ├── contracts/    # Vues des contrats
│   ├── leaves/       # Vues des congés
│   ├── payrolls/     # Vues de la paie
│   ├── trainings/    # Vues des formations
│   ├── evaluations/  # Vues des évaluations
│   ├── reports/      # Vues des rapports
│   ├── settings/     # Vues des paramètres
│   └── layouts/      # Layouts principaux
├── includes/
│   └── session.php   # Gestion des sessions
├── uploads/
│   ├── documents/    # Documents uploadés
│   ├── photos/       # Photos des employés
│   └── exports/      # Fichiers exportés
├── vendor/           # Dépendances Composer
├── database/         # Scripts SQL
├── index.php         # Point d'entrée
└── hrflowsn.sql      # Schéma de la base de données
```

## Modules

L'application comprend les modules suivants :

1. **Authentification** - Login, logout, inscription
2. **Dashboard** - Vue d'ensemble avec statistiques
3. **Collaborateurs** - Gestion des employés
4. **Contrats** - Gestion des contrats de travail
5. **Congés** - Gestion des demandes de congé
6. **Paie** - Gestion de la paie et des bulletins
7. **Formations** - Gestion des formations
8. **Évaluations** - Évaluations des employés
9. **Rapports** - Rapports et exports
10. **Paramètres** - Configuration de l'application

## Utilisateur par Défaut

Après l'installation, vous pouvez créer un compte via la page d'inscription ou insérer directement un utilisateur dans la base de données :

```sql
INSERT INTO users (role_id, email, password) VALUES (1, 'admin@hrflowsn.sn', '$2y$10$hashed_password_here');
```

Le mot de passe doit être hashé avec `password_hash()`.

## Rôles

- **Administrateur** - Accès complet à tous les modules
- **RH** - Gestion des employés, contrats, congés
- **Manager** - Vue limitée sur son équipe
- **Employé** - Accès à ses propres informations

## Design

L'application utilise un style **Claymorphism / Soft UI** avec :
- Palette de couleurs : Primary (#8B5CF6), Secondary (#EC4899), Background (#F6F4FC)
- Police : Outfit
- Icônes : Bootstrap Icons
- Framework CSS : Bootstrap 5

## Développement

Le développement est organisé en sprints :

- **Sprint 1** - Base de données, Authentification, Dashboard ✓
- **Sprint 2** - Employés, Contrats
- **Sprint 3** - Congés, Formations, Évaluations
- **Sprint 4** - Paie, Rapports, Finitions

## Support

Pour toute question ou problème, veuillez contacter l'équipe de développement.
