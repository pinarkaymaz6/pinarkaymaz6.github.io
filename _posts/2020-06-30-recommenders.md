---
title: "Simple Web Application for Data Science Demos"
date: 2020-06-30
tags: [flask, python, gcp]
header:
  image: "/images/recommenders/demo.png"
excerpt: "Python, Flask, Google App Engine"
mathjax: "true"
---

I've been playing around with data science algorithms for a while now. Recently, I watched a tutorial from Pierian Data on Udemy and created a content-based movie recommender. Then I went ahead and built a web application to showcase it. 

In this post, I'll share how you can serve a recommender system with cloud services. If you are also looking for a way to host your model, I hope this post helps you get there. 

The application is live at [http://recommendersystems.appspot.com/](http://recommendersystems.appspot.com/) and you can find the GitHub repository for this demo [here](https://github.com/pinarkaymaz6/Recommender-Systems).

The repo has a structure like this:
![alt]({{ site.url }}{{ site.baseurl }}/images/recommenders/filestructure.png)
You can keep your notebooks and data files under `notebook` folder. These files are not going to be deployed. Everything else is under `recommender` folder which will be deployed to `Google App Engine`. 
#### Get a copy of Recommender-Systems repo
- Go ahead and clone this repo your machine 
```shell
git clone https://github.com/pinarkaymaz6/Recommender-Systems.git
```

#### Run it locally 
Running locally is not a mandatory step, but I highly recommend it. It's easier to save and view your changes, since deployment to cloud takes a few minutes.
- Create a virtual environment and install dependencies
```shell
cd Recommender-Systems/recommender
python3 -m venv FILENAME
source FILENAME/bin/activate
pip install -r requirements.txt
```
- Start the app
```shell
python3 main.py
``` 
Now visit [http://127.0.0.1:8080/](http://127.0.0.1:8080/) to view your application.

#### Deploy to Google App Engine
- First you should create a project on Google Cloud dashboard if you don't have one. You can follow the instructions [here](https://cloud.google.com/resource-manager/docs/creating-managing-projects#creating_a_project?hl=en-GB) to create a project. 
- Install Google Cloud SDK. [Here](https://cloud.google.com/sdk/docs/quickstart-macos) is the guide for macOS. Make sure you initialize the setups by running `gcloud init`.

- Deploy application with your project ID
```shell
gcloud app deploy app.yaml --project PROJECTID
```

Your application should be ready shortly on PROJECTID.appspot.com.

