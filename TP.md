# TP – Cartographie des données sur un serveur VPS avec application et base SQLite

## Contexte pédagogique

Vous êtes **auditeurs internes** dans une organisation qui héberge une application métier sur un **serveur VPS**.
L’application s’appuie sur une **base SQLite** locale. La direction demande :

1. **Une cartographie complète** des données de l’application.
2. Une **classification** des champs selon leur sensibilité et conformité RGPD.
3. La préparation d’un **rapport d’audit** synthétique présentant le patrimoine informationnel.

---

## Objectifs pédagogiques

* Savoir se connecter à un serveur VPS et explorer une base SQLite.
* Être capable d’identifier les **tables, champs, types et relations**.
* Classer les données selon leur **sensibilité** (publique, interne, confidentielle, restreinte).
* Construire une **cartographie technique et métier** des données (flux, usages, acteurs).
* Produire des livrables conformes à un audit (dictionnaire de données + schéma de flux + rapport).

---

## Pré-requis techniques

* Accès SSH au VPS.
* Application fonctionnelle utilisant SQLite (ex. app web en Python/Flask, Node, Django…).
* Outils :

  * `sqlite3` en ligne de commande.
  * Optionnel : `DBeaver` ou `DB Browser for SQLite` pour une exploration graphique.
  * `draw.io` ou `PlantUML` pour les schémas.

---

## Étapes du TP

### Étape 1 – Connexion et exploration initiale

1. Se connecter en SSH au VPS :

   ```bash
   ssh user@ip_serveur
   ```
2. Localiser la base SQLite (ex : `app.db`).
3. Vérifier les tables présentes :

   ```bash
   sqlite3 app.db
   .tables
   ```

---

### Étape 2 – Inventaire des données

1. Lister la structure de chaque table :

   ```bash
   .schema nom_table
   ```
2. Exporter la structure complète de la base :

   ```bash
   .schema > schema.sql
   ```
3. Analyser :

   * **Champs sensibles** : nom, email, mot de passe, logs d’activité.
   * **Relations** entre tables (clés étrangères, jointures possibles).

**Livrable attendu :** un **tableau d’inventaire** :

| Table  | Champ       | Type    | Description             | Sensibilité  | RGPD | Owner |
| ------ | ----------- | ------- | ----------------------- | ------------ | ---- | ----- |
| users  | id          | INTEGER | Identifiant interne     | Interne      | Non  | IT    |
| users  | email       | TEXT    | Adresse email           | Confidentiel | Oui  | DPO   |
| orders | user\_id    | INTEGER | Lien vers utilisateur   | Interne      | Oui  | Sales |
| logs   | ip\_address | TEXT    | Adresse IP de connexion | Interne      | Oui  | Sec   |

---

### Étape 3 – Classification des données

1. Compléter la matrice de classification (similaire à `classification_template.csv`).
2. Catégoriser :

   * Identifiants directs (nom, email) → **Confidentiel / RGPD**.
   * Quasi-identifiants (IP, date naissance) → **Interne / RGPD**.
   * Identifiants techniques (id interne, timestamp) → **Interne**.
   * Données sensibles (mot de passe, token, logs auth) → **Restreint**.

**Livrable attendu :** un fichier `classification.xlsx` ou `.csv`.

---

### Étape 4 – Cartographie des flux

1. Identifier les **flux de données** :

   * Formulaire web → SQLite (table users).
   * Action utilisateur → SQLite (table orders, logs).
   * API externe ? (paiement, email).
   * Sauvegardes ? (fichiers `.db` copiés).
2. Construire un **schéma DFD** (Data Flow Diagram) :

   * Acteurs (utilisateur, admin, API externe).
   * Systèmes (app web, SQLite, backup, API).
   * Données (users, orders, logs).

---

### Étape 5 – Rapport d’audit

Rédiger un **rapport synthétique (3–5 pages)** avec :

1. **Contexte** (application, VPS, base SQLite).
2. **Inventaire et classification** des données.
3. **Cartographie des flux** (schéma joint).
4. **Risques identifiés** :

   * Pas de chiffrement au repos ?
   * Pas de séparation des environnements ?
   * Quasi-identifiants → risque de ré-identification.
5. **Recommandations** :

   * Activer chiffrement disque (LUKS, VeraCrypt, chiffrement SQLite).
   * Mettre en place sauvegardes chiffrées.
   * Restreindre l’accès SSH et app (pare-feu, MFA).
   * Ajouter une politique de rétention des logs.

---

## Livrables attendus

1. Tableau d’inventaire des données (CSV/Excel).
2. Matrice de classification des champs.
3. Schéma de cartographie (DFD/UML).
4. Rapport d’audit écrit (PDF).
