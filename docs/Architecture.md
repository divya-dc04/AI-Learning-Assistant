                   Angular
                      │
              HTTP REST API
                      │
             Spring Boot Backend
          ┌───────────┴───────────┐
          │                       │
      MySQL                  FastAPI
                                  │
          ┌───────────────┬───────────────┐
          │               │               │
      LangChain     Hugging Face     ChromaDB
                             │
                 Sentence Transformers



Angular → User interface
Spring Boot → Business logic and security
MySQL → Application data
FastAPI → AI microservice
LangChain → AI orchestration
Hugging Face → Models
Sentence Transformers → Embeddings
ChromaDB → Vector database for RAG