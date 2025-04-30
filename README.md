This is a fork of the [squidfunk/mkdocs-material](https://github.com/squidfunk/mkdocs-material) repository
that uses [adjusted breakpoints](https://github.com/squidfunk/mkdocs-material/issues/1404) to work
better on smaller screens.

Steps to reproduce:


1.  Clone the repository:

    ```
    git clone https://github.com/jpassing/mkdocs-material-smallscreen.git && cd mkdocs-material-smallscreen
    ```
    
1.  [Adjust breakpoints](https://github.com/squidfunk/mkdocs-material/issues/1404)
    in `src/templates/assets/stylesheets/_config.scss` and `src/templates/assets/javascripts/bundle.ts`.

1.  [Rebuild the theme](https://squidfunk.github.io/mkdocs-material/customization/#building-the-theme):

    ```
    python -m venv venv
    source venv/bin/activate

    pip install -e ".[recommended]"
    pip install nodeenv

    nodeenv -p -n lts
    npm install

    npm run build
    ```
    
    This step regenerates the files in the `material/` directory.
    
1.  Commit changes.
