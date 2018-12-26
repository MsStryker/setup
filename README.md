# Setup for Development Computers

These are the helpful steps I use to setup my local environment for development.

## Libraries

[Git SCM](https://git-scm.com).

Install [Homebrew](https://brew.sh).

    $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

Install [Node](https://nodejs.org/en/):

    $ brew install node

Install [Python](https://www.python.org/downloads/), or install via brew:

    $ brew install python
    
Check you Python version:

    $ python --version
    
If you have a version, then you can install `pip` and `virtualenv` with easy install:

    $ sudo easy_install pip
    
Check your pip version with `pip --version`.

Get your virtual environment:

    $ sudo pip install virtualenv
    
If you are doing any Python Scientific computations, you should look into installing [Anaconda](https://www.anaconda.com).
    
I started with just creating virtualenvs and working on my Python applications in that manner, however using this in a
container is better as it alllows you to deploy to any type of instance and other developers can use the containers in 
their preferred operating system. Plus, if you have a Python application that requires Postgres, Redis, Celery, Celery Beat, and Django, you can have a docker image for each setup and your `docker-compose.yml` will get all these setup for you in one go instead of starting each one separately on your system. Note: more to come on how to do that!

Install [PostgreSQL](https://www.postgresql.org). This has many advantages over MySQL, and some disadvantages, but 
overall it has become my default DB. You can install the [Postgres.app](https://postgresapp.com).

Install with brew:

    $ brew install postgresql
    

### Containers

1. [Docker](https://www.docker.com/products/docker-desktop) because everyone is doing it!

2. Alternatively, you may choose to use [Vagrant](https://www.vagrantup.com).


## IDEs

For my Python applications, install [PyCharm](https://www.jetbrains.com/pycharm/). This is still my top choice for Python!

For my client/front-end code, install [VSCode](https://code.visualstudio.com), with the following extensions:

- Docker
- ESList
- GitLens
- Material Icon Theme
- npm
- Python (optional: `brew install ctags`)


## Linting

Linting makes life easier when you work with a team of developers!

- Python: [Flake8](http://flake8.pycqa.org/en/latest/) and/or [PyLint](https://www.pylint.org).
- JavaScript: [ESLint](https://eslint.org).


## CI/CD (Continuous Integration/Continuous Delivery)

[Jenkins](https://jenkins.io) is my go to choice for running tests and deploying applications as it is: 

- open source
- no additional fees for additional users
- has many many plugins
- security can be managed per user (you should make sure it is secured for authentication)
- you can create a cluster and scale!!!
- you can build for pretty much any application

The downside of Jenkins is that you have to host and configure yourself (unless you have a service that does it), 
but once that is done it is fairly easy to maintain. There are ample resource to help you in the setup process 
should you get stuck!


## Hosting

- [AWS](https://aws.amazon.com) (best documenation IMHO)
- [Google](https://cloud.google.com)
- [Heroku](https://www.heroku.com)
- [Linode](https://www.linode.com)
- [DigitalOcean](https://www.digitalocean.com)
- [Rackspace](https://www.rackspace.com)
etc...


## Notes

AutoFormatting - this should be done with EXTREME care as this can break coding standards (internal and industry) and code in general!!!
