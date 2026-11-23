# NetGuard-ML

Système de détection d'intrusions réseau construit avec Python et scikit-learn.
Le projet part de connexions réseau brutes (durée, protocole, octets échangés,
taux d'erreurs...) et apprend à distinguer le trafic normal des attaques, puis à
identifier le type d'attaque.

## Objectifs

- Détecter si une connexion est **normale** ou **malveillante** (classification binaire)
- Identifier le **type d'attaque** (classification multi-classes)
- Prédire une grandeur continue du trafic (régression)
- Comprendre **quelles mesures comptent vraiment** grâce à la régularisation

## Ce que le projet démontre

- **Prétraitement rigoureux** : valeurs manquantes, encodage des variables
  catégorielles, standardisation, le tout dans un `Pipeline` sans fuite de données
- **Évaluation adaptée aux classes déséquilibrées** : matrice de confusion,
  précision, rappel, F1, courbe ROC et AUC, plutôt que la seule exactitude
- **Comparaison équitable de plusieurs modèles** par validation croisée
  (KNN, régression logistique, arbre de décision)
- **Réglage des hyperparamètres** avec `GridSearchCV` et `RandomizedSearchCV`
- **Réglage du seuil de décision** pour privilégier le rappel : en sécurité,
  rater une attaque coûte plus cher qu'une fausse alerte
- **Régression linéaire, Ridge et Lasso**, avec sélection de caractéristiques

## Données

Jeu de données NSL-KDD (connexions réseau étiquetées : normal ou type d'attaque).

## Stack

Python · pandas · NumPy · scikit-learn · matplotlib

## Structure

- `notebooks/` : exploration et expérimentations
- `src/` : pipelines et fonctions réutilisables
- `README.md` : méthode, résultats et limites

## Résultats

*(à compléter : meilleur modèle, métriques sur le jeu de test, enseignements)*
