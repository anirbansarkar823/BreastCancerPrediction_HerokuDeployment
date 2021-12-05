**Breast Cancer Prediction - End-to-End Deployment**
    - The target variable 'diagnosis' was having two values 'M' and 'B'. 'M' referring malignant indicates the presence of cancer.

    - Have done feature scaling using Standardization i.e., all the featue values are centered around the mean (mean == 0) with a unit standard deviation

    - Used PCA to decompose the features to less number of features keeping all the variances from featues.

    - Finally used Logistic Regression to do the classification

* Find the tutorial (heroku deployment) by [Satyajit Pattnaik](https://www.youtube.com/watch?v=mS8N0eKOD3k&list=PLymcv5WXEpKg14VB_uDEYjruW-VTowEjk&index=2)

About Heroku and steps for deployment of a machine learning end-to-end project on this cloud PaaS:
    - Heroku is the first cloud platform as a service (PaaS)

    - as a pre-requisite, we need to fill the requirements.txt file. We can use the below command to find the environment's current package list installed in our system and accordingly fill the requirements.txt: 
	    pip freeze > requirements.txt

    - need to define set of processes/commands that should run beforehand into file named "Procfile"
	    web: gunicorn app:app
	    * web command tells Heroku to start a web server for the application, using gunicorn, 
        * The Gunicorn "Green Unicorn" is a Python Web Server Gateway Interface HTTP server which is used for running our python application instance. 
	    * Our application's name is app.py, we thus set app name to be app as well

    - Inside Heroku:
        * create your account
        * connect with github (provide read/write accesses to all your repositories)
        * provide the repository name to connect
        * Then deploy the github branch (master or if anything else). Once deployed, click on "view" to see the deployment.
        * via heroku terminal (which we can download from Heroku website), we can login to see the logs:
            > heroku login
            > heroku logs --app="app_name" > logs_appname.txt

    - My application can be viewed [here](https://breastcancerprediction-heroku.herokuapp.com/)
