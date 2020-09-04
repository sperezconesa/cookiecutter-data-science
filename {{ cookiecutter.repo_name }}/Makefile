.PHONY: make_conda update_conda remove_conda update_data

.ONESHELL:

PROJECT_NAME = {{ cookiecutter.repo_name }}

make_conda:
	conda env create -f environment.yml
	ipython kernel install --user --name=$(PROJECT_NAME)

update_conda:
	conda env update --file environment.yml
	ipython kernel install --user --name=$(PROJECT_NAME)

remove_conda:
	conda remove --name=$(PROJECT_NAME)

update_data:
	 while read a b;do rsync -rauv --delete --include-from=data/raw/include_list.txt   data/raw/$$a data/raw/$$b;done < data/raw/dir_list.txt

help:
	@echo "Possible options"
	@echo "make_conda"
	@echo "update_conda"
	@echo "remove_conda"
	@echo "update_data"
