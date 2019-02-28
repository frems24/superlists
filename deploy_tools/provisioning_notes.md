Provisioning a new site
=======================

## Required packages:

* nginx
* Python 3.6
* Pipenv
* Git

eg, on Ubuntu:

    sudo add-apt-repository ppa:deadsnakes/ppa
    sudo apt update
    sudo apt install nginx git python36 python3.6-venv

## Nginx Virtual Host config

* see nginx.template.conf
* replace DOMAIN with, e.g., staging.my-domain.com

## Systemd service

* see gunicorn-systemd.template.service
* replace DOMAIN with, e.g., staging.my-domain.com

## Folder structure:

Assume we have a user account at /home/username

    /home/username
    └── ottg
        ├── DOMAIN1
        │    ├── .env
        │    ├── db.sqlite3
        │    ├── manage.py etc
        │    ├── static
        │    └── Pipfile etc
        └── DOMAIN2
             ├── .env
             ├── db.sqlite3
             ├── etc