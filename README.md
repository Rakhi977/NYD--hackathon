# Where Ancient wisdom collabrating with technology
    A Retrieval-Augmented Generation (RAG) pipeline to answer user queries based on Bhagavad Gita and Patanjali Yoga Sutras. The system retrieves relevant shlokas and generates a summarized response using open-source tools and models.
# Table of Contents
- [Introduction]
- [Features]
- [Installation]
- [Usage]
- [Architecture]
- [Dataset]
- [Results]
- [Contributing]
  
# Introduction
This project was developed for **The NYD Hackathon 2025**, which challenged participants to build a pipeline that retrieves relevant verses (shlokas) from spiritual texts and generates answers to user queries.
# Features
- Retrieve meaningful verses with high accuracy.
- **JSON-formatted** output for easy integration.
- Configurable similarity score for precision.
- **Multi-source Retrieval**: Retrieves verses from both Bhagavad Gita and Patanjali Yoga Sutras.
# Installation
**Install dependencies**:
- Install Python packages using pip
  
**Prepare datasets**:
    Download the following CSV files and place them in the root directory:
    -`Bhagwad_Gita.csv`
    -`Patanjali_Yoga_Sutras_Verses_English_Questions.csv`
