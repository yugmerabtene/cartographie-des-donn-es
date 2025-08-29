# Module 1 – Introduction à la cartographie des données

## 1. Objectifs pédagogiques

À l’issue du module, les étudiants doivent être capables de :

* Définir clairement la donnée, l’information, la connaissance et la métadonnée
* Expliquer la différence entre une cartographie métier et une cartographie technique
* Identifier les enjeux stratégiques, techniques et réglementaires liés à la cartographie des données
* Comprendre pourquoi la cartographie est une étape indispensable avant tout projet d’IA, de Big Data ou de développement logiciel
* Relier les concepts aux cadres légaux (RGPD, ISO/IEC 27001) et méthodologiques (FAIR Data, Data Governance)
* Produire une première cartographie simple à partir d’un cas concret

---

## 2. Plan de cours détaillé

### Partie A – Définitions et concepts clés

1. **Notion de donnée**

   * Donnée brute : valeur isolée, sans interprétation (ex. : “23”).
   * Information : donnée contextualisée (ex. : “23°C aujourd’hui à Paris”).
   * Connaissance : interprétation utile de l’information (ex. : “Au-delà de 30°C, la consommation électrique augmente de 15 % à cause de la climatisation”).

2. **Métadonnée**

   * Définition : “donnée sur la donnée” (description, contexte, origine).
   * Exemple : un fichier CSV contenant des ventes → les métadonnées sont le format, la date de création, l’auteur, le système source.
   * Importance : permet la traçabilité, la réutilisabilité, et la conformité légale.

3. **Patrimoine informationnel**

   * Les données sont un **actif stratégique** de l’entreprise (comme un brevet ou une machine).
   * Valeur économique : data-driven business (Amazon, Google, Netflix).
   * Risques associés : perte, fuite, corruption, obsolescence.

4. **Cartographie des données**

   * Définition : représentation **visuelle et structurée** des données, de leurs traitements, de leurs flux et de leurs usages.
   * Objectifs :

     * Savoir **où se trouvent les données** (inventaire)
     * Comprendre **comment elles circulent** (flux)
     * Identifier **qui les utilise** (acteurs internes/externes)
     * Définir leur **criticité et leur sensibilité**
   * Distinction :

     * **Cartographie métier** = vue des processus (données RH, ventes, marketing, etc.)
     * **Cartographie technique** = vue SI (bases SQL, fichiers CSV, API, pipelines ETL).

**Exemple concret : plateforme e-commerce**

* Données clients : nom, prénom, adresse, moyens de paiement.
* Données produits : références, prix, stock.
* Données techniques : logs serveur, cookies, API de paiement.
* Données métiers : ventes par catégorie, panier moyen, chiffre d’affaires.

---

### Partie B – Enjeux stratégiques

1. **Vision globale de l’entreprise**

   * Sans cartographie, l’organisation ignore souvent :

     * quelles données elle possède,
     * où elles se trouvent,
     * qui en est responsable.
   * Exemple : une même donnée client peut exister en double (CRM + ERP), générant incohérences et coûts.

2. **Impact pour l’IA et le Big Data**

   * Qualité des modèles IA dépend directement de la qualité des données.
   * La cartographie permet de :

     * Identifier les jeux de données pertinents.
     * Vérifier leur qualité (complétude, exactitude, fraîcheur).
     * Documenter les biais éventuels (données déséquilibrées, échantillons incomplets).
   * Exemple : un modèle de détection de fraude → nécessite de cartographier flux financiers, données clients, logs techniques, historiques de transactions.

3. **Impact pour la cybersécurité**

   * La cartographie permet de localiser les **données sensibles** :

     * Données personnelles (RGPD)
     * Données bancaires (PCI DSS)
     * Données médicales (HDS en France)
   * Utile pour mettre en place un **PRA/PCA** (Plan de Reprise/Continuité).
   * Exemple : savoir que les cartes bancaires sont stockées dans une base isolée → permet d’y appliquer un chiffrement AES-256.

4. **Impact pour le DevOps et le MLOps**

   * La cartographie s’intègre dans les pipelines CI/CD :

     * DataOps = automatisation de l’ingestion, du traitement et du monitoring des données.
     * MLOps = suivi de la qualité des datasets utilisés pour entraîner les modèles IA.
   * Exemple : pipeline GitLab CI/CD qui déploie une API → doit inclure la vérification des flux de données entrants/sortants.

---

### Partie C – Normes et cadre légal

1. **RGPD (Règlement Général sur la Protection des Données)**

   * Obligation de **registre des traitements** (art. 30).
   * Catégorisation : données sensibles (santé, biométriques, orientation politique/religieuse).
   * Exemple : un e-commerce doit cartographier les données personnelles collectées → pour justifier leur usage en cas de contrôle CNIL.

2. **ISO/IEC 27001 (sécurité de l’information)**

   * Annexe A.8 : gestion des actifs informationnels.
   * Exige un **inventaire des données** et leur classification (publique, interne, confidentielle, restreinte).
   * Exemple : classer un fichier de paie comme “Confidentiel”, une page produit comme “Publique”.

3. **FAIR Data Principles**

   * Findable (facile à trouver, ex. catalogues de données).
   * Accessible (droits d’accès clairs).
   * Interoperable (formats standards : CSV, JSON, XML).
   * Reusable (documentées pour être réutilisées).
   * Exemple : un dataset Open Data en CSV, documenté avec son schéma, est FAIR.

---

### Partie D – Mise en pratique : exercice de groupe

**Sujet** : “Cartographier les données d’une université.”

1. **Identification des sources**

   * Étudiants : inscriptions, notes, absences, dossiers administratifs.
   * Enseignants : cours, évaluations, plannings.
   * SI : plateformes Moodle, bases RH, ERP universitaire.

2. **Classement par type**

   * Données personnelles (noms, emails, identifiants).
   * Données opérationnelles (emplois du temps, salles).
   * Données techniques (logs Moodle, connexions VPN).

3. **Première représentation schématique**

   * Bloc 1 : collecte (formulaires, bases RH, APIs).
   * Bloc 2 : traitement (ERP, Moodle, bases SQL).
   * Bloc 3 : stockage (serveurs internes, cloud, sauvegardes).

**Livrable attendu** : une ébauche de cartographie simple avec **3 colonnes (collecte – traitement – stockage)**.

---

## 3. Méthodes pédagogiques

* Cours magistral avec exemples concrets (entreprise, université, e-commerce)
* Discussions guidées sur les risques et opportunités
* Travaux de groupe pour produire une première cartographie
* Mise en commun et correction collective

---

## 4. Ressources conseillées

* CNIL – Guide pratique de la cartographie des données
* ISO/IEC 27001 – Norme internationale (Annexe A.8)
* FAIR Principles – [www.go-fair.org](http://www.go-fair.org)
* Article : “Data Governance and Data Management in AI Systems” (Springer, 2021)

---

## 5. Évaluation du module

* Participation active au brainstorming et à l’exercice collectif
* Capacité à identifier correctement les sources et types de données
* Production d’un premier schéma de cartographie simplifié
* Quiz court en fin de module (5 à 10 questions)

---

Veux-tu que je développe le **contenu du quiz de fin de module** (questions + réponses), pour que tu puisses l’utiliser directement avec tes étudiants ?
