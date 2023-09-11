# Playwright Scraping Agent 

## Overview
This Streamlit application allows for web scraping and content extraction using Playwright and OpenAI's GPT-3.5 Turbo. Users can enter URLs and choose a schema for data extraction. The extracted data is saved as a JSON file.

The base schema provided works for the wall street journal.

If you would like to scrape other websites, you simply need import a schema into your database using the sidebar. 

More info on how to create schemas can be found [here](https://python.langchain.com/docs/integrations/toolkits/playwright)

## Install
Drag the playwright_scraper.py file to the pages directory of miniAGI

### Functionality
- Users can input multiple URLs for scraping.
- Users can select a predefined schema for data extraction.
- Uses Playwright for web scraping and GPT-3.5 Turbo for data extraction.
- Saves extracted content as a JSON file.

## Usage
1. Run miniAGI
2. Enter the URLs you wish to scrape in the text input box. Make sure the URL matches your selected schema
3. Select the schema you wish to use for data extraction.
4. Click on the 'Process' button.
5. View extracted content and saved file location.

## Known issues
- Only one schema is included as a demo, but this gives the user complete freedom of creativity to use it how they like. More schemas will be included as the application develops.

- Docker may throw an error saying that browsers are not installed, but this is just because they are in use by other tools and is part of why this is a plugin for now. 

- Docker also may not throw an error, but for now this feature is best reserved for local usage

## Note
- The extracted content will be saved in a JSON file with a unique filename.

## Future Work
- Extend the app to support more extraction schemas.
- Optimize for larger sets of URLs.


