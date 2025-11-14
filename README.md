# Telecom Data Pipeline - Mediation, Rating & Billing System

Un pipeline de données Big Data complet pour la gestion des processus de médiation, tarification et facturation dans l'industrie des télécommunications.

## 📋 Description

Ce projet implémente un pipeline de données simplifié reproduisant les processus critiques d'un opérateur télécom : génération de données d'utilisation, médiation en temps réel, tarification par lot et génération de factures. Le système traite des enregistrements d'utilisation (CDR/EDR) pour produire des factures clients finales.

## 🎯 Objectifs

- **Application pratique** des concepts Big Data dans un cas d'usage industriel
- **Implémentation complète** de la chaîne de valeur télécom
- **Gestion des volumes** importants de données en temps réel et batch
- **Détection et traitement** des erreurs et anomalies

## 🏗️ Architecture du Système

### Composants Principaux
Synthetic Data Generation → Streaming Mediation → Batch Rating → Batch Billing → Reporting & Analytics

### Stack Technique Recommandée

- **Python** - Langage principal
- **Apache Spark** - Traitement batch et streaming
- **Apache Kafka** - Ingestion en temps réel
- **PostgreSQL** - Base de données clients et catalogues
- **Docker** - Containerisation
- **Airflow** - Orchestration des workflows

## 📊 Fonctionnalités

### 1. Génération de Données Synthétiques
- Simulation réaliste des enregistrements d'utilisation télécom
- Types de services : appels voix, SMS, sessions données
- Génération d'anomalies (données corrompues, doublons, champs manquants)
- Contrôle du volume et distribution des services

**Exemple CDR Voix :**
```json
{
    "record_type": "voice",
    "timestamp": "2025-04-18T14:32:15Z",
    "caller_id": "212612345678",
    "callee_id": "212698765432",
    "duration_sec": 180,
    "cell_id": "ALHOCEIMA_23",
    "technology": "3G"
}
2. Médiation en Streaming
Ingestion en temps réel via Kafka

Validation et normalisation des données

Détection et élimination des doublons

Gestion des erreurs (dead letter topics)

Filtrage des enregistrements invalides

3. Moteur de Tarification (Batch)
Application des règles tarifaires complexes

Gestion des plans tarifaires et catalogues produits

Calcul des coûts par service (voix, SMS, données)

Modificateurs temporels (heures pleines/creuses)

Pricing géographique (national/international)

Système de promotions et remises

4. Moteur de Facturation (Batch)
Agrégation des charges par client et cycle de facturation

Gestion des quotas et unités gratuites

Application des taxes et frais réglementaires

Génération des factures (JSON/XML/PDF)

Gestion des cycles de facturation mensuels

5. Reporting et Analytics
Tableaux de bord de consommation

Métriques de revenus et KPI business

Patterns d'utilisation clients

Monitoring des performances du pipeline

🗂️ Structure des Données
Base Clients
Identifiants clients et profils d'abonnement

Plans tarifaires et statuts

Informations de facturation

Catalogue Produits
Services telecom (voix, SMS, données)

Unités de tarification et prix

Règles de pricing avancées

Enregistrements d'Utilisation
CDR (Call Detail Records) pour la voix

EDR (Event Detail Records) pour les données

Métadonnées techniques et business

🚀 Installation et Déploiement
Prérequis
Python 3.8+

Apache Spark 3.0+

Apache Kafka 2.8+

PostgreSQL 13+
