# Clinical Knowledge Retrieval

This project focuses on building an end-to-end Information Retrieval (IR) pipeline for clinical and psychological documents. The system processes raw PDF files, converts them into structured JSON data, indexes the collection, and evaluates multiple retrieval models on a set of predefined queries.

The project is implemented in three phases, following the official specification of the course assignment.

---

## Phase 1 — PDF Extraction & JSON Structuring
The goal of the first phase was to automatically extract structured information from clinical PDF documents.  
Based on the project description, this phase includes:
- Extracting text from PDF files
- Identifying titles, sections, and key attributes
- Designing heuristics to infer document hierarchy
- Converting each document into a structured JSON format  
(According to the specification on page 1 of the project PDF :contentReference[oaicite:2]{index=2})

The extracted JSON files serve as the dataset for the next phases.

---

## Phase 2 — Information Retrieval Models
Using the structured JSON corpus, several retrieval models were implemented and evaluated:
- **TF-IDF Vector Space Model**
- **Boolean Retrieval Model**
- **Custom heuristic model**

Each model was tested on a set of evaluation queries, and performance metrics such as **Precision**, **Recall**, **MAP**, **MRR**, and **NDCG** were computed  
(as required by the project documentation on pages 1–3 and evaluation tables on subsequent pages :contentReference[oaicite:3]{index=3}).

Additional experiments included:
- Normalization
- Lemmatization
- Stemming  
The impact of each preprocessing step on model effectiveness was analyzed.

---

## Phase 3 — Thesaurus Construction & Query Expansion
The third phase focused on improving retrieval quality through query expansion.  
Following the course requirements:
- A thesaurus was constructed from the document collection  
  (synonyms, co-occurrence statistics, and concept relations)
- Multiple query expansion strategies were tested:
  - Using an external thesaurus
  - Filtering synonyms based on document presence
  - Cosine similarity thresholding
  - Co-occurrence matrix–based expansion  
  (as described on pages 15–17 of the project documentation :contentReference[oaicite:4]{index=4})

The effect of query expansion on ranking quality was evaluated using IR metrics.

---
