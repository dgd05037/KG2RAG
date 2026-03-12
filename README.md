# KG2RAG-lite

KG2RAG-lite is a hybrid retrieval system that combines dense embedding retrieval and knowledge graph traversal for entity-centric question answering on cultural heritage data.

The system implements a RAG-style retrieval pipeline where semantic search results are augmented and reranked using knowledge graph relations.

---

## Overview

KG2RAG-lite integrates semantic retrieval with knowledge graph reasoning to improve the accuracy of entity-centric questions.

Instead of relying only on vector similarity, the system incorporates structured knowledge from a cultural heritage knowledge graph to refine retrieval results.

---

## Pipeline

User Query  
→ Entity Extraction  
→ Relation Intent Detection  
→ Dense Retrieval (Sentence-Transformers)  
→ Knowledge Graph Traversal  
→ Hybrid Reranking (Dense Similarity + Graph Score + Relation Bonus)  
→ Structured Answer Generation

---

## Features

- Sentence-transformer based dense embedding retrieval
- Entity extraction from queries using dictionary-based matching
- Relation intent detection from query keywords
- Knowledge graph construction from cultural heritage metadata
- Relation-aware graph traversal for candidate expansion
- Hybrid reranking combining dense similarity and graph proximity
- Structured answer generation from retrieved items

---

## Example Queries

- 이방운 작품에는 어떤 문양이 등장하는가?
- 청자 향로의 재질은 무엇인가?
- 강남춘의도의 작가는 누구인가?

---

## Example Output
Question: 이방운 작품에는 어떤 문양이 등장하는가?
Top item: 동원2174
Target relation: has_pattern
Answer: 「시경」의 「빈풍칠월편」에 등장하는 문양은 나무, 산, 소, 화제, 말, 매미, 개, 버드나무, 새, 괴석, 사람, 돌이다.

## Dataset

The original system was developed using a cultural heritage knowledge graph containing approximately **12,000 cultural heritage items** and multiple relation types (e.g., creator, era, material, pattern).

Due to data sharing restrictions, the full dataset is not included in this repository.  
A small sample dataset is provided for demonstration.

---

## Running

Open `KG2RAG_demo.ipynb` and run the notebook cells sequentially.

---

## Future Work

This retrieval pipeline can be extended into a full Retrieval-Augmented Generation (RAG) system by integrating a language model for answer generation.

