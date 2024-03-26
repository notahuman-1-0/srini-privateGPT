
# privateGPT + ollama integration

a document management system integrating privateGPT, ollama, and langchain alongside chromaDB for streamlined document interaction. 




## Installation

open up a terminal and follow along : 

```bash
  git clone https://github.com/notahuman-1-0/srini-privateGPT.git
  cd srini-privateGPT
```

once you are in the directory make sure you are running python >=3.11.x if not setup a virtual-env

```bash
  pip install virtualenv
  python3.11 -m venv <virtual-environment-name>
```

then finally activate your env
```bash
  source env/bin/activate
```

#### now that we have setup our environment let's proceed with our ollama installation

1. head to [ollama](https://ollama.com/)
2. install the version specific to your OS.
3. now make sure ollama is running in the background

### back to the working directory

1. first install all the required dependcies
```bash
  pip install -r requirements.txt
```

now that the required dependecies are installed let's proceed with ingesting our documents.

#### create a folder under the name "source_documents" in the directory if not there already.

```bash
  mkdir source_documents
  cd source_documents
```


#### now paste the document you wish to interact with here, as of now we support the following file formats.
- .pdf
- .pptx
- .docx
- .csv
- .doc
- .enex
- .eml
- .epub
- .html
- .md
- .odt
- .pdf
- .ppt
- .pptx
- .txt

more soon to come!

once you are done upload document (one at a time) it's to ingest the data into the vectordb!

you can do that by running : 
```bash
  python3 ingest.py
```

this will create vectorstore for the document and split the document to 'n' chunks of data. if sucessfull you should see this kind of a message :

```bash
  Creating embeddings. May take some minutes...
Ingestion complete! Please run privateGPT.py to query your documents
```

once done let's move on to quering with the document!

```bash
  python3 privateGPT.py
```

you can then enter your query and communicate with your document!