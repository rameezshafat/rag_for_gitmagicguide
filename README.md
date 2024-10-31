

# RAG for Git Magic Guide

This project leverages Retrieval-Augmented Generation (RAG) to create an intelligent assistant for navigating and understanding Ben Lynn's "Git Magic" guide. By integrating retrieval and generation steps, this project offers accurate and contextually relevant answers for Git-related queries, making it easier to work with complex materials like technical manuals.

## Project Overview

**Retrieval-Augmented Generation (RAG)** is an advanced architecture designed to enhance text generation accuracy by grounding it in specific reference materials. This project uses RAG to retrieve relevant sections from the "Git Magic" guide, and then generate context-aware responses based on these sections.

### Key Features

1. **Accurate and Reliable Answers**: By retrieving content directly from the Git Magic guide, the assistant minimizes hallucinations and produces grounded, fact-based responses.
2. **Domain-Specific Assistance**: This tool is tailored for Git-related queries, ensuring detailed, relevant guidance straight from a trusted source.
3. **Efficient Document Navigation**: The RAG model intelligently identifies and pulls the most pertinent sections, saving time by avoiding unnecessary content.
4. **Optimized for Performance**: Developed and tested on an M1 chip Mac, the project uses the `all-mpnet-base-v2` model for embeddings and scaled dot-product attention (SDPA) for faster, efficient response generation.

## How It Works

RAG operates in three stages:

1. **Retrieval**: The system finds relevant information within the "Git Magic" guide, pulling out specific passages related to the query.
2. **Augmentation**: Retrieved passages are provided as context for the language model, refining the focus of response generation.
3. **Generation**: Using the context provided, the model generates a detailed response, grounded in the original content of the Git Magic guide.

## Technical Details

- **Model for Embeddings**: [all-mpnet-base-v2](https://huggingface.co/sentence-transformers/all-mpnet-base-v2) — a highly effective model for creating embeddings.
- **Attention Mechanism**: Scaled Dot-Product Attention (SDPA) is employed to efficiently match embeddings, optimizing the relevance of the retrieved information.
- **Hardware Optimization**: The project is optimized to run on an Apple M1 chip, ensuring rapid embedding creation and response generation.

## Repository Structure

- `git_magic.pdf`: Contains Ben Lynn's Git Magic guide, used as the reference document.
- `rag_forgitmagic.ipynb`: The main notebook implementing RAG, which contains the code for creating embeddings, retrieval, and response generation.
- `text_chunks_and_embeddings_df.csv`: A CSV file with pre-processed text chunks and their embeddings, used to speed up retrieval.




## Results and Evaluation

The RAG model provides accurate, contextually relevant answers that are less prone to hallucinations, particularly for domain-specific content like Git commands. This approach is ideal for technical documentation where factual accuracy is essential.

