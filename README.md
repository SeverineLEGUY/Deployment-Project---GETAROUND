# Deployment-Project---GETAROUND
<img width="406" height="443" alt="image" src="https://github.com/user-attachments/assets/1364224b-299c-4999-83ed-18a9942f256f" />#

**Projet réalisé dans le cadre de la certification Fullstack Data chez Jedha Bootcamp.**  
Ce projet vise à analyser les retards de location de voitures sur la plateforme Getaround, prédire les prix optimaux de location à l’aide du Machine Learning, et déployer une API ainsi qu’un tableau de bord interactif.

---

## 📌 Contexte

Getaround, souvent appelée "l’Airbnb des voitures", permet de louer un véhicule pour quelques heures ou plusieurs jours.  
Cependant, les retards de retour des voitures créent des frictions pour les clients suivants.  
Getaround souhaite donc :

- Évaluer un **seuil de sécurité entre deux locations** pour limiter les conflits.
- Proposer une **optimisation du prix de location** via la Data Science.

---

## 🎯 Objectifs

### 🎯 Objectifs Métier
- Étudier l’impact des retards sur la satisfaction et les annulations.
- Simuler un délai minimum entre deux réservations.
- Fournir des recommandations à l’équipe produit.
- Prévoir un prix de location journalier optimal.

### 🛠️ Objectifs Techniques
- Réaliser une analyse exploratoire (EDA).
- Entraîner un modèle de régression pour prédire les prix.
- Suivre les expériences avec MLflow.
- Développer une API REST avec FastAPI.
- Créer un tableau de bord interactif avec Streamlit.
- Déployer l’ensemble avec Docker sur Hugging Face Spaces.

---

## 📊 Analyse Exploratoire

### Fichier `get_around_delay_analysis.xlsx`
- Analyse des retards (avance, ponctualité, retard).
- Impact des retards sur la réservation suivante.
- Type de check-in (mobile / manuel), durée moyenne des retards.
- Déterminer les seuils de retard



## 🤖 Détermination du Modèle Machine Learning optimal

- Type : Modèle de régression et arbres de décisions
- Cible : `rental_price_per_day`
- Variables : `car_type`, `engine_power`, `fuel`, `mileage`, `connect`, etc.
- Suivi via MLflow (local ou distant sur AWS S3)
- Intégré à une API FastAPI

---

## 🧱 Architecture du Projet

Le projet s'articule autour des composants suivants :

- **Analyse** : Notebook Jupyter pour l'analyse des données.
- **Tableau de bord** : Interface web développée avec Streamlit pour l'exploration interactive des résultats.
- **MLOps** : Utilisation de MLflow pour le suivi des expérimentations et la gestion du cycle de vie du modèle.
- **API** : Construite avec FastAPI pour l'inférence en production.
- **Déploiement** : Conteneurisation de l'API avec Docker pour une portabilité et une fiabilité maximales.

 ## 🔗 Liens Utiles

| Outil / Service            | Description                                         | Lien                                                                 |
|----------------------------|-----------------------------------------------------|----------------------------------------------------------------------|
| 🚀 API FastAPI             | Service de prédiction de prix de location          | [Voir l'API déployée](https://(https://slec-getaroundapi.hf.space/predict))   |
| 📄 Swagger Docs API        | Interface de test de l'endpoint `/predict`         | [API documentation](https://slec-getaroundapi.hf.space/docs) |
| 📊 Dashboard Streamlit     | Analyse EDA + Prédiction prix d'une location       | [Voir le Dashboard](https://huggingface.co/spaces/slec/Site_GetAround)     |



