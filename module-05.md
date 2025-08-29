# Module 5 – Projet final : Cartographie complète d’un Système d’Information

## 1. Objectifs pédagogiques

À l’issue de ce module, les étudiants doivent être capables de :

* Réaliser une **cartographie complète** d’un SI à partir d’un cas réel ou fictif.
* Combiner les méthodes apprises (inventaire, classification, schémas, Data Catalog).
* Identifier les enjeux IA, développement, cybersécurité et conformité réglementaire.
* Produire des **livrables exploitables** (inventaire, dictionnaire, schémas, analyse).
* Présenter et défendre leur travail devant un jury (mise en situation RNCP).

---

## 2. Contexte du projet

L’entreprise (réelle ou fictive) choisie par les étudiants doit disposer :

* d’un **système d’information multi-sources** (CRM, ERP, site web, bases SQL/NoSQL, APIs, fichiers, logs, IoT…) ;
* de **processus métiers identifiés** (ex. e-commerce, université, smart city, start-up IA) ;
* de **contraintes réglementaires** (RGPD, ISO/IEC 27001).

Chaque groupe devra construire une **cartographie des données** adaptée à ce contexte et documentée pour être présentée à la direction d’une entreprise.

---

## 3. Étapes du projet

### Étape 1 – Recensement et inventaire

* Identifier toutes les sources de données (bases, fichiers, APIs, capteurs).
* Produire un **tableau d’inventaire** comprenant :

  * Source / Système
  * Type de données
  * Métadonnées associées
  * Sensibilité et classification
  * Propriétaire de la donnée (Data Owner)

### Étape 2 – Classification et cycle de vie

* Définir le niveau de sensibilité : Publique, Interne, Confidentielle, Restreinte.
* Définir le cycle de vie de chaque donnée : création → utilisation → stockage → archivage/suppression.

### Étape 3 – Documentation des flux

* Identifier les flux de collecte, transformation, stockage et restitution.
* Décrire les traitements (ETL, API, batch, temps réel).
* Documenter la **traçabilité (Data Lineage)** des données critiques.

### Étape 4 – Schémas et représentation graphique

* Produire au minimum deux représentations :

  * **Diagramme DFD (Data Flow Diagram)** pour les flux.
  * **Diagramme UML ou ArchiMate** pour l’architecture technique.
* Outils conseillés : Draw\.io, PlantUML, Archi, DBeaver, SchemaSpy.

### Étape 5 – Conformité et risques

* Identifier les données personnelles au regard du RGPD.
* Vérifier la conformité ISO/IEC 27001 (Annexe A.8 et A.18).
* Réaliser une **mini-analyse de risques** :

  * Risques de fuite, perte, corruption, non-conformité.
  * Contre-mesures proposées (chiffrement, anonymisation, PRA/PCA).

### Étape 6 – Livrables et restitution

* Dossier écrit structuré :

  1. Contexte et périmètre
  2. Inventaire des données (tableau)
  3. Classification et cycle de vie
  4. Schémas et cartographies
  5. Analyse conformité et risques
  6. Recommandations et plan d’action
* Présentation orale (15–20 minutes) devant jury.

---

## 4. Livrables attendus

1. **Tableau d’inventaire des données** (Excel ou CSV).
2. **Mini Data Catalog** avec description et classification.
3. **Schémas visuels** (DFD + UML/ArchiMate).
4. **Dossier écrit complet** (rapport).
5. **Présentation orale** avec slides (PowerPoint/Keynote/Google Slides).

---

## 5. Grille d’évaluation (RNCP)

| Critère                              | Pondération | Description                                                          |
| ------------------------------------ | ----------- | -------------------------------------------------------------------- |
| Inventaire des sources et complétude | 20 %        | Qualité du tableau d’inventaire, identification correcte des données |
| Classification et cycle de vie       | 15 %        | Pertinence de la classification et gestion des données sensibles     |
| Schémas et cartographie              | 25 %        | Clarté, exhaustivité, lisibilité, standards utilisés                 |
| Conformité et analyse de risques     | 20 %        | Prise en compte RGPD, ISO, sécurité et risques                       |
| Dossier écrit                        | 10 %        | Structure, rigueur, références                                       |
| Présentation orale                   | 10 %        | Clarté, maîtrise, capacité à défendre les choix                      |

---

## 6. Méthodes pédagogiques

* Travail en groupes (3 à 5 étudiants).
* Encadrement par l’enseignant (coaching, validation d’étapes).
* Soutenance finale type RNCP.

---

## 7. Ressources conseillées

* CNIL – Guide pratique de la cartographie des données
* ISO/IEC 27001 et 27005 (actifs et analyse de risques)
* Outil Draw\.io (pour DFD, UML, BPMN)
* DAMA-DMBOK – Data Management Book of Knowledge
* Documentation Collibra / Talend pour exemples de Data Catalog

---

👉 Veux-tu que je prépare un **exemple de projet final complet** (inventaire en tableau + schéma DFD + analyse conformité) que tes étudiants pourraient utiliser comme **modèle corrigé** pour comprendre les attentes ?
