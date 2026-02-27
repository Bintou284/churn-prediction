# churn-prediction 

## Analyse et Prédiction du Taux de Désabonnement des Clients Télécom  

---

## 📌 Aperçu  
Ce projet explore un ensemble de données de clients d'une entreprise de télécommunications afin d'identifier les facteurs influençant le taux de désabonnement (*churn*) et de prédire les clients susceptibles de quitter l'entreprise.  

Il repose sur :  
- Une analyse exploratoire des données (**EDA**) approfondie  
- La mise en œuvre de modèles prédictifs d’apprentissage automatique  

---

## 🎯 Objectifs  

- Analyser les caractéristiques démographiques, les contrats et les services souscrits par les clients  
- Identifier les corrélations entre ces variables et le taux de désabonnement  
- Développer et évaluer des modèles prédictifs pour anticiper le *churn*  

---

## 📊 Données  

Le jeu de données utilisé est :  

`WA_Fn-UseC_-Telco-Customer-Churn.csv`

Il inclut :

### 🔹 Démographie
- Genre  
- Senior (oui/non)  
- Partenaire  
- Personnes à charge  

### 🔹 Compte client
- Durée d’abonnement (*tenure*)  
- Type de contrat  
- Frais mensuels  
- Frais totaux  

### 🔹 Services
- Téléphone  
- Internet  
- Sécurité en ligne  
- Assistance technique  
- Etc.  

### 🔹 Variable cible
- `Churn` (Oui / Non)  

---

## 🛠 Structure du projet  

### 1️⃣ Nettoyage des données  

- Conversion de `TotalCharges` en type numérique  
- Suppression des 11 valeurs manquantes  
- Encodage des variables catégoriques avec `pd.get_dummies()`  

---

### 2️⃣ Exploration des données (EDA)  

- Visualisations :  
  - Diagrammes en barres  
  - Histogrammes  
  - Boîtes à moustaches  

- Analyse des corrélations entre `Churn` et les variables explicatives  

#### 🔎 Observations clés  

**Corrélation positive avec le churn :**
- Contrats mensuels  
- Absence de sécurité ou d’assistance technique  
- Frais mensuels élevés  

**Corrélation négative avec le churn :**
- Contrats de 2 ans  
- Services DSL  
- Sécurité en ligne  

---

### 3️⃣ Modélisation  

Quatre modèles ont été entraînés et évalués :

| Modèle | Précision |
|--------|-----------|
| Régression logistique | ~80,7 % |
| SVM (noyau linéaire) | ~82 % |
| AdaBoost | ~81 % |
| XGBoost | ~80 % |

Normalisation des données réalisée avec `MinMaxScaler`.

---

## 📦 Dépendances  

### 🐍 Python  
Version 3.x  

### 📚 Bibliothèques  
- `numpy`  
- `pandas`  
- `seaborn`  
- `matplotlib`  
- `scikit-learn`  
- `xgboost`  

Installation :  

```bash
pip install numpy pandas seaborn matplotlib scikit-learn xgboost

## Auteur 
 
Bintou Ba  