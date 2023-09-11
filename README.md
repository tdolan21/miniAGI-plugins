# miniAGI-plugins
This is a repo of plugins available for miniAGI. miniAGI and its documentation are available at http://www.github.com/tdolan21/miniAGI

## Format

The format for plugins follows the same structure as miniAGI
|-miniAGI && init
|--pages
|--documents

If you wish to add a plugin, the structure should replicate this to ensure seamless integration.

## Install

To install any of the plugins simply choose the one you want and download it.

You will find a README for each plugin with the instructions, but the only thing you need to do is drag the file from the plugin repo to the corresponding placement in the miniAGI application.

Plugins inside of pages go inside the pages of miniAGI

Plugins with documents directories may also have their own docstore. For this simply drag the documents subdirectory to the corresponding location inside of miniAGI.

The docker environment has all of the dependencies needed to run these plugins, but you will need to check each readme to ensure you have the proper environment variables enabled for the plugin. 
