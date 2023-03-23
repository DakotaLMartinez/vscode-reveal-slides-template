# Reveal.JS Slides Template

This template repository will serve as a springboard for using markdown (mdx) to generate a [RevealJS](https://revealjs.com/) slideshow within the [VS Code Text editor](https://code.visualstudio.com/) using the [VSCode Reveal extension](https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal). You can publish the slideshow on [GitHub pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site) by [setting the publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) to the main branch at the '/docs' directory. 

The template will preconfigure the VSCode reveal extention to export the slide deck to the /docs directory so it will be published via GitHub pages when configured as described below.

## Requirements

- [Visual Studio Code](https://code.visualstudio.com/) is installed
- The [VSCode Reveal](https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal) Extension is installed and enabled

## Usage:

 Use this template repository to create a new repo for your deck. 
### In VSCode
1. Clone the repository to your local machine
2. Open the repository in VSCode and edit the slides.md file
3. Click on the RevealJS icon in the Sidebar menu
4. Click on the 3rd icon from the left to preview the slideshow in your browser
5. Click on the 1st icon from the left (HTML5) to export the deck to the /docs directory
6. Add, commit, and push your updated built deck to your repository


### On GitHub

- Visit your repository on GitHub and 
  - Navigate to **Settings** 
  - Select **Pages** from the bottom of the Code & Automation section in the left hand navigation
- In the build and deployment section, 
  - Keep **Source** as "Deploy from a branch".
  - Set **Branch** to "main" and the **directory** to "/docs"
  
Once this is complete, building your deck from the VSCode UI as described above will tell GitHub pages to display your deck.

## Gotchas

This repository includes a file `.vscode/settings.json`

```json
{
  "revealjs.css": [
    "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.3.0/css/all.min.css"
  ],
  "revealjs.width": 1000,
  "revealjs.height": 750,
  "revealjs.theme": "night",
  "revealjs.exportHTMLPath": "./docs"
}
```

The two most important settings here are:
- The `.css` option that adds a link to font awesome. This will make sure that the icon links at the bottom left of the slide show will work properly.
- The `.exportHTMLPath` set to `./docs` will make sure that GitHub pages will display the built slide deck (when GitHub pages is properly configured)

These settings will override any user settings that you have configured via the VSCode Reveal configuration options in the preferences menu (UI) or via your user settings JSON file. You may wish to remove these other settings or update them in your repository if doing so would better fit your use case.


## Resources

- [Reveal.js docs](https://revealjs.com/)
- [VSCode Reveal extension](https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal)
- [Creating a Site on GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site)
- [Setting the publishing source for a GitHub pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)