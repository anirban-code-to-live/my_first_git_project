my_first_git_project
====================

Its just a makeshift project. Learning how to use Git.

### How to install multiple python versions in mac

1. Use pyenv. Follow this tutorial : https://weknowinc.com/blog/running-multiple-python-versions-mac-osx
2. Install pyenv  -
    ``brew install pyenv``
3. Check available versions -
    ``pyenv install -l``
4. Install the version you require -
    ``pyenv install 3.6.4``
    It gets installed in a path like this : */Users/<user_name>/.pyenv/versions/3.7.2*
5. To get a list of all Python version available to be activated, execute the following command -
    ``pyenv versions``
6. If there is a project that requires a legacy version like Python 2.7.14, you need to go to the project’s folder and execute this command inside the folder - 
    ``pyenv local 2.7.14``

