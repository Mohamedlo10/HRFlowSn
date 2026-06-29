# Manuel Utilisateur - HRFlowSn
**Version : 1.0**
**Date : Juin 2026**

---

## 📑 Sommaire

1. [Introduction](#1-introduction)
2. [Premiers pas](#2-premiers-pas)
   - 2.1 Connexion à l'application
   - 2.2 Présentation de l'interface principale
3. [Profils et Rôles Utilisateurs](#3-profils-et-rôles-utilisateurs)
4. [Module : Tableau de bord](#4-module--tableau-de-bord)
5. [Module : Gestion des Collaborateurs](#5-module--gestion-des-collaborateurs)
   - 5.1 Ajouter un collaborateur
   - 5.2 Voir et modifier le profil d'un collaborateur
6. [Module : Gestion des Contrats](#6-module--gestion-des-contrats)
   - 6.1 Créer un nouveau contrat
   - 6.2 Renouvellement et modification
7. [Module : Congés & Absences](#7-module--congés--absences)
   - 7.1 Faire une demande de congé
   - 7.2 Validation par les Managers/RH
8. [Module : Évaluations](#8-module--évaluations)
   - 8.1 Planifier une évaluation
   - 8.2 Attribuer une note (Nouveau)
9. [Module : Paie (Simulée)](#9-module--paie)
10. [Module : Formations](#10-module--formations)
11. [Module : Paramètres et Rapports](#11-module--paramètres-et-rapports)
12. [Annexes et Résolution de problèmes](#12-annexes-et-résolution-de-problèmes)

---

## 1. Introduction

Bienvenue dans le manuel d'utilisation de **HRFlowSn**, votre système de gestion des ressources humaines de nouvelle génération. Ce manuel a pour but de vous guider à travers toutes les fonctionnalités de l'application, afin d'optimiser la gestion de votre personnel. 

L'application a été pensée pour être intuitive, rapide et réactive. Elle utilise un design moderne (Claymorphism) pour rendre l'expérience utilisateur la plus agréable possible.

---

## 2. Premiers pas

### 2.1 Connexion à l'application

Pour accéder à HRFlowSn, ouvrez votre navigateur web et rendez-vous sur l'adresse fournie par votre administrateur (ex: `http://localhost/HRFlowSn`).

Vous arriverez sur la page d'authentification.

> `[Insérer ici la capture d'écran de la page de Login]`

- Saisissez votre **Adresse Email**.
- Saisissez votre **Mot de passe**.
- Cliquez sur **Se connecter**.

### 2.2 Présentation de l'interface principale

Une fois connecté, vous découvrirez l'interface principale structurée en deux parties :

1. **La barre de navigation latérale (Sidebar)** : Située à gauche, elle regroupe tous les modules auxquels vous avez accès en fonction de votre rôle.
2. **L'espace de travail central** : C'est ici que s'afficheront les informations, les formulaires et les tableaux de données.

> `[Insérer ici la capture d'écran globale de l'interface principale (Sidebar + Espace de travail)]`

---

## 3. Profils et Rôles Utilisateurs

L'application HRFlowSn gère les permissions via un système de rôles stricts :

- **Administrateur** : A accès à tout le système, y compris la création de comptes utilisateurs et les paramètres globaux de l'entreprise.
- **RH (Ressources Humaines)** : Peut gérer les collaborateurs, les contrats, valider tous les congés, gérer les évaluations et la paie. N'a généralement pas accès aux paramètres techniques.
- **Manager** : Peut voir les collaborateurs de son équipe, approuver leurs demandes de congés et mener leurs évaluations.
- **Employé** : Ne voit que ses propres informations. Peut soumettre des demandes de congés, voir ses fiches de paie et ses évaluations.

---

## 4. Module : Tableau de bord

Le tableau de bord (Dashboard) est la première page que vous voyez après la connexion. Il vous donne une vision à 360° de la santé de votre entreprise.

> `[Insérer ici la capture d'écran du Tableau de Bord avec les graphiques]`

**Que trouve-t-on sur le tableau de bord ?**
- **Cartes récapitulatives** : Nombre total d'employés, congés en cours, alertes (ex: contrats arrivant à échéance).
- **Graphiques analytiques** : 
  - Répartition des employés par département (Graphique circulaire/Pie chart).
  - Évolution des recrutements ou répartition par genre (Graphique en barres).
- **Activités récentes** : Les dernières actions effectuées sur le système.

---

## 5. Module : Gestion des Collaborateurs

Ce module est le cœur de l'application. Il permet de gérer le dossier complet de chaque employé.

> `[Insérer ici la capture d'écran de la liste des collaborateurs]`

### 5.1 Ajouter un collaborateur

Pour ajouter un nouveau collaborateur, cliquez sur le bouton **"Nouveau Collaborateur"** en haut à droite.

> `[Insérer ici la capture d'écran du formulaire de création d'employé]`

**Étapes de création :**
1. Remplissez d'abord les **informations de connexion** (Email, Mot de passe, Rôle). Cela créera le compte utilisateur de l'employé.
2. Remplissez les **informations personnelles** (Nom, Prénom, Genre, Date de naissance).
3. Remplissez les **informations professionnelles** (Département, Poste).
4. Cliquez sur **Enregistrer**.

*Note : La date d'embauche et le salaire de base ne sont pas demandés ici. Ils seront automatiquement calculés lors de la création du contrat du collaborateur.*

### 5.2 Voir et modifier le profil d'un collaborateur

Depuis la liste, cliquez sur l'icône "Oeil" (Voir) pour afficher le profil détaillé.

> `[Insérer ici la capture d'écran du profil détaillé d'un collaborateur (Vue 360)]`

La vue détaillée est un dossier complet qui regroupe, sous forme d'onglets ou de cartes :
- Ses informations générales.
- L'historique de ses contrats.
- L'historique de ses demandes de congés.
- Ses évaluations passées.
- Ses fiches de paie.

---

## 6. Module : Gestion des Contrats

Un collaborateur nouvellement créé a besoin d'un contrat pour que son statut soit pleinement actif.

> `[Insérer ici la capture d'écran de la liste des contrats]`

### 6.1 Créer un nouveau contrat

Lors de la création d'un contrat :
1. Sélectionnez le collaborateur dans la liste déroulante (S'il vient d'être créé, il sera déjà pré-sélectionné).
2. Choisissez le type (CDI, CDD, Stage, etc.).
3. Entrez le **Salaire de base** et la **Date de début**.
4. Renseignez la date de fin (si CDD) et la période d'essai éventuelle.

**Automatisme important** : Une fois le premier contrat validé, la date de début du contrat devient automatiquement la date d'embauche de l'employé, et le salaire renseigné mettra à jour son salaire de base.

> `[Insérer ici la capture d'écran du formulaire de contrat]`

### 6.2 Renouvellement et modification

Pour renouveler un contrat (ex: Passage de CDD à CDI), il est recommandé de clôturer l'ancien contrat (Statut: Expiré) et d'en créer un nouveau afin de garder un historique propre.

---

## 7. Module : Congés & Absences

Le module de gestion des congés simplifie le suivi des absences.

> `[Insérer ici la capture d'écran du module des Congés (Liste des demandes)]`

### 7.1 Faire une demande de congé (Vue Employé)

Un employé peut soumettre une demande depuis son espace :
1. Cliquer sur **Nouvelle demande**.
2. Choisir le type de congé (Annuel, Maladie, etc.).
3. Définir la date de début et la date de fin.
4. Ajouter un motif si nécessaire et valider.

> `[Insérer ici la capture d'écran du formulaire de demande de congé]`

### 7.2 Validation par les Managers/RH

Les profils RH et Managers reçoivent ces demandes dans leur onglet "Congés".
- Ils peuvent consulter les détails.
- Cliquer sur **Approuver** (la demande passe au vert) ou **Refuser** (la demande passe au rouge).

---

## 8. Module : Évaluations

Ce module permet de suivre les performances des collaborateurs.

> `[Insérer ici la capture d'écran de la liste des évaluations]`

### 8.1 Planifier une évaluation

1. Cliquez sur **Nouvelle Évaluation**.
2. Sélectionnez l'employé.
3. Fixez la date de l'entretien.
4. Rédigez les objectifs et les observations globales.
5. Sauvegardez (sans mettre de note pour le moment).

### 8.2 Attribuer une note (Vue Détail)

L'attribution de la note se fait de manière isolée pour éviter toute erreur de manipulation.
1. Allez sur le profil de l'évaluation en cliquant sur "Voir" (l'icône oeil).
2. Dans le panneau de droite intitulé **Résultat**, un encart "Attribuer une note" est disponible.
3. Saisissez la note sur 100 et validez.
4. Une jauge colorée (Verte, Jaune ou Rouge) apparaîtra pour visualiser le niveau de performance.

> `[Insérer ici la capture d'écran du bloc "Attribuer une note" sur le profil de l'évaluation]`

---

## 9. Module : Paie

*(Note : Ce module est une simulation de registre de paie dans la version actuelle).*

Il permet d'archiver les informations liées aux salaires mensuels.

> `[Insérer ici la capture d'écran de la liste des paies]`

Pour générer une paie :
1. Sélectionnez le mois et l'année.
2. Choisissez l'employé.
3. Le salaire de base remonte automatiquement.
4. Ajoutez les primes (Bonus) ou retenues (Absences).
5. Sauvegardez. Le système calcule le brut et le net estimé.

---

## 10. Module : Formations

Ce module gère le développement des compétences.

> `[Insérer ici la capture d'écran du module Formations]`

- Vous pouvez créer des sessions de formation (Titre, Lieu, Dates).
- Sur la page de détail d'une formation, vous pouvez y **inscrire des participants** (collaborateurs).
- À la fin de la formation, il est possible de pointer leur présence.

---

## 11. Module : Paramètres et Rapports

*(Réservé aux Administrateurs / RH).*

> `[Insérer ici la capture d'écran des paramètres ou d'un rapport PDF]`

- **Paramètres** : Permet de modifier le nom de l'entreprise, le logo, les informations légales.
- **Rapports (Bilan Social)** : Permet de générer des statistiques globales (Masse salariale, répartition hommes/femmes, nombre de recrutements) exportables au format **PDF** ou **Excel**.

---

## 12. Annexes et Résolution de problèmes

### Que faire en cas de mot de passe oublié ?
L'administrateur peut réinitialiser le mot de passe d'un utilisateur en allant dans le module Employés, puis en modifiant les paramètres d'accès de la personne concernée (selon l'implémentation active).

### L'application s'affiche mal sur mon téléphone ?
HRFlowSn est conçu de manière *Responsive* (Adaptative). Sur mobile, la barre de navigation latérale est masquée par défaut. Vous pouvez l'afficher en appuyant sur l'icône "Menu" (les trois lignes horizontales) en haut de l'écran.

---
*Fin du document*
