# BARE MINIMUM DJANGO TUTORIAL

i use an apple computer with `homebrew` and `pyenv` 
[please ignore these commands on other systems and feel free to suggest alternate commands that i could add to this tutorial]

homebrew: https://brew.sh/
pyenv: https://github.com/pyenv/pyenv

i have used `Python 3.13.1` and `Django 5.1.5` for this tutorial.
this tutorial should work with other versions as well [if you have success let me know]

COMMANDS:
• create workspace directory named `min_dja_ws`
```
mkdir min_dja_ws
```
• change current working directory to `min_dja_ws`
```
cd min_dja_ws
```
• set python version using `pyenv` https://github.com/pyenv/pyenv
```
pyenv local 3.13.1
```
• check configured python version
```
python -V
```
output:
```
Python 3.13.1
```
• create a python virtual environment name `env` 
```
python -m -venv env
```
• activate the virtual environment
```
source ./env/bin/activate
```
• install `Django` using `pip`
```
python -m pip install Django
```
• check 
```
python -m django --version
```
output:
```
5.1.5
```
• make a directory for our Django project named `min_dja`
```
mkdir min_dja
```
• use `django-admin` to `startproject` named `min_dja_proj` in the new directory named `min_dja`
```
django-admin startproject min_dja_proj min_dja
```
• before we go in look around: list virtual environment and Django code directories, `env` and `min_dja`, in current directory `min_dja_ws`
```
ls
```
output:
```
env	min_dja
```
• change current working directory to `min_dja` 
```
cd min_dja
```
• use `Django`'s `manage.py` to `startapp` named `min_dja_app`
```
python manage.py startapp min_dja_app
```
• before we change any code look around: list Django's `manage.py` file and project and app directories, `min_dja_proj` and `min_dja_app`, in current directory `min_dja_ws`
```
ls
```
```
manage.py	min_dja_app	min_dja_proj
```
• run the development server using Django's `manage.py` command `runserver`
```
python manage.py runserver
```
open a browser and go to:
http://127.0.0.1:8000/
you should see the famous Django rocket !!  🚀🚀🚀🚀
<img width="536" alt="image" src="https://github.com/user-attachments/assets/dc6aa4b1-a668-4ac5-8857-0893cf6d3dfb" />




• 
```
python manage.py runserver
```
