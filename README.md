### **Détection de faux billets – Classification et Analyse géométrique avancée**

*Dans les confins de l'espace intergalactique, l'Organisation Nationale de Lutte contre le Faux-Monnayage (ONCFM) poursuit une quête héroïque : protéger l'intégrité de la monnaie galactique. Leur mission ? Construire un algorithme capable de distinguer les vrais billets des faux à partir de leurs caractéristiques géométriques. Grâce à l'ingéniosité des algorithmes et des méthodes d'analyse, l'ONCFM parviendra à vaincre les menaces de la contrefaçon.*

---

### **Contexte du projet**
Le projet consiste à identifier les faux billets à partir des dimensions géométriques des billets en euros, en appliquant des algorithmes de machine learning. L’objectif est de développer un modèle de classification robuste qui permet de prédire la nature d’un billet, vrai ou faux, en se basant sur ses six caractéristiques géométriques (longueur, hauteur, marges et diagonale).

---

### **Approche technique et outils utilisés**
Le projet se base sur plusieurs techniques d'analyse, incluant l’analyse descriptive des données, la régression, les modèles de machine learning, et diverses métriques d’évaluation.

#### **1. Analyse descriptive des dimensions des billets**
L'analyse descriptive initiale comprend la distribution des dimensions des billets, une première étape cruciale pour comprendre les différences subtiles entre les vrais et les faux billets. Des histogrammes et des boîtes à moustaches ont été utilisés pour observer la distribution des variables comme la longueur et la hauteur. 

- **Paires de corrélation et coefficients de corrélation** : J'ai calculé les coefficients de corrélation pour évaluer les relations entre les dimensions géométriques, visualisées sous forme de matrice de corrélation.
  
---

### **2. Prétraitement des données**
Pour gérer les valeurs manquantes, j'ai utilisé l’imputation par **KNN (K-nearest neighbors)**, permettant de compléter les données avec les valeurs les plus proches en fonction des dimensions disponibles.

---

### **3. Modélisation et Algorithmes**
J'ai mis en œuvre plusieurs modèles d'apprentissage supervisé et non supervisé, avec une analyse comparative de leurs performances.

#### **a. Régression Logistique et Régression Linéaire**
La **régression logistique** a été utilisée pour prédire la classe du billet (vrai ou faux), tandis que la **régression linéaire** a permis de tester la relation entre les dimensions géométriques et la nature du billet.

- **F-statistic et P-value** : J'ai vérifié la significativité des modèles avec des tests statistiques pour évaluer la validité des coefficients et leur impact sur la classification.
- **R² et résidus** : Le coefficient de détermination R² a été calculé pour mesurer la qualité du modèle, et l’analyse des résidus a permis de vérifier l’adéquation du modèle (distribution des résidus étudiée via des graphiques).
  
#### **b. Méthodes de Machine Learning**
Plusieurs algorithmes ont été testés, avec validation croisée pour évaluer leur performance.

- **Scores de validation croisée** : La validation croisée a permis d'évaluer la robustesse des modèles sur des échantillons indépendants. Les modèles testés incluent la **régression polynomiale**, la **Forêt Aléatoire**, **Ridge**, et **Lasso**.
  
  - **Régression Polynomiale (R²)** : Ajustement des modèles pour capturer les relations non-linéaires entre les dimensions géométriques.
  - **Forêt Aléatoire (R²)** : Utilisation d'arbres de décision pour classer les billets en vrais ou faux. Les scores R² de validation croisée ont permis de mesurer la précision du modèle.
  - **Ridge (R²)** et **Lasso (R²)** : Régressions pénalisées pour minimiser le surajustement, avec des scores R² compétitifs.


### **4. Évaluation des modèles**
Les performances des différents modèles ont été évaluées avec des métriques claires :

- **Matrice de confusion** : Pour chaque modèle, la matrice de confusion a été calculée pour visualiser les vrais positifs, faux positifs, vrais négatifs, et faux négatifs.
  
- **Arbre de décision** : Un modèle d’arbre de décision a été implémenté pour mieux comprendre les décisions prises par l'algorithme, en visualisant les critères de segmentation des billets.
  
- **Nombre de composantes et variance (ACP)** : L’Analyse en Composantes Principales (ACP) a été utilisée pour réduire la dimensionnalité des données et déterminer combien de composantes expliquent la majeure partie de la variance dans les données.

- **Variance Inflation Factor (VIF)** : J'ai vérifié la multicolinéarité des variables grâce au VIF, afin de m'assurer qu'aucune variable n'était excessivement corrélée avec une autre, garantissant ainsi un modèle robuste et interprétable.

---

### **Résultats et Recommandations**
Après comparaison des différentes approches, la régression logistique et la Forêt Aléatoire ont montré les meilleures performances en termes de prédiction et de robustesse, avec des scores de validation croisée supérieurs à 90% de précision. La régression linéaire a révélé des informations intéressantes sur les relations entre les dimensions géométriques, tandis que le clustering avec K-means a permis d'identifier des segments naturels dans les données.

*Dans cette odyssée intergalactique, l’ONCFM a désormais à sa disposition des algorithmes puissants, capables de protéger la monnaie contre les faux billets, garantissant ainsi la stabilité économique des systèmes solaires lointains.*

*(Fond spatial avec des GIFs interactifs illustrant les étapes du projet : exploration des données, matrices de confusion, arbre de décision, et analyse des résidus.)*
