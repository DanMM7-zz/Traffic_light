# Traffic_light


### Features remote controlled button to start or stop the system

![Application Demo](/App.jpg?raw=true "Application Demo")

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

How does it work?
There are three major components in the platform:
Blynk App - allows to you create amazing interfaces for your projects using various widgets we provide.
Blynk Server - responsible for all the communications between the smartphone and hardware. You can use our Blynk Cloud or run your private Blynk server locally. It’s
open-source, could easily handle thousands of devices and can even be launched on a Raspberry Pi.
Blynk Libraries - for all the popular hardware platforms - enable communication with the server and process all the incoming and outcoming commands.
Its features:
*Supports majority of development boards like Arduino ,RPI, esp8266
* Easy to use
* Awesome widgets like LCD, push buttons, labelled value, graphs
* Not restricted to local Wifi network
* Direct pin manipulation with no code writing
* Easy to integrate and add new functionality using virtual pins
* 
I guess this should be more than enough to build the project:)

### Prerequisites

1. Smart Phone with Blynk App installed
Note : You better charge your mobile before use:)
2. Led with an 330 ohm resistor
3. Breadboard
4. Arduino IDE 
5. Arduino UNO
6. Raspberry Pi
And that's pretty much the list to be satisfied!!

### Installing

Clone this repository by running

```
git clone https://github.com/DanMM7/Cobra.git
```

Setting up Blynk with Arduino IDE

```
This blynk app has set of library files which have to be included in the Arduino IDE environment before the project is executed
1. Follow the link to install libraries
http://www.blynk.cc/getting-started/
2. Once the Zip file is downloaded ,extract it and individually copy all the folder to your libraries folder of your arduino
3. Once done just open Arduino IDE and go to Sketch-> Include libraries and you would see blynk in the menu
4. If you see that then libraries have been included successfully
*Now it is time to include the board configuration in the Arduino IDE
What is board configuration?
Ok , a simple answer is that it contains all the essential parameters which required to get the board booted and configured.
for example in if you go to Tools->Board Menu you would see a list of boards . All this boards listed have different configuration settings. Therefore we should also include
NodeMCU's board configurations which typically contain the board architecture , clock speed, baud rate etc.
Lets start. In the Arduino IDE go to File->Preferences
Now Copy the below link and paste it in the Additional Boards Manager Url text box
http://arduino.esp8266.com/stable/package_esp8266c...
Restart the Arduino IDE after that.
Now after restarting the Arduino IDE , go to Tools->Boards and select Node MCU board , mine was version 0.9
```
![Application Demo](/setupIDE.jpg?raw=true "Application Demo")


Setting up Blynk

```
1. First install the Blynk app from google play store and then sign in
2. After that Press on click on New Project and you will get a screen (Refer Screen shots)
    *Enter the name of your project, I have given it as led
    *Then Select the Board as ESP8266 and then you will see below the authentication token no. If you want it in your email you can send it through email also
    *And then Finally click on to the create button
3. Now you will get your dashboard screen. Just click on the the top most button "+" on the right corner to add widgets to your project.
4. In this project we add a simple button and then configure its settings as Digital GP13 pin.(Refer Screen Shots)
5. Its your choice you can either have the button set as push type or as a switch
6. Then label the Button as ON and OFF in the settings
Note that since Blynk is free only to an extend, you have to choose your widgets wisely
```
![Application Demo](/setupBlynk.jpg?raw=true "Application Demo")


Circuit Diagram

![Application Demo](/Diagram.jpg?raw=true "Application Demo")


Uploading the Code

```
1. Connect your Esp8266 Wifi to your PC
2. Open Arduino IDE
3. Then go to File->Eamples->Blynk-Boards_Wifi->Esp8266Standalone
   (Refer screenshot)
4. Select the correct board (NodeMCU 1.0) and the com port from the Tools Menu
5. A snippet from the code
   Serial.begin(9600); // Change Baud Rate to 115200
   Blynk.begin(auth, "ssid", "pass"); // Enter your Wifi SSID and password, both inside the double quotation
   Finally Save the file and Press Upload
```
![Application Demo](/Upload.png?raw=true "Application Demo")


Then run

```
1. After uploading the code
2. Open the Blynk app in the Phone
3. Let it connect to the internet
4. Then you would see your dashboard with a button
5. Press Play button on the top most right corner of the app
6. Then Alas!! Press the Button and you would see the LED Turn ON!!!:)
   Now that you have got the basics , you can try some cool stuffs with this awesome board !!
   Have fun exploring this board :)
```
![Application Demo](/Auto-Lights.gif?raw=true "Application Demo")
