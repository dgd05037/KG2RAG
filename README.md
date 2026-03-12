# KG2RAG-lite

KG2RAG-lite is a hybrid retrieval system that combines dense retrieval and knowledge graph traversal for entity-centric question answering on cultural heritage data.

Semantic Search Pipeline
Dense Embedding Retrieval
Knowledge Graph Augmented RAG

## Pipeline

Query  
→ Dense Retrieval  
→ Entity Extraction  
→ Relation-aware KG Traversal  
→ Hybrid Reranking  
→ Structured Answer Generation

## Features

- Sentence-transformer based dense retrieval
- Knowledge graph construction from cultural heritage data
- Relation-aware graph traversal for candidate expansion
- Hybrid reranking combining dense similarity and graph proximity
- Structured answer generation from retrieved items

## Example Queries

- 이방운 작품에는 어떤 문양이 등장하는가?
- 청자 향로의 재질은 무엇인가?
- 강남춘의도의 작가는 누구인가?

## Running

Open `KG2RAG_demo.ipynb` and run the notebook cells sequentially.

## Dataset

The original dataset is not included in this repository.
A small sample file is provided for demonstration.
