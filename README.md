# Quarto Site Rendering Guide

This repository contains a Quarto website with interactive Plotly charts and a customized Sketchy theme.

Live site: [https://astrostat-academy.github.io/presentation/](https://astrostat-academy.github.io/presentation/)

## Prerequisites
- Git
- Conda (or Mamba)
- Quarto CLI

## Local Rendering

1. Clone the repository  
git clone &lt;repo-url&gt;  
cd &lt;repo&gt;

2. Create and activate the environment  
conda env create -f environment.yml  
conda activate quarto-env

3. Verify Quarto  
quarto --version

4. Render the site  
quarto render --clean

5. Open the result  
Linux: xdg-open _site/index.html  
macOS: open _site/index.html

## GitHub Pages Publishing

Publishing is automated via GitHub Actions.

1. Commit and push changes to main  
git add .  
git commit -m "update site"  
git push origin main

2. GitHub Actions will build and publish the site to the gh-pages branch automatically.

3. Access the site at  
https://&lt;username&gt;.github.io/&lt;repo&gt;/

## Notes
- Do not modify the gh-pages branch manually.
- All source files live on the main branch.
- The rendered output is generated into the _site/ directory.
