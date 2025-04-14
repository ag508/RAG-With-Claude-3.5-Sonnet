# RAG-With-Claude-3.5-Sonnet
The code demonstrates the implementation of a Retrieval-Augmented Generation (RAG) model using the LlamaIndex library.
The RAG model combines the power of retrieval systems (efficient document retrieval based on the 
query) and language models (generating coherent and contextual responses based on the retrieved 
information). The LlamaIndex library simplifies the process of setting up and using RAG models by 
providing abstractions and utilities for data loading, indexing, and querying.

Live Demo With a Different Approch And Free To Use : https://colab.research.google.com/drive/16f-61PSUxKmraJjfx472YzdqgXA2Arjs?usp=sharing

1. Setup API Keys: The code sets the ANTHROPIC_API_KEY environment variable, which is required 
to authenticate with the Anthropic API and use the Claude language model.

![image](https://github.com/user-attachments/assets/5db6d2f3-f575-48a9-8c22-7a3ee1b0c87d)

Link: https://console.anthropic.com/settings/keys


3. Setup LLM and Embedding Model: The code imports the necessary classes from LlamaIndex 
to set up the Language Model (LLM) and the Embedding Model on goolgle Colab. It uses the Anthropic class to 
initialize the claude-3-5-sonnet-20240620 model as the LLM and the HuggingFaceEmbedding class 
to initialize the BAAI/bge-base-en-v1.5 model as the Embedding Model.

4. Download Data: The code creates a directory called data/your_data/ and downloads a JSON 
file containing the data for the RAG model from a GitHub repository.

5. Load Data: Use Your own Json file, or Use any site links to scrape data and create a Json file. The SimpleDirectoryReader class from LlamaIndex is used to load the data from the 
downloaded JSON File.

7. Index Data: The loaded data is passed to the VectorStoreIndex.from_documents method, which 
creates an index for the RAG model. This index is used to efficiently retrieve relevant 
documents for a given query.

8. Create Query Engine: The as_query_engine method is called on the created index to obtain a 
QueryEngine instance. This QueryEngine is responsible for processing queries and generating 
responses using the RAG model.

9. . Test Query: The code demonstrates querying the RAG model by calling the query method on 
the QueryEngine instance with the query "Yoru quesiton?". The RAG model 
retrieves relevant documents from the index, passes them to the LLM (Claude), and generates 
a response based on the retrieved information.


