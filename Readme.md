# RAG

RAG is like giving an AI assistant access to a library while it's answering questions. Instead of relying solely on what it learned during training, the AI can now look up specific, current, or specialized information from external sources before generating its response.  
Think of it this way: Traditional language models are like students taking a closed-book exam, they can only use what they memorized. RAG-enabled models are like students in an open book exam, they can reference materials to provide more accurate, detailed and up-to-date answers.

R : RETRIEVAL (Retrieving relevant information from a vector database)  
A : AUGMENTED (Enriching the retrieved content and adding more metadata to the retrieved content)  
G : GENERATION (Generating a response based on the context retrieved by LLM)  

## Prompt Engineering VS Fine Tuning VS RAG

### Prompt Engineering

It's more about giving a prompt to a base LLM. Eg: Open AI, Gemini.  
**Prompt**: Act as a chef, provide me a recipe.  
1. Specific instructions in the prompt.
2. Prompt should be structured with clear context.
3. Model remains unchanged.

**PROS**
1. No technical expertise needed.
2. Instant results.
3. No training cost involved.
4. Works with any LLM.

**CONS**
1. Most LLMs have limited base knowledge. No expertise.
2. Inconsistent results (Different results by tweaking prompts)
3. Every model has a token limit restriction.
4. Can't add new knowledge.

**Best for**
1. Small scale application.
2. Generic purpose tasks.
3. Quick prototyping.


### Fine-Tuning

Teaching the base LLM through training.  
Companies creating their own chatbots.  
1. Prepare domain specific training data.
2. Train model on the data.
3. Creates a specialized version of a base LLM.

**PROS**
1. Deeply specialized knowledge.
2. Consistent behaviour.
3. No prompt engineering needed.
4. Better for a specific domain.

**CONS**
1. Expensive (GPUs required)
2. Require ML expertise.
3. Regular retraining required for updates.

**Best for**
1. Specific style.
2. High volume data.
3. Where accuracy is critical.


### RAG

1. Store documents in Vector database.
2. Retrieve relevant documents from db.
3. LLM generate answers from Context.

**PROS**
1. Always have updated information.
2. No training required.
3. Cost-effective
4. Accuracy is very high and it keeps increasing.
5. Can handle private/proprietary data

**CONS**
1. Infrastructure setup.
2. Retrieval quality affects results.
3. Context window limitation

**Best for**
1. Customer support
2. Knowledge based documentation.
3. Real-time/Frequently updated info
4. Compliance-heavy industries.


## RAG Architecture

**Example of Vector Database :**
1. FAISS
2. ChromaDB
3. DataStax
4. PineCone

**Techniques to retrieve similar vectors :**
1. Similarity Search
2. Euclidean Distance
3. Cosine Similarity

### Document Ingestion and Preprocessing Phase
1. Read data from all sources(pdf/doc/website) and create a data ingestion pipeline and do some pre-processing for ingestion.
2. Divide documents in chunks.
3. Pass all data to embedding model.
4. Embedding model converts them to vectors.
5. Stored in Vector Database. Query Processing Phase

### Query Processing Phase
### Generation Phase






























