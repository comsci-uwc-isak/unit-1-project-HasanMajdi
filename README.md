![CarRental](logo.png)

Car Rental Minimal App
===========================

A car rental management minimal app in Bash.

Contents
-----
  1. [Planning](#planning)
  1. [Design](#design)
  1. [Development](#development)
  1. [Evalution](#evaluation)

Planning
----------
### Definition of the problem 
This will be a bash program that records car information for a car rental office. 
Each car will have its own ID number (license Plate) will be saved into TXT file 
Every car will have its own file with its information, and there is going to be a specific file for all cars trips and info, all data will be installed through online links/USB. 
Another TXT file is going to calculate the history of the car (Km/h) and give the total distance that the car passed.
In summary the program will show the name of the car, the total distance with Km, and number of the trips. 
For documentation READ.ME file will be provided and also bash help.

Design
---------
### First sketch of system 
![CarRental](CSProject.jpg)
**fig. 1** This program shows the main components of the minimal rental app. it includes the Output/Input and actions. 

Development
--------
``` sh 
#!/bash/bin

#This program creatsfile structure for the minimal rental app
echo "start installing"
echo "installing in desktop (default). Press enter"
read
cd ~/Desktop

#create app folder
mkdir RentalCarApp

cd RentalCarApp

mkdir database
mkdir sripts
echo "installation complete successfully"

```
this script meets the requirement of the client for a simple instalation 
however, it 

Evaluation
-----------



