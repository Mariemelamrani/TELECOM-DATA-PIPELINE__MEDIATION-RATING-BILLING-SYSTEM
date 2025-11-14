Telecom Data Pipeline - Mediation, Rating & Billing System

Pipeline Big Data complet pour la gestion des processus de médiation, tarification et facturation dans le secteur télécom.

🎯 Objectifs

Appliquer les concepts Big Data dans un cas industriel

Implémenter la chaîne complète : médiation → tarification → facturation

Traiter de gros volumes de données en temps réel et batch

Détecter et gérer les anomalies et erreurs

🏗️ Architecture

Pipeline principal :

Synthetic Data Generation → Streaming Mediation → Batch Rating → Batch Billing → Reporting & Analytics

💻 Stack Technique

Python

Apache Spark (Batch & Streaming)

Apache Kafka (Ingestion en temps réel)

PostgreSQL (Base de données clients & catalogues)

Docker (Containerisation)

Airflow (Orchestration des workflows)

⚙️ Fonctionnalités

Génération de données synthétiques

Voix, SMS, données

Génération d’anomalies (doublons, champs manquants, données corrompues)

Médiation en streaming

Ingestion via Kafka

Normalisation et validation

Détection des doublons et gestion des erreurs

Tarification batch

Application des règles tarifaires

Gestion des plans produits, promotions et modificateurs temporels/géographiques

Facturation batch

Agrégation par client et cycle de facturation

Application des taxes

Export des factures en JSON, XML ou PDF

Reporting & Analytics

Tableaux de bord de consommation

KPI et monitoring du pipeline

🗂️ Structure des données

Base Clients : profils, abonnements, informations de facturation

Catalogue Produits : services, unités, règles de pricing

Enregistrements : CDR (voix), EDR (data), métadonnées techniques

⚡ Prérequis

Python 3.8+

Apache Spark 3.0+

Apache Kafka 2.8+

PostgreSQL 13+
