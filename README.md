# Système de Gestion Hospitalière

Ce projet est une application web Flask conçue pour gérer les patients et le personnel médical d'un hôpital de campagne. Il a été développé dans le cadre d'un projet étudiant pour démontrer la mise en œuvre des concepts de développement web et de gestion de base de données.

## Fonctionnalités

- **Gestion des utilisateurs**
  - Système d'authentification pour les médecins et administrateurs
  - Différents niveaux d'accès (médecin, administrateur)
  - Gestion des sessions utilisateurs

- **Gestion des patients**
  - Ajout et suivi des patients
  - Gestion des traitements
  - Suivi des symptômes
  - État actif/inactif des patients
  - Attribution des salles

- **Interface administrative**
  - Ajout de nouveaux médecins (réservé aux administrateurs)
  - Gestion des permissions

## Technologies utilisées

- **Backend**
  - Python 3.x
  - Flask 3.0.3
  - SQLAlchemy 3.1.1
  - Flask-WTF 1.2.1

- **Frontend**
  - HTML5
  - Tailwind CSS
  - JavaScript

- **Base de données**
  - SQLite

## Installation

1. Cloner le repository
```bash
git clone https://github.com/votre-username/hopital-campagne.git
cd hopital-campagne
```

2. Créer un environnement virtuel
```bash
python -m venv venv
source venv/bin/activate  # Pour Linux/Mac
venv\Scripts\activate     # Pour Windows
```

3. Installer les dépendances
```bash
pip install -r requirements.txt
```

4. Initialiser la base de données
```bash
python create_user.py
```

5. Lancer l'application
```bash
python app.py
```

## Configuration

Les paramètres de configuration se trouvent dans le fichier `config.py`. Assurez-vous de modifier la `SECRET_KEY` avant le déploiement en production.

## Identifiants par défaut

L'application est initialisée avec deux comptes :

- **Administrateur**
  - Email : admin@mail.hopital-h6.net
  - Mot de passe : tpRT9025

- **Médecin**
  - Email : medecin@mail.hopital-h6.net
  - Mot de passe : tpRT9025

## Structure du projet

```
hopital-campagne/
├── app.py              # Point d'entrée de l'application
├── config.py           # Configuration de l'application
├── models.py           # Modèles de base de données
├── forms.py            # Formulaires WTForms
├── routes.py           # Routes de l'application
├── decorators.py       # Décorateurs personnalisés
├── requirements.txt    # Dépendances du projet
└── templates/          # Templates HTML
    ├── base.html
    ├── index.html
    └── ...
```

## Sécurité

- Mots de passe hashés avec Werkzeug Security
- Protection CSRF sur tous les formulaires
- Contrôle d'accès basé sur les rôles
- Sessions sécurisées

## Auteur

Réalisé avec ❤️ par Locqmen HAMDI - Projet réalisé dans le cadre du cours de la SAé 502 en 3ème année de BUT R&T
