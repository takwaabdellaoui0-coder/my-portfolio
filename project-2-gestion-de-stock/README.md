# 🖥️ Gestion de Stock — Service Helpdesk (Groupe Médis)

<p align="center">
  <b>Application web de gestion de tickets d'intervention et de stock informatique, développée dans le cadre d'un stage au sein du Groupe Médis / Neapolis Pharma.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/PHP-7.4%2B-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white" alt="jQuery" />
</p>

🔗 **[Live Demo](#)** &nbsp;•&nbsp; 📩 **Code source complet disponible sur demande**

---

## 🎯 Contexte

Réalisé lors d'un stage de perfectionnement au sein du **service Helpdesk du Groupe Médis** (leader pharmaceutique tunisien), ce projet répond à un vrai problème opérationnel : le suivi du matériel informatique (souris, claviers, écrans, etc.) utilisé lors des interventions techniques se faisait entièrement à la main, sans traçabilité ni visibilité sur les quantités disponibles.

**L'objectif** : concevoir une application web centralisant les tickets d'intervention, le stock d'articles, les factures d'achat et les comptes utilisateurs — pour donner au service une vue claire et fiable de son activité.

---

## ✨ Fonctionnalités clés

### 🎫 Gestion des tickets (3 rôles distincts)
- **Utilisateur** : crée, consulte, modifie et suit ses demandes d'intervention
- **Technicien** : traite les tickets (acceptation, mise en attente, annulation avec justification), avec vérification et décrémentation automatique du stock
- **Administrateur** : supervision complète du système

### 📦 Gestion de stock en temps réel
- Suivi des articles avec seuils d'alerte
- Décrémentation automatique lors du traitement d'un ticket
- Notifications en cas de rupture de stock

### 🧾 Gestion des factures
- Création de factures multi-articles avec calcul automatique (HT, TVA, TTC, timbre fiscal)
- Mise à jour automatique du stock à l'enregistrement
- Impression / export PDF

### 👤 Gestion des comptes & rôles
- Authentification sécurisée (hachage des mots de passe)
- Gestion des comptes utilisateurs, techniciens et administrateurs

### 📊 Tableau de bord & statistiques
- Indicateurs clés (articles, stock total, alertes, tickets, utilisateurs)
- Graphiques de répartition des tickets et de consommation par article
- Historique et export des rapports

### 🔔 Système de notifications
- Alertes de stock critique en temps réel
- Historique des annulations avec raison

---

## 🛠️ Stack technique

| Couche | Technologie |
|---|---|
| Backend | PHP (PDO) |
| Base de données | MySQL |
| Frontend | HTML5, CSS3, JavaScript, jQuery |
| Modélisation | UML (StarUML) — diagrammes de cas d'utilisation, séquence, classes |
| Environnement | WAMP |

---

## 🧠 Un défi technique intéressant

Le traitement d'un ticket devait automatiquement vérifier la disponibilité du stock, décrémenter la quantité si suffisante, et bloquer/alerter dans le cas contraire — tout en gardant un historique complet de chaque changement d'état (`ticket_history`) pour garantir la traçabilité des actions du technicien.

La conception a suivi une démarche complète : identification des acteurs → besoins fonctionnels/non-fonctionnels → diagrammes de cas d'utilisation et de séquence → diagramme de classes → implémentation et tests (formulaires, contraintes, cas d'erreur).

---

## 📸 Captures d'écran

*(Ajoute ici quelques screenshots : dashboard admin, espace technicien, formulaire de ticket)*

| Espace Utilisateur | Espace Technicien | Dashboard Admin |
|---|---|---|
| ![](#) | ![](#) | ![](#) |

---

## 📬 Voir le code

Le code source complet (structure des tables, requêtes SQL, logique métier) reste privé pour protéger le travail. Je peux le présenter en détail lors d'un entretien ou sur demande.

**Contact :** *takwaabdellaoui0@gmail.com*
