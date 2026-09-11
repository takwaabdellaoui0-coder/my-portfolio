# 🚗 AUTO LOC — Plateforme de Location de Voitures

<p align="center">
  <b>Application web de gestion de location de véhicules, développée avec Symfony dans le cadre d'un projet académique.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Symfony-000000?style=for-the-badge&logo=symfony&logoColor=white" alt="Symfony" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/Twig-B9D9D4?style=for-the-badge&logo=twig&logoColor=black" alt="Twig" />
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap" />
</p>

🔗 **[Live Demo](#)** &nbsp;•&nbsp; 📩 **Code source complet disponible sur demande**

---

## 🎯 Contexte

Les services de location de voitures reposent encore souvent sur des méthodes manuelles (registres papier, fichiers Excel, appels téléphoniques), ce qui entraîne des erreurs, des doubles réservations et un manque de visibilité sur la disponibilité réelle des véhicules.

**AUTO LOC** digitalise ce processus : les clients consultent le catalogue et réservent en ligne, pendant que l'administrateur gère le parc automobile, les utilisateurs et le suivi des paiements — le tout depuis une interface unique et sécurisée.

---

## ✨ Fonctionnalités clés

### 👤 Espace Client
- Inscription / connexion sécurisée
- Consultation du catalogue de véhicules (marque, modèle, catégorie, prix/jour)
- Réservation en ligne avec sélection des dates et lieu de récupération
- Suivi de l'historique des réservations et de leur statut (confirmée, en attente, terminée)
- Paiement lié à la réservation

### 🛠️ Espace Administrateur
- **Tableau de bord** : véhicules disponibles, revenus totaux, réservations actives, clients enregistrés, graphique des revenus mensuels et répartition par catégorie
- **Gestion des véhicules** : ajout, modification, suppression, filtrage par catégorie/disponibilité
- **Gestion des réservations** : vue globale avec statuts (confirmées, en cours, en attente, annulées)
- **Gestion des clients** : liste des utilisateurs, rôles, historique de réservations
- **Gestion des paiements** : suivi des transactions, montants encaissés/en attente
- **Gestion des catégories** de véhicules (Berline, SUV, Luxe...)

### 🔐 Authentification par rôle
Deux parcours de connexion distincts (Admin / Client) avec gestion des accès via le système de rôles de Symfony (`ROLE_ADMIN`, `ROLE_USER`).

---

## 🛠️ Stack technique

| Couche | Technologie |
|---|---|
| Framework | Symfony 8 |
| Base de données | MySQL (via Doctrine ORM) |
| Templating | Twig |
| Frontend | Bootstrap |
| Sécurité | Symfony Security Bundle |

---

## 🧩 Modèle de données (aperçu)

L'application s'articule autour de 5 entités principales : **Utilisateur**, **Voiture**, **CategorieVoiture**, **Réservation** et **Paiement**, avec des relations qui garantissent la cohérence des données — par exemple, chaque réservation est automatiquement liée à un seul paiement, et chaque voiture appartient à une catégorie.

*(Le détail complet du schéma de base de données et des entités reste dans le rapport de projet privé.)*

---

## 🧠 Un point technique intéressant

La séparation stricte des contrôleurs entre `Controller/ADMIN` et `Controller/USER` permet de garder une logique métier claire pour chaque type d'utilisateur, tout en s'appuyant sur le système de rôles de Symfony pour restreindre l'accès aux bonnes interfaces selon le profil connecté.

---

## 📸 Captures d'écran

| Dashboard Admin | Catalogue Client | Réservation |
|---|---|---|
| ![](#) | ![](#) | ![](#) |

---

## 📬 Voir le code

Le code source complet (entités, contrôleurs, logique de réservation et de paiement) reste privé. Je peux le présenter en détail lors d'un entretien ou sur demande.

**Contact :** *(takwaabdellaoui0@gmail.com*
