### Network security project for phishing data

Objectif :
Détecter automatiquement les sites de phishing à partir d’un ensemble de caractéristiques d’URL, à l’aide d’un modèle de Machine Learning intégré dans une architecture MLOps complète.


🔹 Machine Learning :
Préparation des données : ingestion, validation, transformation.

Entraînement de plusieurs modèles avec GridSearchCV.

Sélection du meilleur modèle.

Sauvegarde du modèle et du pipeline de prétraitement (model.pkl, preprocessor.pkl).

🔹 Suivi des expériences :
Utilisation de MLflow pour tracer les expériences.

Intégration à DagsHub pour une visualisation centralisée.

🔹 API avec FastAPI :
Création d’une API REST pour :

Démarrer un entraînement via /train.

Prédire des résultats à partir d’un CSV via /predict.

Retour des résultats au format tableau HTML.

🔹 Déploiement :
Conteneurisation de l’application FastAPI avec Docker.

Push automatique de l’image sur Amazon ECR via GitHub Actions.

Déploiement automatique sur une instance EC2 à l’aide de CI/CD :

Pull de l’image depuis ECR.

Lancement du conteneur sur le port 8080.

🔹 Stockage :
Artifacts, modèles finaux, et outputs de prédiction envoyés sur Amazon S3.

CI/CD avec GitHub Actions :
CI (Intégration Continue) : tests et vérifications sur chaque push.

CD (Livraison & Déploiement Continu) :

Création de l’image Docker.

Livraison sur ECR.

Déploiement automatique sur EC2 via SSH Docker run.



