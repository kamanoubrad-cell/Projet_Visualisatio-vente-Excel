# 📊 Sales Dashboard — Analyse des ventes & KPIs sous Excel

> Projet Excel #1 — Série "Data Analyst Toolbox"  
> Manipulation de données de vente, calcul de KPIs et visualisation sur dashboard interactif.

---

## 🎯 Contexte & objectif

Ce projet constitue le **premier volet d'une série** visant à maîtriser les outils essentiels du Data Analyst dans le cadre d'une recherche d'alternance.

L'objectif est de travailler avec des données de vente réelles (format Superstore US) pour :
- Pratiquer l'**extraction et la transformation de données** sous Power Query
- Calculer des **KPIs financiers et commerciaux** via des formules Excel avancées
- Construire un **dashboard visuel** permettant de comprendre la performance du business

> Les formules et techniques utilisées s'inspirent directement de ce qui a été mobilisé lors de stages au **Crédit Mutuel Arkéa** (reporting risques) et chez **ACE Finance** (suivi d'activité, rapprochements).

---

## 📁 Source des données

| Paramètre | Détail |
|---|---|
| **Fichier source** | `Projet_Visualisation-vente_Data_.csv` |
| **Volume** | 9 974 lignes × 22 colonnes |
| **Période** | 2014 – 2017 |
| **Marché** | États-Unis |
| **Nature** | Données de vente retail (commandes clients) |

### Colonnes principales

| Colonne | Description |
|---|---|
| `Order ID` | Identifiant unique de la commande |
| `Order Date / Ship Date` | Dates de commande et d'expédition |
| `Ship Mode` | Mode de livraison (Same Day, First Class, Second Class, Standard) |
| `Customer ID / Name` | Identification client |
| `Segment` | Segment client (Consumer, Corporate, Home Office) |
| `Region / State / City` | Localisation géographique |
| `Category / Sub-Category` | Catégorie produit (Furniture, Office Supplies, Technology) |
| `Sales` | Chiffre d'affaires brut |
| `Quantity` | Quantité commandée |
| `Discount` | Taux de remise appliqué |
| `Profit` | Bénéfice net |
| `Net Revenue` | Chiffre d'affaires net (après remise) |
| `Margin %` | Taux de marge |

---

## 🔧 Structure du projet

### Étape 1 — Extraction des données sous Power Query
- Import du fichier CSV brut
- Nettoyage des types de données (dates, montants, pourcentages)
- Suppression des colonnes inutiles et gestion des valeurs manquantes
- Renommage et standardisation des colonnes
- Chargement dans Excel pour analyse

### Étape 2 — Calcul des KPIs & Tableaux Croisés Dynamiques (TCD)

**KPIs calculés :**

| KPI | Formule / méthode | Intérêt métier |
|---|---|---|
| Chiffre d'affaires total | `SOMME(Sales)` | Vision globale du business |
| Marge nette moyenne | `MOYENNE(Margin %)` | Rentabilité globale |
| Profit total | `SOMME(Profit)` | Performance financière |
| Taux de remise moyen | `MOYENNE(Discount)` | Impact commercial |
| Nombre de commandes | `NB.SI.ENS(...)` | Activité volume |
| CA par catégorie | TCD + `SOMME.SI.ENS` | Analyse produit |
| Marge par segment | TCD + `MOYENNE.SI.ENS` | Analyse client |
| Top produits / régions | TCD trié | Décision stratégique |

**Tableaux Croisés Dynamiques :**
- CA et profit par **catégorie** et **sous-catégorie**
- Performance par **segment client** (Consumer / Corporate / Home Office)
- Analyse par **région** et **état**
- Évolution temporelle **(par année / trimestre)**

### Étape 3 — Dashboard de visualisation

**Graphiques intégrés :**
- 📈 Évolution du CA et du profit dans le temps
- 🥧 Répartition du CA par catégorie de produit
- 📊 Comparaison de la marge par segment client
- 🗺️ Performance par région géographique
- 📉 Impact des remises sur la marge

**Éléments interactifs :**
- Segments (slicers) par année, catégorie, région
- Mise en forme conditionnelle sur les KPIs critiques

---

## 📈 Principaux enseignements

- La catégorie **Technology** génère les marges les plus élevées
- Les **fortes remises** (> 40%) entraînent des marges négatives sur certaines lignes
- Le segment **Consumer** représente le plus grand volume de commandes
- La région **West** domine en chiffre d'affaires

---

## 🛠️ Outils & compétences mobilisées

```
Excel
├── Power Query        → import, nettoyage, transformation des données
├── Formules avancées  → SOMME.SI.ENS, MOYENNE.SI.ENS, NB.SI.ENS, RECHERCHEV
├── TCD                → tableaux croisés dynamiques + segments interactifs
└── Dashboard          → graphiques combinés, mise en forme conditionnelle
```

---

## 🔮 Améliorations prévues

- [ ] Connecter le fichier à **Power BI** pour un dashboard plus interactif
- [ ] Automatiser le calcul des KPIs avec des **macros VBA**
- [ ] Ajouter une analyse de **prévision des ventes** (tendance + saisonnalité)
- [ ] Reproduire l'analyse en **Python (Pandas + Plotly)** pour comparer les approches

---

## 📚 Série "Data Analyst Toolbox"

| # | Projet | Outil | Statut |
|---|---|---|---|
| 1 | Sales Dashboard — KPIs & Visualisation | Excel / Power Query | ✅ Terminé |
| 2 | Analyse de risque de portefeuille | Python (NumPy, Pandas, scipy) | ✅ Terminé |
| 3 | Credit Scoring Model | Python (Scikit-Learn) | 🔜 À venir |
| 4 | NPL Dashboard automatisé | Python (openpyxl, Plotly) | 🔜 À venir |

---

## 👤 Auteur

**Brad Aymeric Feltre Kamanou**  
Étudiant Master Data Management — IÉSEG School of Management  
Ancien stagiaire Risque de Crédit — Crédit Mutuel Arkéa  

> *Projet réalisé en autonomie avec l'appui de Claude (Anthropic) pour débloquer certaines situations techniques.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/ton-profil)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/ton-profil)
