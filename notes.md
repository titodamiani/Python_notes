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
source = Read and execute commands from given FILENAME and return. Pathnames in $PATH are used to find the directory containing FILENAME

alias = create CLI shortcut


## Virtual Environment (VE)
### Create VE with the built-in venv module
Tutorial (Corey Schafer): https://www.youtube.com/watch?v=Kg1Yvry_Ydk&ab_channel=CoreySchafer

Create new VE (called "new_ve") with the built-in venv module:
```
python -m venv new_ve
```
The new VE will come as a folder (called as the name given to the VE, i.e., new_ve in this case) that contains the bin, include and lib subfolders. The bin subfolder contains the file to be run to activate the environment.

Activate the VE:
```
source new_ve/bin/activate
```

Deactivate the VE:
```
deactivate
```
Tip: create the VE inside of the project's folder (e.g. my_project) and call it venv. This is a very common convention. 
```
mkdir my_project
python -m venv my_project/venv
```

### Create VE with Anaconda
```
conda create -n yourenvname python=3.10.0 anaconda
```
Activate the VE:
```
source activate yourenvname
```
Deactivate the VE:
```
source deactivate
```
