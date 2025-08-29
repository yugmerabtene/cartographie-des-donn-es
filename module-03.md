# Module 3 – Techniques et outils de cartographie des données

## 1. Objectifs pédagogiques

À la fin du module, les étudiants doivent être capables de :

* Identifier les outils disponibles pour cartographier les données (open source et professionnels)
* Utiliser des outils graphiques (Draw\.io, PlantUML, Archi) pour représenter des flux et des entités
* Automatiser l’inventaire des données et l’extraction de métadonnées à l’aide de scripts et connecteurs
* Comprendre le rôle et l’intérêt d’un **Data Catalog** pour l’IA, le DevOps et la gouvernance des données
* Construire une cartographie semi-automatisée combinant inventaire technique et représentation graphique

---

## 2. Plan de cours détaillé

### Partie A – Panorama des outils de cartographie

1. **Outils graphiques simples (Open Source / gratuits)**

   * **Draw\.io (Diagrams.net)** : idéal pour réaliser des Data Flow Diagrams (DFD), UML et BPMN.
   * **PlantUML** : génération automatique de diagrammes (classes, séquences, DFD) à partir de scripts textuels.
   * **Archi** : outil basé sur le langage ArchiMate, adapté à l’urbanisation du SI.

2. **Outils professionnels (payants ou avancés)**

   * **Talend Data Catalog** : inventaire automatisé et gestion des métadonnées.
   * **Collibra Data Governance** : gouvernance des données à grande échelle.
   * **Atlan, Alation, Informatica** : plateformes spécialisées en Data Catalog et Data Lineage.
   * **Power BI / Tableau** : souvent utilisés pour la visualisation, mais peuvent intégrer des flux de données.

3. **Critères de choix d’un outil**

   * **Taille de l’organisation** (startup vs grand groupe).
   * **Complexité du SI** (bases multiples, microservices, cloud hybride).
   * **Budget et conformité** (RGPD, ISO 27001, SecNumCloud en France).
   * **Niveau d’automatisation souhaité** (manuel, semi-automatisé, full catalog).

---

### Partie B – Automatisation et inventaire technique

1. **Exploration des bases relationnelles**

   * Utiliser SQL via `INFORMATION_SCHEMA` pour inventorier :

     * Tables
     * Colonnes et types
     * Clés primaires et étrangères
   * Exemple :

     ```sql
     SELECT table_name, column_name, data_type
     FROM information_schema.columns
     WHERE table_schema = 'public';
     ```

2. **Exploration des bases NoSQL**

   * MongoDB : commandes `db.stats()`, `db.collection.stats()`
   * Elasticsearch : API `_mapping` pour explorer la structure des index.

3. **Extraction des métadonnées avec Python**

   * Bibliothèques utiles :

     * `sqlalchemy` pour explorer une base SQL
     * `pandas` pour analyser des CSV/JSON
     * `pyodbc` pour interroger divers SGBD
   * Génération d’un dictionnaire de données automatique (export vers Excel ou CSV).

4. **Automatisation de la documentation**

   * Générer des dictionnaires de données avec :

     * Nom du champ
     * Type de donnée
     * Description
     * Source
     * Niveau de sensibilité (Publique / Interne / Confidentiel / Restreint).

---

### Partie C – Data Catalogs et gouvernance des données

1. **Définition**

   * Plateforme centralisée qui référence, documente et gère toutes les données d’une organisation.

2. **Fonctionnalités principales**

   * Recherche et indexation des datasets.
   * Gestion des métadonnées et glossaire.
   * Traçabilité (Data Lineage).
   * Contrôle d’accès et gestion des rôles.

3. **Avantages pour l’IA et le développement**

   * Accélère la recherche et l’accès aux données utiles.
   * Réduit la duplication et les incohérences.
   * Favorise la conformité RGPD et ISO.
   * Facilite la réutilisation et le partage des données entre équipes (Dev, Data, IA).

---

### Partie D – Travaux pratiques guidés

**Exercice 1 : Inventaire d’une base MySQL**

* Connexion via Python + SQLAlchemy.
* Export des métadonnées (tables, colonnes, types) vers un fichier Excel.

**Exercice 2 : Génération automatique de schéma UML**

* Utiliser un outil comme **SchemaSpy** ou **DBeaver**.
* Générer un diagramme des tables et relations.
* Enrichir manuellement le schéma dans Draw\.io avec les flux entre systèmes.

**Exercice 3 : Construction d’un mini Data Catalog**

* Construire un tableau Excel structuré :

  * Nom du champ
  * Type
  * Description
  * Source
  * Sensibilité
  * Usage (IA, reporting, réglementaire)

**Livrables attendus** :

* Inventaire Excel des données
* Schéma UML ou DFD semi-automatisé
* Mini Data Catalog documenté

---

## 3. Méthodes pédagogiques

* Démonstrations pas à pas (scripts + outils)
* Mise en pratique en binômes sur des datasets fournis
* Comparaison des résultats (inventaires, schémas) entre groupes
* Discussion critique : limites des outils manuels vs automatisés

---

## 4. Ressources conseillées

* Outils : Draw\.io, PlantUML, DBeaver, SchemaSpy, Talend Data Catalog, Collibra
* Bibliothèques Python : `pandas`, `sqlalchemy`, `pyodbc`
* Références :

  * DAMA-DMBOK (Data Management Body of Knowledge)
  * CNIL – guides sur la cartographie et la gestion des données
  * Gartner – études sur les Data Catalogs

---

## 5. Évaluation du module

* Qualité de l’inventaire produit (30 %)
* Pertinence du schéma UML/DFD généré et enrichi (30 %)
* Complétude du mini Data Catalog (30 %)
* Présentation orale des résultats (10 %)

---

