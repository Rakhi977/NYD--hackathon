# Where Ancient wisdom collabrating with technology
    A Retrieval-Augmented Generation (RAG) pipeline to answer user queries based on Bhagavad Gita and Patanjali Yoga Sutras. 
# Table of contents
- [Introduction]
- [Features]
- [Installation]
- [Usage]
- [Architecture]
- [Dataset]
- [Results]
- [Contributor]
- [Future work]
  
# Introduction
This project was developed for **The NYD Hackathon 2025**, which challenged participants to build a pipeline that retrieves relevant verses (shlokas) from spiritual texts and generates answers to user queries.


# Features
- Retrieve meaningful verses with high accuracy.
- **JSON-formatted** output for easy integration.
- Configurable similarity score for precision.
- **Multi-source Retrieval**: Retrieves verses from both Bhagavad Gita and Patanjali Yoga Sutras.


# Installation
1.**Install dependencies**:
- Install Python packages using pip
  
2.**Prepare datasets**:
- Download the following CSV files and place them in the root directory:
- `Bhagwad_Gita.csv`
- `Patanjali_Yoga_Sutras_Verses_English_Questions.csv`
  
3.**Run the script**:
- using python main.py `as example`


# Usage

1.**Enter your query**
- run the program and input the query

2.**Getting the result**
- the output will display with the top relevant shlokas
- the result will be saved in `results.json`


# Architecture
the pipeline follows the steps:

- Data Preprocessing
- Embedding Generation
- Information Retrieval (using FAISS)
- Query Expansion and Ranking
- Answer Generation
- JSON Output

## Dataset
The project uses two primary datasets:
- **Bhagavad Gita**: Translation of all chapters.
- **Patanjali Yoga Sutras**: Translations of all verses.

Both datasets are stored as CSV files with columns such as `chapter`, `verse`, `translation`, and `book_name`.

## Results
- **Model**: `all-MiniLM-L6-v2`
- **Sample Query**:
    - Query: what gita says about selflessness?
    - Retrieved Verse: "He sees, who sees that all actions are performed solely by Nature and that the Self is without action."`
 
# Contributors
This project was developed by the following team members during the NYD Hackathon 2025:
- Rakhi
- Anjali Yadav
- Piyush Gautam

# Future work
- Fine-tune the Sentence Transformer model for more accurate retrieval.
- Incorporate additional spiritual texts.
- Deploy the project as a web app for public access.
- Optimize the pipeline for faster query processing.
