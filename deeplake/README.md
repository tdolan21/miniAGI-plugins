# miniAGI + deeplake

This is a suite of tools to integrate various deeplake functionality with miniAGI. I will include information about each tool specifically, but the install applies to all of the tools whether you want one of them or all of them. 

## ⚠️ Warning ⚠️

These plugins can be extremely expensive if used improperly. For example, if you used this tool to chat with the twitter codebase you would find that it costs roughly 4$ per scan of the codebase using GPT-4. This is achieved by using openAI embeddings, so if you create a large dataset, keep in mind that the whole thing will be embdedded once per session. After the initial embed, it will only charge you for the token count of the embeds used to answer the question.

If your embed is 100k tokens it will embed 100k tokens the first time
The second question may only use 100 tokens worth of embedded content. 

## Install

Drag the features you wish to use into the pages directory of miniAGI

If you are using the image similarity search feature you will need the deeplake_images directory to be placed inside of documents directory in miniAGI.

### Environment Variables
- `ACTIVELOOP_USERNAME`: Username for your own deeplake dataset. This is used to create a codebase with miniAGI and chat with the code itself
- `ACTIVELOOP_HUB_PATH`: Activeloop hub path to the dataset you wish to chat with

# Deeplake Codebase Search

## Overview
This Streamlit application is designed to search through the miniAGI codebase and provide relevant code snippets based on user queries. The app uses OpenAI Embeddings and DeepLake vector stores to power the search.

### Functionality
- The application scans through `.py` files in the codebase and loads them into memory.
- Text from the codebase is split and embedded.
- A retrieval-based model assists in answering queries about the codebase.

## Usage
1. Run miniAGI
2. Type your query in the chat input.
3. View the assistant's response in real-time.

## Note
- Make sure to configure the environment variables as specified in the `.env` file.

## Future Work
- Extend the search capabilities.
- Integrate with other codebases.


# Deeplake Image Similarity Search

## Overview
This Streamlit application is designed for image similarity search using the Deeplake vector store. Users can upload images to a vector store and search for similar images within the store.

### Functionality
- The application uses a pretrained ResNet18 model to generate embeddings for images.
- Users can upload images to a Deeplake vector store.
- Users can search for similar images by asking queries.

## Usage
1. Run miniAGI
2. Navigate the sidebar to configure settings.
3. Upload images using the file uploader.
4. Use the chat input to initiate a search query.

## Note
- Make sure to configure the environment variables as specified in the `.env` file.
- The app is currently under construction :construction:.




