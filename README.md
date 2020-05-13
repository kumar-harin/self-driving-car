# self-driving-car

Hi,

This is Harin Kumar

This self driving car is developed by using Machine Learning(ML) and not Artificial Intelligence(AI) . They have subtle differences.
An ML Agent is developed by feeding it the training data and showing it the glimpses of how driving works.
But an AI Agent is directly thrown into the world and it should figure out how driving works by experimenting and exploring.

This is the same process used by TESLA and NVIDIA to design self driving cars.But this process is less complex, takes less time and not as
stable as their processes.

We start off by making a Neural Network, which is basically a bunch of perceptrons connected to one another. A Perceptron is an Artificial Neuron.So, technically, Neural Network is an Artificial Brain.

NOTE: BASIC KNOWLEDGE OF PYTHON AND MACHINE LEARNING IS REQUIRED.

I think its obvious, works only on pc.

first off, download python version 3.5.2 from official website https://www.python.org/downloads/release/python-352/ using this link.
Download the executable installer for your OS and install it.

then open the terminal and execute the followning commands(hit "ENTER" to execute):

    pip3 install numpy
    pip3 install matplotlib
    pip3 install jupyter
    pip3 install opencv-python
    pip3 install pillow
    pip3 install scikit-learn
    pip3 install scikit-image
    pip3 install scipy
    pip3 install h5py
    pip3 install eventlet
    pip3 install flask-socketio
    pip3 install seaborn
    pip3 install pandas
    pip3 install imageio
    pip3 install moviepy
    pip3 install tensorflow==1.1
    pip3 install keras==1.2
    
-Git clone or download this repo into your pc

-Simulator folder contains the car simulator/game

-ML Agent folder contains the ML code required


IF YOU WANT TO MAKE YOUR OWN MODEL DO THE FOLLOWING STEPS OR IF YOU WANT TO DIRECTLY GET INTO SELF DRIVING SCROLL DOWN TO DIRECT SELF DRIVE SECTION:

TRAIN YOUR OWN MODEL:

1)open beta_simulator.exe and select graphics settings(depends on your processor) , check out controls first and select training mode. hit R to start training....select a folder(new or existing) to save the training data(training data is basically your recorded gameplay)...and start driving ....drive like you drive in the real life as this will be recorded and used for the agent...drive around for about 6-10 times around the map.Hit R to stop recording and it will take few minutes to save the data

-training data(driving_log.csv) contains an excel sheets which records camera feed, which is fixed on front side of the car and its velocity, steering angle

2)open ML Agent folder and open model.py and go to def main() function:

the argument in argparser is the location of your saved training data..type in the location there.
Then, open the terminal run this command:
    
    python model.py
    
This starts the training of the model...this takes 30min-8hrs....depends on your processor.
After this is done, a couple of model.h5 files are made in the directory...
At the end of each epoch, model.h5 is saved if it is better than the previous model.
(model-00x.h5, the model with greatest x values is your best model)

3)open drive.py and in if__name__ == " __main__ ":

the first argparser argument is the location of your best model...type in the location
then open the terminal and run the following command:

    python drive.py model-00x.h5
    
choose your best model.
DON'T HIT ENTER YET!!!
open the simulator and select autonomous mode and hit enter in the terminal

and the SELF DRIVING CAR IS ACTIVATED!!!!




DIRECT SELF DRIVE:

If you don't want to make a new model and use my trained model(model-007.h5)
then open the terminal and run the following command:

    python drive.py model-007.h5
    
choose your best model.
DON'T HIT ENTER YET!!!
open the simulator and select autonomous mode and hit enter in the terminal

and the SELF DRIVING CAR IS ACTIVATED!!!!



















    
