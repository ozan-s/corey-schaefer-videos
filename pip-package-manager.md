# Python Tutorial: pip - An in-depth look at the package management system
[Video](https://www.youtube.com/watch?v=U2ZN104hIcc)

## Help on pip
    pip help
    pip help install

## Search for packages
    pip search Pympler

## Install a package
    pip install Pympler

## List of installed packages
    pip list

## Uninstall package
    pip uninstall Pympler

## List packages with available updates
    pip list -o     

## Update package
    pip install -U setuptools

## Get a list of packages and version numbers in requirements format
    pip freeze
    pip freeze > requirements.txt

## Install all packages from a requirements file
    pip install -r requirements.txt

## Upgrade all packages with available updates
    pip freeze --local | grep -v '^\-e' | cut -d = -f 1 | xargs -n1 pip install -U
