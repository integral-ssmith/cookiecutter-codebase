# Instructions
Install miniconda and open anaconda prompt. Create a conda environment with cookiecutter:
> conda create --name <ENVIRONMENT_NAME_HERE>
> 
> conda active <ENVIRONMENT_NAME_HERE>
> 
> conda install cookiecutter

Change the directory to the folder path where you would like to create the project
> cd <FULL_FILE_PATH_HERE>

Create a project using cookiecutter
> cookiecutter gh:integral-ssmith/cookiecutter-codebase

Follow the prompts to generate the project, either entering new inputs and pressing enter, or pressing enter to accept the default values in [ ] beside the prompt.


# TODO
- use cookiecutter 2.1.2 when it releases for boolean support
- use private variable for project slug https://cookiecutter.readthedocs.io/en/stable/advanced/private_variables.htm