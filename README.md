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

- 
# Installation
1.**Install dependencies**:
- Install Python packages using pip
  
2.**Prepare datasets**:
- Download the following CSV files and place them in the root directory:
- `Bhagwad_Gita.csv`
- `Patanjali_Yoga_Sutras_Verses_English_Questions.csv`
  
3.**Run the script**:
- named as python main.py


# Usage

1.**Enter your query**
-run the program and input the query
`Enter your query: What gita says about selflessness?`

2.**Getting the result**
- the output will display with the top relevant shlokas
json output
   {
    "query": "what gita says about selflessness?",
    "results": [
        {
            "text": "He sees, who sees that all actions are performed solely by Nature and that the Self is without action.",
            "chapter": 13,
            "verse": 29,
            "score": 0.9530283212661743
        },
        {
            "text": "But for that man who rejoices only in the Self, who is satisfied with the Self and is content in the Self alone, indeed there is nothing to do.",
            "chapter": 3,
            "verse": 17,
            "score": 0.9996389150619507
        },
        {
            "text": "With the self unattached to external contacts, he finds happiness in the Self; with the self engaged in the meditation of Brahman, he attains endless happiness.",
            "chapter": 5,
            "verse": 21,
            "score": 0.9997164607048035
        }
    ]

   
-the result will be saved in `results.json`


# Architecture
the pipeline follows the steps:

`1.Data Preprocessing
2.Embedding Generation
3.Information Retrieval (using FAISS)
4.Query Expansion and Ranking
5.Answer Generation
6.JSON Output`

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
