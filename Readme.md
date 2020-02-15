# Flask Intro App
  A simple todo task manager web app.

## Install python3 and pip3

- `$ python3 --version`
- `$ pip3 --version`
- Remove pylint wrong warning or errors in VSCode by:
  - `$ pip install pylint_flask_sqlalchemy` 
  - and add the following line in settings.json
    ```
    "python.linting.pylintArgs": ["--load-plugins", "pylint_flask_sqlalchemy"]
    ```

## Setup work environment

- Install virtualenv: `$ pip3 install virtualenv`
- Create the environment: `$ virtualenv env`
- Activate the environment: `$ source env/bin/activate`
- Install dependencies: `pip3 install flask flask-sqlalchemy'`
- Run applicatoin in virtual env: `python3 app.py`

## Create sqlite database from app.py

  - `source env/bin/active`
  - `python3`

## host on heroku.com
1.Register and install heroku cli tool
- `sudo snap install --classic heroku`
- `$ heroku login`

2.Freeze the requirements in virtual env:
- `pip3 install gunicorn`
- `pip3 freeze > requirements.txt`

3.Create the git repository for heroku
- `git init`
- `git add .`
- `git commit -m "Init the App repository"`

4.Create `Procfile` file(tell heroku what to do) 
- `touch Procfile`
- Add the following content
  ```
  web: gunicorn app:app
  ```

5.Create Heroku App 
- `keroku create domainname`
- `git remote -v`
- `git push heroku master`
