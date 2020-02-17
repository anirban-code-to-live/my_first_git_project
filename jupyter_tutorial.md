### Jupyter notebook setup for venv

- To add virtual environment to jupyter notebook, first activate your venv and install ipykernel:
`pip install --user ipykernel`
- Add your virtual environment by typing: `python -m ipykernel install --user --name=myenv`
- Find the installed kernelspec in *kernel.json* file (location should be printed after running the previous command).

- See the list o kernels available using: `jupyter kernelspec list`
- Remove an existing kernel by: `jupyter kernelspec uninstall myenv`
