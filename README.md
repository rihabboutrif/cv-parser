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





