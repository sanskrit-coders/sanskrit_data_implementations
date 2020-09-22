[![Build Status](https://travis-ci.org/sanskrit-coders/sanskrit_data_implementations.svg?branch=master)](https://travis-ci.org/sanskrit-coders/sanskrit_data_implementations)
[![Documentation Status](https://readthedocs.org/projects/indic-sanskrit_data_implementations/badge/?version=latest)](http://indic-transliteration.readthedocs.io/en/latest/?badge=latest)
[![Actions Status](https://github.com/sanskrit-coders/sanskrit_data_implementations/workflows/Python%20package/badge.svg)](https://github.com/sanskrit-coders/sanskrit_data_implementations/actions)
[![PyPI version](https://badge.fury.io/py/sanskrit_data_implementations.svg)](https://badge.fury.io/py/sanskrit_data_implementations)


## Introduction
An implementation of sanskrit_coders/sanskrit_data package.

While this package was originally motivated by Sanskrit text annotation 


# For users
## Installation
- Install this library (Replace pip2 with pip3 as needed)
    - Latest release: `sudo pip3 install sanskrit_data_implementations -U`
    - Development copy: `sudo pip3 install git+https://github.com/sanskrit-coders/sanskrit_data_implementations@master -U`
    - Local modifications: `pip install -e .`
    - [Web](https://pypi.python.org/pypi/sanskrit_data_implementations).
- Install libraries for the particular database you want to access through the sanskrit_data.db interface (as needed): pymongo, cloudant (for couchdb).

## Usage
- Please see the generated python sphinx docs in one of the following places:
    - http://sanskrit-data-implementations.readthedocs.io
    - [project page](https://sanskrit-coders.github.io/sanskrit_data_implementations/build/html/).
    - under docs/build/html/index.html
- Design considerations for data containers corresponding to the various submodules (such as books and annotations) are given below - or in the corresponding source files.

# For contributors
## Packaging
* ~/.pypirc should have your pypi login credentials.
```
python3 setup.py bdist_wheel
twine upload dist/* --skip-existing
```

## Document generation
- sphinx html docs can be generated with `cd docs; make html`
- http://sanskrit-data.readthedocs.io/en/latest/sanskrit_data.html should automatically have good updated documentation - unless there are build errors.
- To update UML diagrams, copy the outputs of the below to docs:
  - `pyreverse -ASmy -k -o png sanskrit_data.schema -p sanskrit_data_schema`
  - `pyreverse -ASmy -k -o png sanskrit_data.db -p sanskrit_data_db`
