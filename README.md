# Video search engine

Flask-based application using MySQL, MongoDB and Neo4j for storing video data and provides interface to search video and show related videos and recommendations.

## Setup

* Install python3, pip, python-virtualenv
    ```
    sudo apt-get install python3 python3-pip
    pip3 install virtualenv
    ```
* Install databases : MySQL, MongoDB, Neo4j
  - MySQL
    ```
    sudo apt-get install mysql-client mysql-server libmysqlclient-dev
    ```
  - MongoDB
    ```
    sudo apt-get install mongodb
    ```
  - GUI for MySQL
    ```
    sudo apt-get install mysql-workbench
    ```
  - GUI for MongoDB : Robomongo
* Clone repository and setup virtualenv inside folder
  ```
  git clone https://github.com/nitish6174/video-search-engine
  cd <downloaded project path>
  virtualenv -p python3 venv_py3
  ```
* Setup SCSS compiler using gulp
  ```
  sudo apt-get install nodejs nodejs-legacy npm
  npm install .
  ```
* Install pip dependencies inside virtualenv
  ```
  source venv_py3/bin/activate
  pip install -r requirements.txt
  ```
* Make config file and modify it
  ```
  cp flaskapp/config.py.example flaskapp/config.py
  ```
* Add video data in the root of repository as the folder name ```data/```
  Sample data files available at [this link](https://goo.gl/gZHPL8)

* Running :
  - Make sure databases are up
  - Export the flask variable with ```export FLASK_APP=./flaskapp/app.py```
  - Init the DB models with ```flask create_db```
  - Run gulp to compile CSS ```gulp```
  - Run server with ```./run.sh```
  - Project will be available at ```localhost:5000```
  - Use ```Ctrl-C``` to stop flask server
  - Use ```deactivate``` to exit virtualenv
