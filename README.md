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
### Solution proposed
so we decided to use a bash program for the solution because the user asks for something easy and simple.
also we're working on the terminal because its already on the computer.
### Success Criteria
1.A car can be created and stored in the database

2.A car information can be edited

3.A car can be deleted

4.The installation is simple 

5.A summery can be generated for a particular car

6.Trips can be recorded and stored for an existing car.

7.A basic backup plan is available.

Design
---------
### First sketch of system 
![CarRental](CSProject.jpg)
**fig. 1** This program shows the main components of the minimal rental app. it includes the Output/Input and actions. 

### flow diagram for creating a frame in bash terminal
![CarRental](flow.jpg)
**fg. 1**  this program creats a frame in the bash 
# script for frame 
``` sh 

#!/bin/bash

word=$1
len=${#word}
padding=4

echo $len

#lenght of the frame
width=80 
(( spaces=$width/2-$len/2-1 )) #didnt got why //
echo $spaces

#Print a whole line with symbol
for (( i=0; i<$width; i++ ))
do
        echo -n "#"
done
	echo " "  #this is for going down one line

#prints the padding
for (( p=1; p<padding ; p++ ))
do
     echo -n "#"   #how the program show spaces without variable
        for (( s=0; s<$width-2; s++ ))
        do
                echo -n " "
        done
        echo "#"
done

#line for the word
	echo -n "#"
for (( s=0; s<$spaces; s++ ))
do
        echo -n " "
done

if [[ $(( $len % 2 )) -ne 0 ]]; then 
	(( spaces=$spaces-1 ))
fi 

echo -n $word
for (( s=0; s<$spaces; s++ ))
do
        echo -n " "
done
echo "#"

#prints the padding
for (( p=1; p<padding ; p++ ))
do
        echo -n "#"
        for (( s=0; s<$width-2; s++ ))
        do
                echo -n " "
        done
        echo "#"
done

#print bottom frame
for (( i=0; i<$width; i++ ))
do
        echo -n "#"
done
	echo " " #this is for going down one line
  ``` 


Development
--------
### Action: Edit 
Get inputs (license plate)
  
Check arguments and Check if car exists  (ONLY ONE) if not one then show a message to user to enter the right argument 

If one then show a message asking what do you want to edit ? (color, name, model, ect..)

Edit the information 

Save new info 

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

### problem solving 
1 how to detect is a words lenght is odd or even 
```.sh 
if [ $len%2 -eq 0 ]
```
how to create a unistall program 
rm -r app 
Evaluation
-----------
Test 1: A car can be created and sorted in the database 
for this purpose we will create the file testCreate.sh. this is called software testing 
# step1 navigate to the folder containing crete.sh file

first step is to check for the file 
```.sh
cd../scripts/
if [ -f "createe.sh" ]; then
        echo "file exists, test wil start now"
else
        echo "file create.sh does not exist. test failed"
fi
```
here the option -f in the if condition checks for a file in the working folder 

this correspnds to dynamic testing and alpha.

