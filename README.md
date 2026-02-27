Ton projet s’appelle :

> **Comparaison règles SIEM vs IA** 

L’objectif est de comparer deux philosophies de détection de cyberattaques sur le même dataset .

---

# 🎯 1️⃣ Objectif réel du projet

Ce projet n’est pas seulement technique.

Tu dois répondre à une question stratégique :

* Quand les règles classiques suffisent-elles ?
* Quand faut-il passer à l’IA ?
* Quels sont les risques opérationnels ? 

Donc tu compares :

🔹 Approche 1 : Détection basée sur règles (SIEM)
🔹 Approche 2 : Détection basée sur Machine Learning

Sur le même dataset : **CICIDS2017** 

---

# 📊 2️⃣ Partie A – Analyse des données (Obligatoire)

Tu dois d’abord comprendre le dataset .

## ✔ Ce que tu dois expliquer :

### 🔹 a) Description du dataset

* Trafic réseau simulé
* Normal + plusieurs types d’attaques
* Données sous forme de flows réseau

### 🔹 b) Types d’événements

Exemples :

* DoS / DDoS
* PortScan
* Brute Force
* Botnet

---
Tu dois définir des règles simples .

## 🔎 Principe

Une règle = condition logique fixe.

Exemple :

```
IF Flow_Packets/s > 1000 THEN Alert DoS
```

### Tu dois :

1. Définir 3–5 règles simples
2. Expliquer les hypothèses
3. Expliquer les limites

---

## 🎯 Exemple de règles possibles

### 🔹 Règle 1 – Détection DoS

Si :

* Bytes/sec très élevé
* Packet rate élevé

Alors → Alerte DoS

---

### 🔹 Règle 2 – Brute Force

Si :

* Nombre élevé de connexions courtes
* Tentatives répétées
---
---
* Sensible au seuil choisi
* Ne détecte pas les nouvelles attaques
* Beaucoup de faux positifs si mal réglé
* Maintenance manuelle constante

---

# 🤖 4️⃣ Partie C – Approche IA

Tu dois utiliser un modèle ML simple  .

## Étapes :

### 1️⃣ Sélection des features

Exemple :

* Flow Duration
* Total Fwd Packets
* Flow Bytes/s
* Packet Length Mean

---

### 2️⃣ Choix du modèle

Simple modèle recommandé :

* Logistic Regression
* Random Forest
* Decision Tree

Random Forest est souvent le meilleur compromis.

---

### 3️⃣ Entraînement

* Split train/test (70/30)
* Entraîner modèle
* Tester

---

### 4️⃣ Évaluation

Tu dois comparer :

* Accuracy
* Precision
* Recall
* F1-score
* Matrice de confusion

Très important : expliquer les faux positifs et faux négatifs.


## ❗ Limites à expliquer

---

# 📈 5️⃣ Partie D – Comparaison Finale


Alors → Alerte scan

Si :

* Une IP contacte plusieurs ports différents en peu de temps
C’est la partie la plus importante .

Tu compares :

| Critère             | Règles SIEM    | IA          |

### 🔹 Règle 3 – Port Scan

| ------------------- | -------------- | ----------- |

Alors → Alerte brute force

| Couverture attaques | Limitée        | Large       |

# 🛡 3️⃣ Partie B – Approche Règles SIEM (Baseline)

| Faux positifs       | Souvent élevés | Optimisable |
* Infiltration
* Répartition normal vs attaque
* Visualisations (si possible)
| Adaptabilité        | Faible         | Forte       |
| Maintenance         | Manuelle       | Retraining  |
* Web attacks

* Statistiques
| Explicabilité       | Très claire    | Moyenne     |
| Coût                | Faible         | Plus élevé  |

---

# 🏗 6️⃣ Architecture SOC recommandée

Tu dois répondre : 

## 🔥 Recommandation intelligente :

Architecture hybride :

Layer 1 → SIEM règles rapides
Layer 2 → Modèle ML
Layer 3 → Analyste SOC humain

Pourquoi ?

* Les règles filtrent le bruit simple
* L’IA détecte les comportements complexes
* L’humain valide

---

# 🧠 7️⃣ Réponse aux Questions Stratégiques

## Quand les règles suffisent ?

* Environnement stable
* Attaques connues
* Petites entreprises
* Contraintes réglementaires

---

## Quand l’IA devient nécessaire ?

* Volume élevé
* Attaques polymorphes
* Zero-day
* SOC mature

---

# 📦 Structure finale de ton rapport

1. Introduction
2. Description du dataset
3. Implémentation règles SIEM
4. Implémentation ML
5. Résultats
6. Comparaison critique
7. Recommandation SOC
8. Conclusion

---

# 🎓 Ce que ton professeur veut vraiment voir

### 🔹 c) Labels disponibles


✔ Compréhension technique
✔ Capacité d’analyse critique
✔ Vision opérationnelle SOC
✔ Argumentation logique
✔ Discussion sur risques
* BENIGN

👉 Ici tu fais :

---
