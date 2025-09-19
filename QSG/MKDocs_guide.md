> **Title:** Quick Start: MkDocs  
> **Author:** Saumil Khanna  
> **Last updated:** 2025-09-03  
> **Version:** 1.0  

# Quick Start : MkDocs

## Overview
This article explains how to install, configure and run MkDocs for the first time. 
## Prerequisites
- Python 3.x installed
- pip package manager installed
- Terminal or command line access
## Installation
> **Note:** The package and command name are lowercase `mkdocs`.  
> Using `MkDocs` or `Mkdocs` may sometimes work during installation,  
> but the recommended and reliable form is always `mkdocs`.

1. Check the python version : 
```bash
python --version
```
Expected output:

```bash
python 3.x.x
```
2. Check the pip package manger version : 
```bash
pip --version 
```
Expected output:
```bash
pip x.x.x from C:\Python311\Lib\site-packages\pip (python 3.x)
```
---
![SS for steps1&2](screenshots\S12.png)
--
3. Install Mkdocs :
```bash
pip install MkDocs
```
Expected output:
```bash
Successfully installed MkDocs-1.6.1 ....

```
4. check for installation:
```bash
python -m mkdocs --version
```
Expected output:
```bash
mkdocs, version 1.6.1 from C:\Python311\Lib\site-packages\pip (python 3.x)

```

## Create a new project
1. Create a new project:
```bash
python -m mkdocs new my-docs
```
Expected output:
```bash
> python -m mkdocs new my-docs
INFO    -  Creating project directory: my-docs
INFO    -  Writing config file: my-docs\mkdocs.yml
INFO    -  Writing initial docs: my-docs\docs\index.md
```
2. Open the new project:
```bash
cd my-docs
``` 
3. Open the index.md file which is an auto-generated file.
Expected output:
![s22](screenshots\s22.png)
4. This is the expected project structure:
![s23](screenshots\S23.png)

## Run the development server
1. Run the development server :
```bash
python -m mkdocs serve 
```
Expected output:
```bash
INFO    -  Building documentation...
INFO    -  Cleaning site directory
INFO    -  Documentation built in 0.19 seconds
INFO    -  [03:20:14] Watching paths for changes: 'docs', 'mkdocs.yml'
INFO    -  [03:20:14] Serving on http://127.0.0.1:8000/

```
2. Click on http://127.0.0.1:8000/, this will open the index.md on the server.
Expected output:
![s24](screenshots\s24.png)

## Build the site
### To build the site,
Run this command :
```bash
python -m mkdocs build
```
Expected output:
```bash
INFO    -  Cleaning site directory
INFO    -  Building documentation to directory: C:\QA_1F\my-docs\site
INFO    -  Documentation built in 0.20 seconds

```
After the build, a new site/ folder appears in your project with HTML, CSS, JavaScript, and other assets.
![ss25](screenshots\ss25.png)

## Troubleshooting
**Problem:** pip is not recognized
**Solution:** Ensure Python is added to your system PATH during installation. You can verify this by running:
```bash
python --version
```
If Python works but pip doesn't, reinstall Python and select “Add Python to PATH.”

**Problem:** mkdocs is not recognized after installation
**Solution:** Use the safer form, which runs MkDocs directly from Python without relying on the PATH:


```bash
python -m mkdocs --version
```

**Problem:** Port 8000 already in use

**Solution:** Run the development server on a different port:


```
python -m mkdocs serve -a 127.0.0.1:9001
```
**Problem:** Permission denied while installing packages

**Solution:** Add the --user flag:


```bash
python -m pip install --user mkdocs
```
Alternatively, run your terminal or PowerShell as an Administrator.

**Problem:** Changes in index.md not showing in the browser

**Solution:** Refresh the browser tab and check the terminal logs to confirm the server is running and watching for changes.

## Next Steps
- Add pages: Create new .md files in docs/ and add them to mkdocs.yml under nav.

- Explore themes: Try built-in themes or Material for MkDocs
.

- Customize navigation: Edit mkdocs.yml to structure sections and pages.

-Deploy to GitHub Pages:
```bash
python -m mkdocs gh-deploy
```

- Learn advanced features: Add search, plugins, and versioning

---
**Document Owner:** Saumil Khanna  
**Review Cycle:** Every 6 months  
**Feedback:** Please report issues or suggestions to saumil.khanna@example.com  
---