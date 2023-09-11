# miniAGI-plugins

![miniAGI Logo](logos/cropped_logo_blue.png)

This is a repo of plugins available for miniAGI. miniAGI and its documentation are available at [GitHub miniAGI Repository](http://www.github.com/tdolan21/miniAGI).

![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-336791?logo=postgresql&logoColor=white)
![Conda](https://img.shields.io/badge/-Conda-44A833?logo=anaconda&logoColor=white)
![Streamlit](https://img.shields.io/badge/-Streamlit-FF4B4B?logo=streamlit&logoColor=white)
![Langchain](https://img.shields.io/badge/-Langchain-3E8FC9?)
![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![GitHub Followers](https://img.shields.io/github/followers/tdolan21?label=Follow&style=social)
![GitHub Stars](https://img.shields.io/github/stars/tdolan21?label=Stars&style=social)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
[![Issues](https://img.shields.io/github/issues/tdolan21/miniAGI.svg)](https://github.com/tdolan21/miniAGI/issues)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/tdolan21)
[![Playwright](https://img.shields.io/badge/Playwright-v1.12.3-brightgreen)](https://github.com/microsoft/playwright)
[![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-v4.9.3-brightgreen)](https://www.crummy.com/software/BeautifulSoup/)
![Built with OpenAI](https://img.shields.io/badge/Built%20with-OpenAI-2877ff)

## Format

The format for plugins follows the same structure as miniAGI:

```
- miniAGI && init
  - pages
  - documents
```

If you wish to add a plugin, the structure should replicate this to ensure seamless integration.

## Install

To install any of the plugins, simply choose the one you want and download it.

You will find a README for each plugin with the instructions. The only thing you need to do is drag the file from the plugin repo to the corresponding placement in the miniAGI application.

- **Pages**: Plugins inside of pages go inside the pages of miniAGI.
- **Documents**: Plugins with documents directories may also have their own docstore. For this, simply drag the documents subdirectory to the corresponding location inside of miniAGI.

### Dependencies

The Docker environment has all of the dependencies needed to run these plugins, but you will need to check each README to ensure you have the proper environment variables enabled for the plugin.
