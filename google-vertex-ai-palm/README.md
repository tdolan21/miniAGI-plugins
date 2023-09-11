# Google Vertex AI PaLM

## Overview
Note: This is seperate from the Google PaLM integration, it exposes Vertex AI PaLM API on Google Cloud. 

This Streamlit application integrates Google Vertex AI for generating responses to user queries. It offers multiple models for different use-cases like code chat, text embedding, etc. Users can input questions and receive step-by-step answers from the assistant.

## Install

First you must acquire Google credentials and have them set up in the .env before continuing. 

By default, Google Cloud does not use customer data to train its foundation models as part of Google Cloud's AI/ML Privacy Commitment. More details about how Google processes data can also be found in Google's Customer Data Processing Addendum (CDPA).

To use Vertex AI PaLM you must have the google-cloud-aiplatform Python package installed and either:

    Have credentials configured for your environment (gcloud, workload identity, etc...)
    Store the path to a service account JSON file as the GOOGLE_APPLICATION_CREDENTIALS environment variable

This codebase uses the google.auth library which first looks for the application credentials variable mentioned above, and then looks for system-level auth.

For more information, see:

    https://cloud.google.com/docs/authentication/application-default-credentials#GAC
    https://googleapis.dev/python/google-auth/latest/reference/google.auth.html#module-google.auth

## Environment Variables

```
GOOGLE_API_KEY=your_google_api_key
GOOGLE_CSE_ID=your_google_cse_id
```

### Functionality
- Uses Google Vertex AI for generating responses.
- Allows users to select from multiple models.
- Provides a chat interface for user queries.

## Usage
1. Run miniAGI && select the agent from the sidebar
2. Select a model from the dropdown.
3. Input your question in the chat box.
4. View the assistant's response in the chat window.

## Requirements
- Google Cloud SDK
- Google Cloud JSON credentials acquired locally. (More information in miniAGI main docs)
- Google Cloud Bucket storage
- Environment variables set in the .env

## Future Work
- Additional AutoML/Vertex capabilities.
- Add more models for diverse use-cases.
- Enhance the interactive experience with additional UI components.


