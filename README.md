# BARE MINIMUM DJANGO TUTORIAL [ [60 SECONDS](#lightning-speed) ⚡⚡⚡⚡ ]

i use the default z shell `zsh` in the apple computer `terminal` with `homebrew`, `pyenv` and `vscode`

[ please ignore the system specific commands on other systems and feel free to suggest alternate commands that i could add to this tutorial ]

i have used `Python 3.13.1` and `Django 5.1.5` for this tutorial.

this tutorial should work with other versions as well 

[ if you have success let me know ]

[ see links at the bottome of the page ]

let's get started !!

🐍🐍🐍🐍

---

#### COMMANDS:

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
• run the development server using Django's `manage.py` command `runserver`
```
python manage.py runserver
```
open a browser and go to:

http://127.0.0.1:8000/

you should see the famous Django rocket !!

🚀🚀🚀🚀

<img width="536" alt="image" src="https://github.com/user-attachments/assets/dc6aa4b1-a668-4ac5-8857-0893cf6d3dfb" />

---

#### CREATE DJANGO APP
• use `Django`'s `manage.py` to `startapp` named `min_dja_app`
```
python manage.py startapp min_dja_app
```
• before we change any code look around: list Django's `manage.py` file and project and app directories, `min_dja_proj` and `min_dja_app`, in current directory `min_dja_ws`
```
ls
```
output:
```
manage.py	min_dja_app	min_dja_proj
```

open this file:

`min_dja_ws/min_dja/min_dja_proj/settings.py`

you can comment out everything except these 3 lines or you can even just replace the file contents with this:
#### settings.py
```
SECRET_KEY = 'django-insecure-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX'  # use your autogenerated secret key

DEBUG = True

ROOT_URLCONF = 'min_dja_proj.urls'

```
open this file:

`min_dja_ws/min_dja/min_dja_app/views.py`

replace the contents with this code:
#### views.py
```
from django.http import JsonResponse


def heyo(request):
    return JsonResponse({
        "heyo": "multiverse",
        "request.GET": request.GET,
    })

```
open this file:

`min_dja_ws/min_dja/min_dja_proj/urls.py`

replace the contents with this code:
#### urls.py
```
from django.urls import path

from min_dja_app import views


urlpatterns = [
    path('heyo/', views.heyo)
]

```
• run the development server using Django's `manage.py` command `runserver`
```
python manage.py runserver
```
open a browser and go to:

http://127.0.0.1:8000/heyo/

you should see the JSON response from your API's end point:
```
{
"heyo": "multiverse",
"request.GET": {}
}
```
try adding some key value parameters to the URL query string

http://127.0.0.1:8000/heyo/?alligator=bear&cat=dog&wolf=xenops&yak=zebra

you should see the JSON response from your API's end point echo back key values from your request's query string:
```
{
  "heyo": "multiverse",
    "request.GET": {
      "alligator": "bear",
      "cat": "dog",
      "wolf": "xenops",
      "yak": "zebra"
    }
}
```
that's about it

enjoy !!

[ try [LIGHTNING SPEED](#lightning-speed) below: 60 SECONDS ⚡⚡⚡⚡ ]

---

#### DJANGO PROJECT FILE STRUCTURE:

`min_dja_ws/min_dja`:
```
min_dja % tree .    
.
├── manage.py
├── min_dja_app
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── migrations
│   │   └── __init__.py
│   ├── models.py
│   ├── tests.py
│   └── views.py  ** WE CHANGED THIS FILE
└── min_dja_proj
    ├── __init__.py
    ├── asgi.py
    ├── settings.py  ** WE CHANGED THIS FILE
    ├── urls.py  ** WE CHANGED THIS FILE
    └── wsgi.py

```

---

# LIGHTNING SPEED: [ 60 SECONDS ]

⚡⚡⚡⚡

i was able to copy, paste and run these commands in one go in my terminal, change the files, and launch the development server to complete this tutorial in lightning speed ....
```
mkdir min_dja_ws
cd min_dja_ws
pyenv local 3.13.1
python -m -venv env
source ./env/bin/activate
python -m pip install Django
mkdir min_dja
django-admin startproject min_dja_proj min_dja
cd min_dja
python manage.py startapp min_dja_app
```
• change the 3 files:
```
min_dja_ws/min_dja/min_dja_proj/settings.py
min_dja_ws/min_dja/min_dja_app/views.py
min_dja_ws/min_dja/min_dja_proj/urls.py
```
• run this command: 
```
python manage.py runserver
```
• test in browser:

http://127.0.0.1:8000/heyo/?alligator=bear&cat=dog&wolf=xenops&yak=zebra

now that's really it

ENJOY !!!!

---

PYTHON IS THE GREATEST !!!!

🐍🐍🐍🐍

DJANGO IS THE GREATEST !!!!

🚀🚀🚀🚀

YOU ARE THE GREATEST CODER THAT EVER LIVED !!!!

⚡⚡⚡⚡

#### LINKS:

###### Django:

https://www.djangoproject.com/

###### Python: [ i use `pyenv` below to install python ]

https://www.python.org/

###### Homebrew: [ i use Homebrew to install pyenv ]

https://brew.sh/

###### pyenv: [ manage multiple versions of python on your computer ]

https://github.com/pyenv/pyenv

###### vscode:

https://code.visualstudio.com/

###### vscodium: [ open source builds of vscode; i have used both ]

https://vscodium.com/

