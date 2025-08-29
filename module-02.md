# Module 2 – Méthodologie de la cartographie des données

## 1. Objectifs pédagogiques

À l’issue de ce module, les étudiants doivent être capables de :

* Décrire les étapes de mise en place d’une cartographie des données
* Identifier et recenser les sources de données d’une organisation
* Classifier les données selon leur sensibilité, criticité et usage
* Documenter les traitements et flux de données entre systèmes
* Relier la cartographie aux processus métiers et aux responsabilités internes
* Utiliser des standards (UML, BPMN, DFD, ArchiMate) pour représenter visuellement la cartographie

---

## 2. Plan de cours détaillé

### Partie A – Étapes principales d’une cartographie

1. **Recensement des sources de données**

   * Bases de données relationnelles (SQL Server, MySQL, PostgreSQL)
   * Bases NoSQL (MongoDB, Cassandra, Redis)
   * Fichiers (CSV, Excel, JSON, logs)
   * APIs internes et externes
   * IoT, capteurs, objets connectés
   * Applications métier (CRM, ERP, outils RH, outils financiers)

2. **Classification des données**

   * Critères de classification :

     * Sensibilité (publique, interne, confidentielle, restreinte)
     * Criticité (impact sur le métier en cas de perte ou d’altération)
     * Usage (IA, reporting, opérationnel, réglementaire)
   * Exemple :

     * Fichier de paie → Données personnelles, Confidentiel, Critique
     * Page catalogue produit → Publique, Faible criticité

3. **Documentation des traitements et flux**

   * Collecte (formulaires, API, batch ETL, flux temps réel Kafka)
   * Transformation (scripts Python, pipeline Spark, jobs ETL)
   * Stockage (bases SQL, data lakes, entrepôts cloud, archives)
   * Restitution (BI, IA, tableaux de bord, reporting réglementaire)
   * Notion de **Data Lineage** : traçabilité de bout en bout d’une donnée (de la collecte à l’usage).

4. **Mise en relation avec les processus métiers**

   * Chaque donnée doit être reliée à un processus métier ou technique.
   * Exemple :

     * Données clients → processus de facturation, marketing, service client.
     * Données capteurs IoT → maintenance prédictive, optimisation énergétique.

---

### Partie B – Outils et méthodes de collecte d’information

1. **Entretiens et questionnaires**

   * Interroger les responsables métiers (RH, finance, logistique).
   * Identifier les flux de données entre départements.
   * Exemple : poser la question “Quelles données utilisez-vous pour établir un reporting mensuel ?”.

2. **Inventaires techniques**

   * Scripts d’exploration de bases de données (SQL `INFORMATION_SCHEMA`, MongoDB `db.stats()`…).
   * Analyse de logs d’applications et serveurs.
   * Détection automatique de métadonnées.

3. **Observation des processus métier**

   * Workflow (comment circulent les données dans une activité donnée).
   * Diagrammes BPMN pour modéliser les flux.

---

### Partie C – Standards et notations de représentation

1. **BPMN (Business Process Model and Notation)**

   * Utilisé pour représenter les processus métiers et leurs données associées.
   * Exemple : processus de commande en ligne (saisie client → validation → paiement → livraison).

2. **UML (Unified Modeling Language)**

   * Diagramme de classes pour représenter les entités et leurs relations.
   * Diagramme d’activités pour illustrer les flux de traitement.

3. **DFD (Data Flow Diagram)**

   * Représentation simple des entrées, traitements, sorties et stockages.
   * Exemple : flux entre CRM, ERP et plateforme e-commerce.

4. **ArchiMate**

   * Standard de modélisation pour représenter les couches métier, application et technique.
   * Utilisé pour la gouvernance SI et l’urbanisation.

---

### Partie D – Travaux pratiques guidés

**Sujet : plateforme e-commerce**

1. Étudiants listent les sources de données :

   * Site web, CRM, ERP, base SQL des produits, API de paiement, fichiers logs.

2. Classification par type et criticité :

   * Données clients → personnelles/confidentielles.
   * Données produits → publiques, internes pour la gestion du stock.
   * Logs serveurs → internes/techniques.

3. Représentation des flux sous forme de **Data Flow Diagram** :

   * Client → \[Formulaire] → Base SQL (commande).
   * Base SQL → \[ERP] → Reporting ventes.
   * Logs serveur → \[SIEM] → Sécurité.

4. Livrable attendu : une première **cartographie méthodologique** documentée (schéma + tableau d’inventaire).

---

## 3. Méthodes pédagogiques

* Alternance théorie et pratique (cours + application sur un cas concret)
* Travail en sous-groupes pour lister les sources et définir les flux
* Utilisation d’outils simples (Draw\.io, PlantUML, Excel) pour modéliser
* Restitution collective et comparaison des résultats

---

## 4. Ressources conseillées

* CNIL – Outil de cartographie RGPD (registre de traitement)
* OMG – Normes BPMN et UML
* The Open Group – Spécifications ArchiMate
* “Data Management Body of Knowledge” (DAMA-DMBOK)

---

## 5. Évaluation du module

* Grille d’évaluation des livrables de groupe :

  * Complétude de l’inventaire des sources (30 %)
  * Pertinence de la classification (20 %)
  * Cohérence du schéma de flux produit (30 %)
  * Présentation orale de la démarche (20 %)
