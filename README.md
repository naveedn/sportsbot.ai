# Goals

- I want to fine-tune a pre-trained LLM model on a custom dataset
- I want to vectorize and store embeddings of the custom dataset
- I want to embed the user query and do a similarity search on the custom dataset
- I want to use contextual compression and prompt engineering to allow the LLM to generate a response to the user query
- I want to give the LLM a peppy, assured response to the user query (personality)

## Next Steps

- I will use the [European Soccer Database](https://www.kaggle.com/hugomathien/soccer) to train the model.
- I will use openapi embeddings to vectorize and store the custom dataset alongside the row data in the database

## Potential approaches

- I could tell the LLM to create a sqlite query and use langchain to execute the query and return the results
  - I would have to see if there was a sqlite tool available for the LLM
- I could try and use vector similarity search on the embeddings to pull in relevant results into the token context (using faiss / pinecone / milvus / redis / etc.)
- Fine-tuning (not recommended): I will use the [HuggingFace Transformers](https://huggingface.co/transformers/) library to fine-tune a pre-trained LLM model on a custom dataset.

### Notes