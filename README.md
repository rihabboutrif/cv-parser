# ATS API Candidate
PDF CV Content Extractor

Automatically extract structured information from PDFs such as Education, Experience, Skills, and Personal Details using layout-aware NLP and a fine-tuned spaCy model.

# Overview

This project processes PDFs (CVs/resumes) in a two-step pipeline:

PDF Parsing with spaCy-Layout

Converts PDFs into structured text while preserving sections, headers, and paragraphs.

Returns each paragraph along with its section header.

Section Classification with Fine-Tuned spaCy Model

Each header + paragraph block is merged and fed into a fine-tuned fr_core_news_md model.

The model classifies blocks into categories such as:

Education

Experience

Skills

Projects

Other relevant sections

This allows accurate extraction of structured CV data for analysis or database storage.

# Installation
1️⃣ Create a Virtual Environment

Linux / macOS:

python3 -m venv venv
source venv/bin/activate


Windows (Command Prompt):

python -m venv venv
venv\Scripts\activate


Windows (PowerShell):

python -m venv venv
.\venv\Scripts\Activate.ps1


2️⃣ Install Dependencies

pip install --upgrade pip
pip install spacy spacy-layout
python -m spacy download fr_core_news_md


3️⃣  Model Test  


📌 Merged Text:
 Contact
Phone
98625548
Predicted Category: phone
----------------------------------------
📌 Merged Text:
 Email
rihabboutrif0@gmail.com
Predicted Category: email
----------------------------------------
📌 Merged Text:
 Address
korba,nabeul
Predicted Category: address
----------------------------------------
📌 Merged Text:
 Education
présent Itbs nabeul
3 ème année cycle ingénieur spécialité BI
2020-2023  Issat sousse licence en Système informatique
Predicted Category: education
----------------------------------------
📌 Merged Text:
 Certifications
AWS Academy Machine Learning Foundations
Getting Started with Deep Learning (Nvidea)
Predicted Category: certifications
----------------------------------------
📌 Merged Text:
 Soft Skills
Esprit d'analyse
Travail d'équipe
Résolution de problèmes
Communication
Predicted Category: soft_skills
----------------------------------------
📌 Merged Text:
 Language
Anglais
Francais
Predicted Category: langues
----------------------------------------
📌 Merged Text:
 Rihab Boutrif
É t u d i a n t e   e n   G é n i e   I n f o r m a t i q u e   -   S p é c i a l i t é   B I
Étudiante passionnée par l'analyse de données, l'intelligence artificielle et le développement  logiciel  full  stack.  J'ai  réalisé  des  projets  concrets  en  IA  (NLP,  Deep Learning), BI (Power BI, SSIS), et développement web. Je cherche un stage d'été dans un environnement innovant mêlant data et technologie.
Predicted Category: name
----------------------------------------
📌 Merged Text:
 Experience
Stage d'été 2024
Projet BI - Analyse de la performance commerciale | Power BI
Création  de  tableaux  de  bord  interactifs  pour  Forggith  Pharmaceuticals,  permettant  le suivi de KPIs clés : chiffre d'affaires (YTD, SPLY), performance des équipes, atteinte des objectifs,  répartition  géographique et sectorielle.  Utilisation  avancée  de  Power BI,  DAX, slicers temporels et visualisations dynamiques pour soutenir les décisions des commerciaux, managers et dirigeants.
Predicted Category: projects
----------------------------------------
📌 Merged Text:
 Stage PFE  - Plateforme web pour dentistes
Développement  d'une  plateforme  web  facilitant  la  mise  en  relation  entre  dentistes expérimentés  et  jeunes  diplômés  à  la  recherche  de  remplacements.  Conception  des fonctionnalités d'inscription, de gestion de profils et d'annonces, avec un design responsive.  Projet  réalisé  en  Laravel  9,  MySQL,  Bootstrap  et  jQuery,  en  méthode  Scrum avec GitHub et Trello.
Predicted Category: projects
----------------------------------------
📌 Merged Text:
 Projet ETL - Traitement de données Amazon Prime | SSIS
Intégration d'un dataset brut (films et séries)
Transformation et nettoyage avec SSIS
Chargement dans SQL Server + Dashboard Power BI
Predicted Category: projects
----------------------------------------
📌 Merged Text:
 Détection de Fake News (NLP + ML)
Prétraitement de texte (TF-IDF, Stopwords)
Classification avec Logistic Regression (accuracy 96%)
Sauvegarde du modèle avec Pickle pour future API
Predicted Category: projects
----------------------------------------
📌 Merged Text:
 Classification de races de chiens (Tensorflow)
Projet basé sur un dataset Kaggle de plus de 10 000 images. Conception d'un modèle de classification  d'images  à  l'aide  d'un  CNN  basé  sur  ResNet50V2  .  Déploiement  d'une application  de  prédiction  via  Streamlit,  conteneurisée  avec  Docker  et  hébergée  sur Google Cloud Platform (GKE) pour une mise à l'échelle flexible et professionnelle.
Predicted Category: projects
----------------------------------------
📌 Merged Text:
 Application Web intelligente - Gestion de matériels (ASP.NET Core, Angular, IA)
Développement d'une application web pour la gestion et la réservation de matériels au sein de la faculté, avec une interface pour administrateurs et utilisateurs. Intégration d'un système de discussion en temps réel (SignalR) et d'un chatbot IA basé sur l'API GPT pour automatiser les réponses aux questions fréquentes. Architecture fullstack avec ASP.NET Core  (backend)  et  Angular  (frontend),  authentification  sécurisée,  gestion  des  rôles  et calendrier de disponibilité des ressources.
Predicted Category: projects
----------------------------------------
📌 Merged Text:
 Application RH - Gestion des ressources humaines (Spring Boot & Angular)
Développement  d'une  application  web  de  gestion  RH  avec  authentification  sécurisée (Spring Security), gestion des employés, absences, et départements. Création d'un tableau de  bord  dynamique  avec  Chart.js  pour  visualiser  les  indicateurs  clés  (effectifs,  taux d'absences, répartition  par  département),  mettant  en  valeur  mes  compétences  en développement fullstack et en visualisation de données.
Predicted Category: projects
----------------------------------------
