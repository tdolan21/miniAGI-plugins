# miniAGI with Streamlit and OpenAI API Chains

## Overview
This Streamlit application is designed to interact with different APIs via OpenAI's language model. It provides a chat interface where the user can select an API, input a query, and receive a real-time response.

### Environment Variables
- `LISTEN_API_KEY`: API key for the Podcast API.
- `TMDB_BEARER_TOKEN`: Bearer token for TMDB API.

### API Chains
- `chain`: API chain for TMDB.
- `podcast_chain`: API chain for Podcasts.

## Usage
1. Run miniAGI
2. Select the API you want to query using the dropdown.
3. Type your query in the chat input.
4. Receive the assistant's response in real-time.
5. Information about the executed API chain is saved in a YAML file.

## Future Work
- Add more APIs to the selection.
- Provide error handling for API failures.

Note: Ensure that environment variables `LISTEN_API_KEY` and `TMDB_BEARER_TOKEN` are set before running the app.
