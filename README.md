# This is a template repository for python projects


*Note: this config description is to be moved to the IAI styleguide once finalized.*

## Local development config (one-time)

### Black
 
  * Install Black using `pip install black`
  * Add Black to PyCharm
    - Preferences / External tools / Add (+)
    - Program: path to black (e.g., `/opt/anaconda3/bin/black`)
    - Arguments: `$FilePath$`
    - Working directory: `$ProjectFileDir$`
  * Overwrite PyCharm's default Reformat Code shortcut with Black
    - Preferences / Keymap
    - Remove "&#8997; &#8984; L" from "Reformat Code"
    - Add "&#8997; &#8984; L" to "External tools/Black"
    
### Flake8

  * Install Flake8 using `pip install flake8`
  * Add Flake8 to PyCharm
    - Preferences / External tools / Add (+)
    - Program: path to black (e.g., `/opt/anaconda3/bin/flake8`)
    - Arguments: `$FilePath$`
    - Working directory: `$ProjectFileDir$`
 
### Pytest

  * Install Pytest using `pip install pytest`

### Install pre-commit hooks

  * This is to be done once Black and Flake8 are installed!
  * Make sure the pre-commit package is installed: `pip install pre-commit`
  * Execute `pre-commit install` to install pre-commit hooks (which are defined in `.pre-commit-config.yaml`)

### PyCharm config

  * Google-style docstrings 
    - Preferences / Tools / Python Integrated Tools
    - Docstring format: Google
  * Using pytest (instead of unittest)
    - Preferences / Tools / Python Integrated Tools
    - Default test runner: pytest
  * [Configure error highlighting according to Flake8](https://tirinox.ru/flake8-pycharm/) *For now, you can read the page using Google Translate in Chrome... we should have our internal version based on this (in English ;) )*


## Repo-level config (one-time)

### Pytest

  * Create a blank conftest.py file using `touch conftest.py`
  * Create a folder called 'tests' at the root of the repository and make it a module by creating `touch __init__.py` file
     - Use the same module structure as the source code and write tests with `test_` prefix
