This repository provides the documentation for Exoscale managed cloud
products.

# Description

This website is build using [mkdocs](http://www.mkdocs.org/)
documentation framework. It uses a theme replica of 
[ReadTheDocs](https://readthedocs.org/) and is built with Bootstrap.

All configuration is done under mkdocs.yml and the site is distributed
as a static website.

# Contributing

You need Python and pip as a requirement for this project.

1. Fork this repository and clone it to your computer
2. Create a Virtual environment `mkvirtualenv managed-docs`
3. install requirements `pip install -r requirements`
4. Run the documentation website with `mkdocs serve`

You can then start modifying documentation stored under `docs/`
folder.

On Windows we recommend that you install Python and pip 
with [Chocolatey](https://chocolatey.org/).
