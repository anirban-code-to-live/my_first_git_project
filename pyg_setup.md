Setup PyTorch-Geometric
=============================================

### How to use pytorch-geometric in linux
1. Create a virtual environment in conda with python version >= 3.7 - 

    ``conda create --name <venv_name> python=<python_version>``
    
2. Install pytorch (version >= 1.11) - 

    #### CUDA 10.2
    ``conda install pytorch==1.11.0 torchvision==0.12.0 torchaudio==0.11.0 cudatoolkit=10.2 -c pytorch``

    #### CUDA 11.3
    ``conda install pytorch==1.11.0 torchvision==0.12.0 torchaudio==0.11.0 cudatoolkit=11.3 -c pytorch``

    #### CPU Only
    ``conda install pytorch==1.11.0 torchvision==0.12.0 torchaudio==0.11.0 cpuonly -c pytorch``
    
3. Install pytorch-geometric -

    ``conda install pyg -c pyg``
