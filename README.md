Breast Cancer Prediction
by Satyajit Pattnaik

* Find the tutorial here: https://www.youtube.com/watch?v=mS8N0eKOD3k&list=PLymcv5WXEpKg14VB_uDEYjruW-VTowEjk&index=2

About Heroku and steps for deployment of a machine learning end-to-end project on this cloud PaaS:
    - Heroku is the first cloud platform as a service (PaaS)

    - as a pre-requisite, we need to fill the requirements.txt file. We can use the below command to find the environment's current package list installed in our system and accordingly fill the requirements.txt: 
	    pip freeze > requirements.txt

    - need to define set of processes/commands that should run beforehand into file named "Procfile"
	    web: gunicorn app:app
	    * web command tells Heroku to start a web server for the application, using gunicorn, 
        * The Gunicorn "Green Unicorn" is a Python Web Server Gateway Interface HTTP server which is used for running our python application instance. 
	    * Our application's name is app.py, we thus set app name to be app as well

