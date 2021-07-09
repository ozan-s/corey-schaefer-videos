# Python Tutorial: VENV (Mac & Linux) - How to Use Virtual Environments with the Built-In venv Module
[Video](https://www.youtube.com/watch?v=Kg1Yvry_Ydk)

## List of installed modules
    pip3 list

## Create new virtual environment
    python3 -m venv project_env
    
## Activate virtual environment
    source project_env/bin/activate
    
## Check the active interpreter
    which python
    
## Install modules in the virtual environment
    pip install requests
    pip install pytz
    
## Export packages used in the virtual environment
    pip freeze > requirements.txt
    
## Deactivate virtual environment
    deactivate

## Delete the virtual environment
    rm -rf project_env/
    
## Create a new environment using requirements.txt
    mkdir my_project
    python3 -m venv my_project/venv
    source my_project/venv/bin/activate
    pip install -r requirements.txt
    pip list
    
Do not put project files in the venv directory.  
Do not commit venv directory to source control.

## Create virtual environment with access to system packages
    python3 -m venv my_project/venv --system-site-packages
    
## List packages only installed in the virtual environment
    pip list --local
