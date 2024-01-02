Important : The functional requirements had some changes and the login features were removed from the project as they proved obselete. (As previously discussed).

Once the file is unzipped, several important components are observed
-Apps.py file
-Datasets used in the project
-Model files (pickle file and notebook file)
-Read me file
-Requirements.txt file
-ENV (Folder containing enviornment variables and other components)
-Static (Folder containing Static variables and other components)
-Templates (Used in project)
-If required restore FPW.bak file to ensure SQL integration to database (One will need to then replace server name with local server name in apps.py (Near pydbc) to run successfully) 
(No manipulations performed using the same in the project performed as they proved redundant)

# Flight Fare Prediction

*Predicting flight prices is a typical example of a time series forecasting issue that looks for patterns in past observations to estimate the future. Today's most well-known websites for booking flights, like Google Flights, provide crucial details on: 
The current fair status: high, low, or fair

Helps determine the ideal time to purchase a flight ticket by providing historical fare trends, predicted future trends, and In this project, we'll create a Python flight fare prediction app that gives the predicted fare for a given set of travel information, including the departure and arrival dates, cities, stopovers, and airline carriers.

# Steps to run Flight Fare App - (on Windows)

* Prerequisites: [Python 3.9](ensure Python is added to [PATH] )

* Open Terminal (Locate target folder containing project documents in your device)
* We will Run Project in Flask (Using PIP + Virtualenv)
* We enter following commands :

pip install virtualenv                                      # install virtual environment        
virtualenv ENV                                              # create virtual environment by the name ENV
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass  # Grants Permission / Access 
.\ENV\Scripts\activate                                      # activate ENV
pip install -r .\requirements.txt                           # install project dependencies
python app.py                                               # run the project
deactivate                                                  # close virtual environment once done

- The dataset used to train model is obtained from kaggle.
- The HTML templates used are obtained from free to use online repositories.  

# Working :

*This is a Python Flask web application that predicts flight prices using a machine learning model.

The machine learning model is loaded from the "c1_flight_rf.pkl" file using pickle.

The user inputs the journey date, departure time, arrival time, airline, and number of stops. These inputs are then processed to extract useful information such as the day and month of the journey, departure hour and minute, arrival hour and minute, duration of the flight, and total number of stops.

The airline input is one of several possible airlines, and each airline is converted to a one-hot encoded format to be used as input to the machine learning model.

The processed inputs are then passed to the machine learning model to predict the flight price, which is then returned to the user as output
