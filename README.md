<h1>LangChain Pinecone Book Query</h1>

<p>This project demonstrates how to use LangChain to query a book using OpenAI and Pinecone. By splitting the book into smaller documents using LangChain, and then converting them into embeddings using OpenAI's API, users can query the data stored in Pinecone to receive contextually relevant answers to their questions.</p>

<h2>Getting Started</h2>
<p>To get started, clone or download the project repository from GitHub. Make sure you have Python 3.x and Jupyter Notebook installed on your machine. Then, navigate to the project directory and open the Notebook "Ask A Book Questions.ipynb"</p>

<h2>Loading Data</h2>
<p>The notebook begins by loading an unstructured PDF file using LangChain's UnstructuredPDFLoader. You can also load an online PDF file using OnlinePDFLoader. Once the file is loaded, the RecursiveCharacterTextSplitter is used to split the document into smaller chunks. The chunk_size and chunk_overlap parameters can be adjusted to your liking.</p>

<h2>Creating Embeddings and Indexing</h2>
<p>After the data is chunked up, the next step is to create embeddings of the documents using OpenAI's API. Make sure you have an API key from OpenAI and Pinecone before proceeding. Once the embeddings are created, Pinecone is initialized with the api_key and environment parameters, and a new index is created with a name of your choice.</p>

<p>The documents are then indexed into Pinecone using Pinecone.from_texts. This allows for semantic search later on.</p>

<h2>Querying the Documents</h2>
<p>Once the documents are indexed, the notebook demonstrates how to use LangChain's Question Answering module to query the indexed documents for an answer to a specific question. The similarity_search function is used to query the indexed documents in Pinecone, and then the load_qa_chain function is used to load the question-answering chain. Finally, the notebook outputs the answer to the question, which is retrieved from the indexed documents.</p>

<h2>Conclusion</h2>
<p>By following this notebook, you can use LangChain and Pinecone to efficiently query large documents for relevant information. Feel free to modify the notebook and experiment with different documents, chunk sizes, and search queries to see how well the system performs.</p>
