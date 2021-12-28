# General
New MacOS come with python3 (v3.8.9 in "/usr/bin" in my case) already installed. It cannot be deleted because /usr/bin is on the System's read-only volume.
I first used Homebrew to install Anaconda (/opt/homebrew/anaconda3). Then, I used Anconda to install Python (/opt/homebrew/anaconda3/bin/python)

## MacOS Terminal 
Zsh-shell Beginners' Tutorial: https://www.youtube.com/watch?v=ogWoUU2DXBU&t=262s&ab_channel=Academind

### Commands
cd = change directory
cd / = go to root-directory
cd / Users = got o Users-directory
cd ~ (or cd) = go to home-directory
cd .. = go to higher directory
pwd = print working directory 
ls = list objects and info
mkdir = create new directory
touch = create an empty file
which or type = see object’s path 
echo $PATH = print PATH environment variable
source = read and execute commands from given 'file_name' and return. Pathnames in $PATH are used to find the directory containing 'file_name'
alias = create CLI shortcut


## Virtual Environment (VE)
### Create VEs with the built-in venv module
Tutorial (Corey Schafer): https://www.youtube.com/watch?v=Kg1Yvry_Ydk&ab_channel=CoreySchafer<br>
Create a new VE (e.g. 'new_ve'):
```
python -m venv new_ve
```
The new VE will come as a folder (called as the name given to the VE, i.e., 'new_ve' in this case) that contains the 'bin', 'include' and 'lib' subfolders. The 'bin' subfolder contains the file to be run to activate the environment.

Activate the VE:
```
source new_ve/bin/activate
```

Deactivate the VE:
```
deactivate
```
Tip: it is convention to first create the project's folder (e.g. my_project) and then create the VE, called venv, inside it. In this manner, your own files don't get mixed with the VE files. For example:
```
mkdir my_project
python -m venv my_project/venv
```

### Create VEs with Anaconda
Guide: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html<br>
Differently form the venv module, Anaconda installs all the VEs into the 'envs' directory in the conda directory by default. To see a list of all of the VEs created with Anaconda, run `conda env list`. If you decide to keep the defalt settings, you can directly create the new project directory (e.g. my_project):
```
conda create -n my_project python=3.10.0
```
To activate the VE, run `conda activate my_project` (you can do it from any directory). To deactivate the VE, run `conda deactivate`.

To remove the VE:
```
conda remove --name my_project --all #where 'all' refers to 'all installed packages'
```

