# Deploy Keras Model with Flask as Web App in 10 Minutes

[![](https://img.shields.io/badge/python-2.7%2C%203.5%2B-green.svg)]()
[![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html)

> A pretty and customizable web app to deploy your DL model with ease

------------------

## Getting started in 10 minutes

- Clone this repo 
- Install requirements
- Run the script
- Check http://localhost:5000
- Done! :tada:

:point_down:Screenshot:

<p align="center">
  <img src="https://s18.postimg.cc/l01x6fn3d/demo1.png" width="600px" alt="">
</p>

------------------

## Docker Installation

### Build and run an image for keras-application pretrained model 
```shell
$ cd keras-flask-deploy-webapp
$ docker build -t keras_flask_app .
$ docker run -d -p 5000:5000 keras_flask_app 
```

### Build and run an image from your model into the containeri.
After build an image as above, and 
```shell
$ docker run -e MODEL_PATH=/mnt/models/your_model.h5  -v volume-name:/mnt/models -p 5000:5000 keras_flask_app
```

### Pull an built-image from Docker hub
For your convenience, can just pull the image instead of building it. 
```shell
$ docker pull physhik/keras-flask-app:2 
$ docker run -d -p 5000:5000 physhik/keras-flask-app:2
```
Open http://localhost:5000 after waiting for a minute to install in the container.


## Local Installation

### Clone the repo
```shell

### Install requirements

```shell
$ pip install -r requirements.txt
```

Make sure you have the following installed:
- tensorflow
- keras
- flask
- pillow
- h5py
- gevent

### Run with Python

Python 2.7 or 3.5+ are supported and tested.

```shell
$ python app.py
```

### Play

Open http://localhost:5000 and have fun. :smiley:

