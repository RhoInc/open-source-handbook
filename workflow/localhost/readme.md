# Hosting a Webpage Locally with Python
Sometimes hosting a local copy of a webpage is helpful for testing or development tasks. Follow the steps below to host a page in Windows 10 using Python. 

## Download Python v2.7 (one time only)

1. Go to [the python downloads page](https://www.python.org/downloads/release/python-2716) and click the link to download the 'Windows x86-64 MSI installer'
2. Step through the installer
3. Add the python directory to the windows PATH following [these directions](https://superuser.com/a/143121)

## Clone the repo (one time per repo)

1. Open the command prompt
2. Navigate to the location where you’ll save the repo (e.g. ’cd github’
3. Download the repository by typing the following command (fill in the repository name): `git clone https://github.com/RhoInc/**your-repo-here**.git` (e.g. `git clone https://github.com/RhoInc/safety-explorer-suite`)

## Locally host a branch of a webpage

1. Open the command prompt
2. Navigate to the repo (e.g. `cd github\safety-explorer-suite`)
3. Update the repo with `git pull`
4. Change to the desired branch with `git checkout **branch-name**` (e.g. `git checkout dev-v0.8.3`)
5. Update the branch with `git pull`  
6. Start a temporary local web server by typing this command: `python -m SimpleHTTPServer 8000`
7. View the page in your web-browser by going to `localhost:8000\test-page` in the navigation bar. 
