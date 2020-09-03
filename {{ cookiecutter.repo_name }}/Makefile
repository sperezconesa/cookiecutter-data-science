.PHONY: make_conda update_conda remove_conda

PROJECT_NAME = {{ cookiecutter.repo_name }}

make_conda:
	conda env create -f environment.yml

update_conda:
	conda env update --file environment.yml

remove_conda:
	conda remove --name $(PROJECT_NAME) --all
