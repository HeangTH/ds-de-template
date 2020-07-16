# ds-de-template

## Folder structure
```
ds-de-template
├── conf
│   ├── base         <- Space for shared configurations like parameters
│   └── local        <- Space for local configurations, usually credentials
├── data
│   ├── external     <- Data from third party sources
│   ├── interrim     <- Intermediate data the has been transformed
│   ├── processed    <- The final, canonical data sets for modeling
│   └── raw          <- The original, immutable data dump
├── notebooks        <- Jupyter notebooks in "logical chunks" ({something-logical}-notebook.ipynb).
│   │                   We may use some notebooks for prototyping ({something}-prototype.ipynb)
│   └── archive      <- Jupyter notebooks that no longer useful
├── references       <- Data dictionaries, manuals, and all other explanatory materials
├── scripts          <- logical units of computation that aren't part of the notebook narratives
│   └── archive      <- scripts that no longer useful
├── src              <- Source code for use in this project
│   ├── __init__.py  <- Makes src a Python module
├── test             <- Unit tests
├── .gitignore       <- Avoids uploading data, credentials, outputs, system files etc.
├── environment.yml  <- conda virtual environment definition file
└── README.md        <- The top-level README for develops using this project
```

## .gitkeep and .dummy
Both .gitkeep and .dummy are using to keep template folder structure. But they serve difference purpose.
```
.gitkeep             <- Files in folder that has .gitkeep file will be not pushed to repository.
                        Don't delete it.
.dummy               <- Using to keep template folder structure only.
                        When you push your own file to repository, can you delete .dummy file. 
```
# Set up
Install the virtual environment with conda and activate it:
```
$ conda env create -n {{name}} -f environment.yml
$ conda activate {{name}} 
```
Install src in the virtual environment:
```
$ pip install --editable .
```

## Jupyter notebooks
Now by default we turn the project into a Python package (see the setup.py file). You can import your code and use it in notebooks with a cell like the following:

```
# OPTIONAL: Load the "autoreload" extension so that code can change
%load_ext autoreload

# OPTIONAL: always reload modules so that as you change code in src, it gets loaded
%autoreload 2

from src.data import make_dataset
```





# References
https://www.dataquest.io/blog/data-science-portfolio-machine-learning/<br />
https://towardsdatascience.com/introduction-to-github-for-data-scientists-2cf8b9b25fba<br />
https://gist.github.com/ericmjl/27e50331f24db3e8f957d1fe7bbbe510<br />
http://drivendata.github.io/cookiecutter-data-science/<br />
https://medium.com/swlh/how-to-structure-a-python-based-data-science-project-a-short-tutorial-for-beginners-7e00bff14f56<br />
https://godatadriven.com/blog/how-to-start-a-data-science-project-in-python/<br />
https://github.com/cltk/cltk/wiki/Example-Git-and-Python-workflow<br />
https://towardsdatascience.com/a-guide-to-conda-environments-bc6180fc533