# Django Project Setup


## Course Outline
+ [Lesson 01](#lesson-01-python-virtual-enviornment): Python Virtual Environment
+ [Lesson 02](#lesson-02-creating-venv-environment): Creating a `venv` Python Environment
+ [Lesson 03](#lesson-03-install-django-framework): Install Django Framework

<br>

## Lesson 01: Python Virtual Environment
A virtual environment is a Python environment such that the Python interpreter, libraries and scripts installed into it are isolated from those installed in other virtual environments, and (by default) any libraries installed in a “system” Python, i.e., one which is installed as part of your operating system.

A virtual environment is a directory tree which contains Python executable files and other files which indicate that it is a virtual environment.
<br><br>

## Lesson 02: Creating `venv` Python Virtual Environment
To create a virtual enviroment, we first need to install python on the main machine. Most personal computers, esecially those running MacOS or Linux distros already have python installed on the machine.
<br><br>

> Python Version

To check the python version installed on your machine, simply open a `Terminal`, `Command Prompt` or `Powershell` (on Windows) and type in `python --version` and check out the result. You may see something similar to what is below:

```
1. $ python --version
2. Python 3.10.0
```
From the above, I typed `python --version` in my Terminal as seen on line **1.** and the `Python 3.10.0` as seen on line **2.** was the output or result. This means that I have Python version 3.10.0 installed globally on my computer.
<br><br>

> Install Python

However, if `python --version` outputs an error that indicats the Python language runtime was not installed on your computer, then you need to install it yourself. To install the Python runtime;

1. Open your web browser and search for Python
2. Or type in the address bar [`www.python.org/downloads/`](https://www.python.org/downloads/)
3. Download the latest for your operating system.
4. Follow the installation process outlined for your operating system
<br><br>

> Creating virtual environments

Creation of virtual environments is done by executing the command venv in your `Terminal`:

```
python3 -m venv /path/to/new/virtual/environment
```

Running this command creates the target directory (creating any parent directories that don’t exist already) and places a `pyvenv.cfg` file in it with a `home` key pointing to the Python installation from which the command was run (a common name for the target directory is `.venv`). It also creates a `bin` (or `Scripts` on Windows) subdirectory containing a copy/symlink of the Python binary/binaries (as appropriate for the platform or arguments used at environment creation time). It also creates an (initially empty) `lib/pythonX.Y/site-packages` subdirectory (on Windows, this is `Lib\site-packages`). If an existing directory is specified, it will be re-used.

On Windows, you can create your virtual environment in the current users path as follows:
```
python3 -m venv c:\Users\Joejo\Envs\DjangoWeb
```
Here, my computer user account name is `Joejo`. Therefore, I'm creating my python environment called `DjangoWeb` and that is in the folder called `Envs`. I choose this approach so I can have multiple python virtual environments in the future, and all of them will be in the `Envs` folder with their respective names.
<br><br>

> Activating and Deactivating the virtual enviroment

Now that we have our virtual environment creating, we need to power it on and install the `Django framework` into it.

Still within the `Terminal`, run the following command to activate the virtual environment (on Linux or MacOS)
```
source /path/to/virtual/enviroment/bin/activate
```
On Windows (just like in my case), run the following command instead.
```
c:/Users/Joejo/Envs/DjangoWeb/Scripts/Activate.ps1
```
**Note:** Don't forget tot replace `Joejo` with your user account name and `DjangoWeb` with the name of the virtual enviroment you created in the previous section.

Observe your terminal for the resulting output. You will notice that, you have `(DjangoWeb)` as the first on the current directory. This means the virtual environment has been activated.