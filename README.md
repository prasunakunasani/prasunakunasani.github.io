# painfullydetailednotes
Holds notes that can be published to a public site with no authentication

## Setup Repo: 
* Github.com: Created an empty github repo
* For User pages, follow instructions here: https://pages.github.com/
    * Meaning, the content will be at <username>.github.io
* Add .gitignore. 
    * Ref: 
        * <https://github.com/github/gitignore> 
        * <https://github.com/mkdocs/mkdocs/blob/master/.gitignore>

## Setup local environment:  
* Create virtual env: 
    * For your sanity and not having to worry about dif python version, work using a virtual environment. 
    * check python version using `python -V`
    * `python3 -m venv venv` will create a folder call venv
    * `source venv/bin/activate` will activate the environment. Do the rest of your work in the venv. 
* Run: `pip install mkdocs-material`
    * This will install all the correct versions for dependencies. 

## Setup mkdocs project: 
* git clone the created repo: `git clone https://github.com/<username>/<reponame>.git`
* add a `/docs/index.md` and an empty `mkdocs.yml` file
* Add the necessary remotes:* User pages: `git remote add homesite https://github.com/<username>/<username>.github.io.git`
* Min info needed in the .yml:     
    ```yaml
    site_name: Site name
    theme:
      name: material
    ```
* Manual commands to push build to any git repo:
* User pages: `mkdocs gh-deploy --clean -r homesite`
* What this does: It'll push to a gh-pages branch on the repository.
* For user pages, the site will be available at username.github.io