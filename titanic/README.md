# 🚢 Projet Machine Learning : Prédiction de la Survie du Titanic

## 📋 Description du Projet

Ce projet a pour objectif de prédire la survie des passagers du Titanic en utilisant des algorithmes de Machine Learning. Il s'agit d'un problème de **classification binaire supervisée** basé sur les données réelles du naufrage du Titanic.

**Variable cible** : `Survived` (0 = Décédé, 1 = Survécu)

**Dataset** : [Titanic - Machine Learning from Disaster (Kaggle)](https://www.kaggle.com/c/titanic)

---

## 🎯 Objectifs

- Analyser les facteurs qui ont influencé la survie des passagers
- Construire et comparer plusieurs modèles de Machine Learning
- Prédire la probabilité de survie en fonction des caractéristiques des passagers
- Respecter le workflow complet d'un projet Machine Learning

---

## 📁 Structure du Projet

```
titanic/
├── README.md
├── data/
│   ├── train.csv                 # jeu d'entraînement
│   ├── test.csv                  # jeu de test (Kaggle)
│   └── gender_submission.csv     # exemple de soumission Kaggle
├── notebooks/
│   └── titanic_survival_prediction.ipynb   # notebook principal
└── outputs/
    └── submission.csv            # prédictions générées par le notebook
```

---

## 🔧 Installation et Configuration

### Prérequis

- Python 3.8 ou supérieur
- Jupyter Notebook ou JupyterLab
- pip (gestionnaire de paquets Python)

### Étape 1 : Cloner ou télécharger le projet

Téléchargez tous les fichiers du projet dans un même dossier.

### Étape 2 : Installer les dépendances

Ouvrez un terminal dans le dossier du projet et exécutez :

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

**OU** si vous avez le fichier `requirements.txt` :

```bash
pip install -r requirements.txt
```

### Étape 3 : Télécharger le dataset

1. Allez sur [Kaggle - Titanic Dataset](https://www.kaggle.com/c/titanic/data)
2. Téléchargez `train.csv` et `test.csv`
3. Placez-les dans `data/` (déjà inclus dans ce dépôt)

---

## 🚀 Utilisation

### Lancer le notebook

1. Ouvrez un terminal dans le dossier `notebooks/` (les chemins sont relatifs à ce dossier)
2. Lancez Jupyter Notebook :

```bash
jupyter notebook
```

3. Dans l'interface qui s'ouvre dans votre navigateur, cliquez sur `titanic_survival_prediction.ipynb`

### Exécuter le code

**Option 1 - Exécution complète** :
- Dans le menu Jupyter : `Cell` → `Run All`
- Toutes les cellules s'exécuteront dans l'ordre

**Option 2 - Exécution pas à pas** :
- Cliquez sur une cellule de code
- Appuyez sur `Shift + Enter` pour l'exécuter
- Passez à la cellule suivante

### Ordre d'exécution recommandé

Les cellules doivent être exécutées **dans l'ordre** car elles dépendent les unes des autres :

1. **Import des bibliothèques** (obligatoire en premier)
2. **Chargement des données** (vérifiez que `data/train.csv` est présent)
3. **Analyse exploratoire** (comprendre les données)
4. **Nettoyage des données** (gérer les valeurs manquantes)
5. **Préparation des données** (encodage, split)
6. **Entraînement des modèles** (5 algorithmes différents)
7. **Évaluation** (comparaison des performances)
8. **Conclusion** (synthèse des résultats)

---

## 🧩 Organisation du notebook (12 phases)

### **Phase 1 : Compréhension du problème**
- Définition des objectifs du projet  
- Identification de la variable cible  
- Détermination du type de problème Machine Learning  

---

### **Phase 2 : Compréhension des données**
- Chargement du dataset  
- Aperçu global des données (shape, head, info)  
- Description des variables  

---

### **Phase 3 : Analyse exploratoire des données (EDA)**
- Statistiques descriptives  
- Visualisations  
- Analyse des corrélations entre les variables  

---

### **Phase 4 : Nettoyage des données**
- Traitement des valeurs manquantes  
- Suppression des colonnes inutiles  
- Vérification de la cohérence des données  

---

### **Phase 5 : Préparation des données**
- Encodage des variables catégorielles  
- Normalisation / standardisation si nécessaire  
- Vérification finale du dataset  

---

### **Phase 6 : Construction du jeu de données ML**
- Séparation des features et de la variable cible  
- Découpage du dataset en jeux d’entraînement et de test (80 % / 20 %)  

---

### **Phase 7 : Modélisation**
Les algorithmes de classification suivants sont implémentés :
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)  

---

### **Phase 8 : Entraînement des modèles**
- Entraînement de chaque modèle sur le jeu d’entraînement  
- Ajustement des paramètres de base  

---

### **Phase 9 : Prédiction**
- Génération des prédictions sur le jeu de test  
- Comparaison des résultats entre les modèles  

---

### **Phase 10 : Évaluation des performances**
- Accuracy  
- Matrice de confusion  
- Rapport de classification (precision, recall, F1-score)  

---

### **Phase 11 : Interprétation et analyse critique**
- Identification des variables influentes  
- Analyse comparative des modèles  
- Limites et points faibles du projet  

---

### **Phase 12 : Conclusion et perspectives**
- Synthèse des résultats obtenus  
- Choix du modèle le plus performant  
- Propositions d’améliorations futures  
- Compétences acquises  

---

## 📈 Résultats Attendus

Les modèles atteignent généralement une **accuracy de 80-85%**.

**Facteurs clés de survie identifiés** :
- 👩 **Sexe** : Les femmes avaient beaucoup plus de chances de survivre
- 🎩 **Classe** : Les passagers de 1ère classe avaient plus de chances
- 👶 **Âge** : Les enfants avaient plus de chances de survivre

**Meilleur modèle** : Généralement Random Forest ou Logistic Regression

---

## 🛠️ Technologies Utilisées

| Bibliothèque | Version | Utilisation |
|--------------|---------|-------------|
| **Python** | 3.8+ | Langage de programmation |
| **Pandas** | 1.3+ | Manipulation de données |
| **NumPy** | 1.21+ | Calculs numériques |
| **Matplotlib** | 3.4+ | Visualisation de données |
| **Seaborn** | 0.11+ | Visualisation statistique |
| **Scikit-learn** | 1.0+ | Algorithmes de Machine Learning |
| **Jupyter** | Latest | Environnement de développement |

---

## 🐛 Résolution des Problèmes Courants

### Erreur : "FileNotFoundError: train.csv"
**Solution** : Assurez-vous que le fichier `train.csv` est dans `titanic/data/` et lancez Jupyter depuis `titanic/notebooks/`.

### Erreur : "ModuleNotFoundError: No module named 'pandas'"
**Solution** : Installez les dépendances avec `pip install pandas numpy matplotlib seaborn scikit-learn`

### Erreur : "ValueError: could not convert string to float"
**Solution** : Exécutez toutes les cellules dans l'ordre depuis le début (`Cell` → `Run All`)

### Les graphiques ne s'affichent pas
**Solution** : Vérifiez que la ligne `%matplotlib inline` est présente dans la cellule d'import

---

## 📚 Ressources et Références

- [Documentation Scikit-learn](https://scikit-learn.org/)
- [Documentation Pandas](https://pandas.pydata.org/)
- [Documentation Seaborn](https://seaborn.pydata.org/)
- [Kaggle - Titanic Competition](https://www.kaggle.com/c/titanic)
- [Encyclopedia Titanica](https://www.encyclopedia-titanica.org/) - Informations historiques

---

## 🎓 Compétences Développées

### Compétences techniques
- ✅ Manipulation de données avec Pandas
- ✅ Visualisation avec Matplotlib et Seaborn
- ✅ Prétraitement des données (nettoyage, encodage)
- ✅ Implémentation d'algorithmes de classification
- ✅ Évaluation et comparaison de modèles ML

### Compétences méthodologiques
- ✅ Workflow complet d'un projet Machine Learning
- ✅ Analyse exploratoire de données (EDA)
- ✅ Techniques de validation et d'évaluation
- ✅ Identification des limites et biais
- ✅ Documentation et présentation de résultats

---


## 👥 Auteur

**Projet réalisé par :** HAJAR BELLAFROUH 
**Date :** Février 2026  
**Contexte :** Projet d'Apprentissage Automatique  
**Établissement :** ENSA Khouribga

---

## 📄 Licence

Ce projet est réalisé à des fins éducatives dans le cadre d'un cours de Machine Learning.

Dataset source : [Kaggle - Titanic Dataset](https://www.kaggle.com/c/titanic) (Licence publique)

---


## ⭐ Remerciements

- Kaggle pour la mise à disposition du dataset
- Les enseignants du cours d'Apprentissage Automatique

---

**Dernière mise à jour :** Février 2026
