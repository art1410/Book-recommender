# 📚 LLM-Powered Book Recommender
A semantic book recommendation engine powered by Language Models (LLMs), vector embeddings, and modern NLP libraries like LangChain, OpenAI, and Hugging Face.

# Features
- Recommends books based on user preferences using semantic similarity (not just keywords)
- Utilizes LLM embeddings for high-quality recommendations
- Easy-to-use interface for e.g. Gradio


# HOW IT WAS DONE(STEP BY STEP)
1. Installed Dependencies
-Main packages:
-langchain
-openai
-huggingface_hub
-pandas
-gradio (for UI)

2. Get API Keys
OpenAI API Key 
Hugging Face Access Token: 

4. Set Up Environment Variables
Created a .env file in the project root which had:
OPENAI_API_KEY=sk-xxxxxx
HUGGINGFACEHUB_API_TOKEN=hf_xxxxxxx

5. Preprocessed Book Data & Built the Recommendation Pipeline  
- Cleaned and tagged book descriptions (using pandas and custom scripts)
- Saved processed descriptions to `tagged_description_clean.txt`
- Loaded text using LangChain’s `TextLoader` with UTF-8 encoding
- Used `CharacterTextSplitter` to split documents for processing
- Generated vector embeddings for book descriptions using OpenAI/Hugging Face APIs
- Built a semantic search pipeline with LangChain (vector search)
- Connected everything to a Gradio interface for easy querying and recommendations

# Project Structure
book-recommender-llm/
│
├── data/
│   └── books.csv,books_with_categories.csv
├── tagged_description_clean.txt
├── gradio-dashboard.py
├── data-exploration.ipynb,vector-search.ipynb,sentiment-analysis.ipynb
├── .env
└── README.md

References
- freeCodeCamp
- LangChain Documentation
- OpenAI API Docs
- Hugging Face Hub
