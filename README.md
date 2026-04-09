# Drug-Response-Chatbot
This project is a Retrieval-Augmented Generation (RAG)-based biomedical chatbot that provides insights about anticancer drugs using real pharmacogenomic data from the GDSC (Genomics of Drug Sensitivity in Cancer) dataset.
The system combines bioinformatics, machine learning, and generative AI to deliver accurate, drug-specific information such as:

- Drug targets
- Biological pathways
- Cancer types affected
- Drug sensitivity (IC50 range)

# Features
-  Biomedical data processing from GDSC dataset
-  Advanced data cleaning and missing value handling
-  Drug level aggregation for structured knowledge creation
-  Semantic search using Sentence Transformers
-  Fast retrieval with FAISS vector database
-  Answer generation using BioGPT (Microsoft)
-  Retrieval-Augmented Generation (RAG) pipeline
-  Interactive UI using Streamlit

 # Project Architecture
 Raw GDSC Data
      ↓
Data Cleaning & Preprocessing
      ↓
Drug-level Aggregation
      ↓
Text Knowledge Base Creation
      ↓
Embeddings (SentenceTransformer)
      ↓
FAISS Vector Store
      ↓
User Query
      ↓
Semantic Retrieval
      ↓
BioGPT Generation
      ↓
Streamlit UI Output


# Methodology
1. Data Preprocessing
- Handled missing values using "Unknown" labels
- Created missing indicators for important biological features
- Removed duplicates and irrelevant columns
- 
2. Feature Engineering
- Selected biologically relevant features:
- Drug name, IC50, AUC
- Target and pathway
- Cancer type and cell line

3. Drug-Level Aggregation
- Grouped dataset by drug
- Generated summary statistics:
- IC50 (mean, min, max)
- AUC mean
- Associated cancer types and targets

4. Knowledge Base Creation
Converted structured data into natural language text

5. Embeddings & Retrieval
- Used all-MiniLM-L6-v2 for text embeddings
- Built FAISS index for fast similarity search

6. Generative AI (RAG)
- Retrieved relevant drug data
- Used BioGPT to generate domain-specific answers
- Applied prompt engineering to avoid hallucinations

# Technologies Used
- Python
- Pandas, NumPy
- Sentence Transformers
- FAISS
- HuggingFace Transformers (BioGPT)
- Streamlit

# Evaluation
- Semantic retrieval ensures relevant context selection
- Prompt constraints ensure accurate, drug-specific responses
- Combines structured biomedical data with generative AI

# Applications
- Precision medicine
- Drug discovery research
- Cancer pharmacogenomics
- Clinical decision support systems
