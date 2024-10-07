# projects
Instructions for working with the code:
- Clone locally preferably via SSH protocol
- Ensure in git repo working dir
- Work with codebase:
    - Open Powershell, cd to working dir (projects site git repo)
    - Run the command: .\hugo.exe server
    - Now you can open the preview on the given localhost address:
        - http://localhost:1313/*baseURL*/
    - Make changes to content folder (content is used for build)
    - Ctrl + c to stop server	
    - In 'config.toml' ensure 'canonifyURLs = true' is present
    - Run the command: .\hugo.exe -D (builds the site)
- Push local changes to repo
- This triggers a deployment of changes (CICD via Github Actions)
- Changes will be visible post successful deployment
