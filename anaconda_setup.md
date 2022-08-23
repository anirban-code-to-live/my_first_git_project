
Anaconda Setup
====================

In this, we learn how to set up a conda environment in few steps (without much talking!).

### How to install anaconda in linux
1. Download the anaconda installer for your OS.

    ``wget https://repo.anaconda.com/archive/Anaconda3-2021.11-Linux-x86_64.sh``

2. Install by executing the following commans - 

    ``sh <downloaded_path>/Anaconda3-2020.02-Linux-x86_64.sh``
    
3. The installer prompts “In order to continue the installation process, please review the license agreement.” Click Enter to view license terms.
4. Scroll to the bottom of the license terms and enter “Yes” to agree.
5. Install in the deafult location.
6. The installer prompts “Do you wish the installer to initialize Anaconda3 by running conda init?” We recommend “yes”.
7. Close and open your terminal window for the installation to take effect, or you can enter the command ``source ~/.bashrc``

For more details, follow this tutorial : https://docs.anaconda.com/anaconda/install/linux/

### How to use anaconda in linux
1. Verify conda installed or not - 

    ``conda --version``

2. Create a new environment (with a specific python version) -

    `` conda create --name <venv_name> python=<python_version>``
  
3. To see the list of environments - 

    ``conda info --envs``

4. Activate the base environment - 

    ``conda activate``

5. Activate the specific environment you just created -

    ``conda activate <venv_name>``
   
6. To search a specific python package available or not - 

    ``conda search <python_package_name>``
   
7. To install specific python package in conda -

    ``conda install <python_package_name>=<package_version>
    
8. To view list of python packages installed -

    ``conda list``
    
9. To remove a conda environment -

    ``conda env remove --name <env_name>``

References: https://conda.io/projects/conda/en/latest/user-guide/getting-started.html#more-information
    
### Installing jupyter notebooks in conda environment
1. Install jupyter notebooks- 

    ``conda install -c conda-forge notebook``
    
    ``conda install -c conda-forge nb_conda_kernels``
   
2. Install jupyter lab -

    ``conda install -c conda-forge jupyterlab``
    
    ``conda install -c conda-forge nb_conda_kernels``
    
3. Install jupyter notebook extensions -

    ``conda install -c conda-forge jupyter_contrib_nbextensions``
    
4. Running the following command will create a kernel that can be used to run jupyter notebook commands inside the virtual environment -

    ``ipython kernel install --user --name=<venv_name>``
    
5. Select the installed kernel when you want to use jupyter notebook in this virtual environment

References: https://www.geeksforgeeks.org/using-jupyter-notebook-in-virtual-environment/, https://towardsdatascience.com/how-to-set-up-anaconda-and-jupyter-notebook-the-right-way-de3b7623ea4a
