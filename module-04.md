# Module 4 – Cas d’usage et bonnes pratiques

## 1. Objectifs pédagogiques

À l’issue de ce module, les étudiants doivent être capables de :

* Appliquer la cartographie des données à des cas d’usage concrets (IA, développement logiciel, cybersécurité).
* Identifier les données pertinentes et leur cycle de vie selon les projets.
* Intégrer la cartographie des données dans une démarche de **DataOps / MLOps**.
* Mettre en œuvre des bonnes pratiques pour maintenir une cartographie vivante et conforme.
* Relier les cas d’usage aux exigences réglementaires (RGPD, ISO/IEC 27001, SecNumCloud).

---

## 2. Plan de cours détaillé

### Partie A – Cas d’usage orientés Intelligence Artificielle et Machine Learning

1. **Identification des datasets nécessaires**

   * Données d’entraînement, de validation, de test.
   * Données brutes vs données enrichies (feature engineering).
   * Exemple : modèle de recommandation → logs utilisateurs + historique d’achats + catalogue produits.

2. **Évaluation de la qualité des données**

   * Complétude (pas de valeurs manquantes).
   * Cohérence (formats normalisés).
   * Fraîcheur (actualisation régulière).
   * Exemple : un dataset de détection de fraude devient inutile si les logs ne sont pas collectés en temps réel.

3. **Conformité et anonymisation**

   * Suppression ou masquage des données personnelles sensibles.
   * Techniques : pseudonymisation, hashing, k-anonymity.
   * Exemple : projet IA en santé → anonymiser les dossiers médicaux avant traitement.

---

### Partie B – Cas d’usage orientés Développement logiciel

1. **Microservices et flux de données**

   * Cartographier les interactions entre microservices (ex. Auth, Paiement, Produits).
   * Identifier les dépendances critiques (API, bases partagées).
   * Exemple : un service "Facturation" dépend à la fois du service "Clients" et du service "Produits".

2. **Interopérabilité et APIs**

   * Cartographie des flux API entrants et sortants.
   * Suivi des dépendances avec des fournisseurs tiers (Stripe, PayPal, Open Data).

3. **Intégration CI/CD et DataOps**

   * Intégrer la mise à jour de la cartographie dans le pipeline CI/CD.
   * Exemple : un commit qui ajoute une nouvelle colonne dans une base → mise à jour automatique du dictionnaire de données.

---

### Partie C – Cas d’usage orientés Cybersécurité et conformité

1. **Protection des données sensibles**

   * Cartographie = point de départ pour une analyse de risque ISO 27005.
   * Identifier : où sont stockées les données sensibles, qui y accède, quels contrôles existent.

2. **Lien avec le RGPD et la CNIL**

   * Obligation de documenter les traitements et les flux.
   * Exemple : une entreprise qui transfère des données clients vers un fournisseur cloud → cartographie obligatoire pour prouver la conformité.

3. **Lien avec ISO/IEC 27001 et SecNumCloud**

   * Inventaire des actifs informationnels (Annexe A.8).
   * Classification et gestion du cycle de vie.
   * Exemple : données archivées > 5 ans → suppression ou anonymisation selon la politique interne.

---

### Partie D – Bonnes pratiques de cartographie des données

1. **Approche progressive et itérative**

   * Ne pas chercher la perfection dès le début.
   * Commencer par un périmètre limité (ex. : RH ou e-commerce).

2. **Responsabilités claires**

   * Nommer des **Data Owners** (responsables métier).
   * Nommer des **Data Stewards** (garants de la qualité et documentation).

3. **Cartographie vivante et dynamique**

   * Intégrer la mise à jour dans le cycle de vie du SI.
   * Lier la cartographie aux outils DevOps (Git, CI/CD, monitoring).

4. **Documentation et communication**

   * Centraliser dans un wiki ou un Data Catalog.
   * Former les équipes à l’usage de la cartographie.

---

### Partie E – Étude de cas pratique : Smart City

**Contexte** : une ville connectée veut cartographier ses données pour lancer des services IA.

1. **Sources de données**

   * IoT (capteurs pollution, trafic, éclairage).
   * Données publiques (open data SIG).
   * Données internes (ERP de la mairie, RH).
   * Données sensibles (vidéosurveillance, données citoyennes).

2. **Flux identifiés**

   * Capteurs → API IoT → Data Lake.
   * Data Lake → Algorithmes IA (trafic prédictif, consommation énergie).
   * Résultats IA → Tableau de bord municipal.

3. **Bonnes pratiques appliquées**

   * Anonymisation des données citoyennes.
   * Classification des données sensibles.
   * Mise en place d’un Data Catalog pour documenter toutes les sources.

**Livrable attendu** : une cartographie visuelle (DFD ou UML) + un dictionnaire des données sensibles.

---

## 3. Méthodes pédagogiques

* Présentation théorique des cas d’usage.
* Travail en groupes sur l’étude de cas (Smart City ou e-commerce).
* Restitution avec schémas et tableaux.
* Comparaison des solutions proposées par les groupes.

---

## 4. Ressources conseillées

* CNIL – Études de cas de cartographie RGPD
* ISO/IEC 27005 – Analyse de risque appliquée à la donnée
* Ouvrage DAMA-DMBOK (chapitres Data Governance et Data Architecture)
* Rapports Gartner sur DataOps et MLOps

---

## 5. Évaluation du module

* Qualité de l’étude de cas rendue (30 %)
* Pertinence de l’identification des sources et flux (30 %)
* Respect des bonnes pratiques (20 %)
* Présentation et justification orale (20 %)

---

Veux-tu que je passe maintenant au **Module 5 – Projet final : Cartographie complète d’un SI**, en le structurant comme un mini-projet avec livrables, grille d’évaluation et soutenance type jury RNCP ?
