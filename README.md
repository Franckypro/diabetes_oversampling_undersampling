# diabetes_oversampling_undersampling

# 🩺 Analyse de Données Médicales - Prédiction du Diabète 🩺

Ce projet vise à analyser les données liées au diabète et à créer un modèle prédictif pour déterminer si une personne est susceptible de développer le diabète. Le modèle utilise l'algorithme K-Nearest Neighbors (KNN) et aborde des techniques de rééchantillonnage comme l'oversampling et l'undersampling pour traiter les déséquilibres dans les données.

## 📦 Packages nécessaires

Le code utilise plusieurs bibliothèques Python pour le traitement des données et la création du modèle :

- `numpy`
- `pandas`
- `sklearn`
- `matplotlib`
- `seaborn`
- `imblearn`

## 📊 Chargement et Exploration des Données

Les données utilisées proviennent d'un fichier CSV, `diabetes.csv`, qui contient les informations suivantes :

- `Glucose`
- `BloodPressure`
- `SkinThickness`
- `Insulin`
- `BMI`
- `DiabetesPedigreeFunction`
- `Age`
- `Outcome` (0 = pas diabétique, 1 = diabétique)

### Nettoyage des données

1. **Suppression des doublons** : Les doublons sont supprimés en fonction de la colonne `Age` en gardant la première occurrence.
2. **Analyse des valeurs manquantes** : Aucune valeur manquante n'est trouvée dans les données.

### Visualisation des Données

- **Distribution des classes** : Un diagramme circulaire est généré pour afficher la répartition des patients diabétiques et non diabétiques.
- **Corrélation entre les variables** : Une carte de chaleur est utilisée pour visualiser la corrélation entre les différentes variables.

## 🔍 Modélisation

### Séparation des Données

Les données sont séparées en variables explicatives (`X`) et cible (`y`). Ensuite, elles sont divisées en ensembles d'entraînement et de test.

### Standardisation

Les données sont standardisées à l'aide de `StandardScaler` pour rendre les différentes caractéristiques comparables.

### Modèle KNN

Un modèle de classification est créé en utilisant l'algorithme K-Nearest Neighbors (KNN). Ensuite, des évaluations de performance sont réalisées à l'aide de la validation croisée et des courbes ROC (Receiver Operating Characteristic).

## ⚖️ Techniques de Rééchantillonnage

### 🛠️ Oversampling (Suréchantillonnage)

L'oversampling est appliqué pour équilibrer les classes en augmentant le nombre d'échantillons de la classe minoritaire. Cela améliore les performances du modèle sur la classe minoritaire.

#### SMOTE

SMOTE (Synthetic Minority Over-sampling Technique) est utilisé pour générer des échantillons synthétiques de la classe minoritaire.

### 📉 Undersampling (Sous-échantillonnage)

L'undersampling est une technique qui consiste à réduire la taille de la classe majoritaire pour équilibrer les classes. Cela peut améliorer la performance du modèle en réduisant le biais de la classe majoritaire.

### Évaluation des Modèles

Les performances du modèle sont évaluées pour les deux scénarios :

- **Base basique (sans rééchantillonnage)**
- **Base oversampled (avec suréchantillonnage)**

## 🚀 Visualisation des Performances

Les résultats des modèles sont comparés à l'aide de l'AUC (Area Under the Curve) sur les ensembles d'entraînement et de test.

### 📈 Exemple de Courbe ROC

Les courbes ROC sont tracées pour les ensembles d'entraînement et de test afin d'évaluer les performances des modèles.

## 📝 Conclusion

Ce projet illustre l'importance du traitement des déséquilibres dans les données pour améliorer les performances des modèles de classification. L'oversampling et l'undersampling sont des techniques puissantes pour gérer ce problème.

### 📅 Étapes suivantes

- Améliorer le modèle avec d'autres techniques de classification.
- Ajouter des fonctionnalités de prédiction en temps réel.

## 📬 Contact

Pour plus d'informations, contactez-moi à : ffouejio@gmail.com

## ✍️ Auteur
Fouejio Francky Joël
