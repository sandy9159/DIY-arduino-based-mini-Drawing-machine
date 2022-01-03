# DIY-arduino-based-mini-Drawing-machine

# How-to-make-Arduino-mini-CNC-plotter-machine

![image](https://user-images.githubusercontent.com/19898602/130724472-a252a63e-2492-451a-be66-375b1137fa5a.png)


Hello friends in this post we will see how to make mini CNC plotter machine using old scrap DVD drives, arduino & L293D motor shield.
In fact in past I have build some arduino mini CNC plotter machine or drawing machine in past.


But those projects are not well documented and unclear so I got many request to make a detail in depth tutorial about how to make arduino based mini CNC plotter machine.
So in this post I an going to cover all points like hardware assembly, code for arduino, processing GUI, G-code generation etc.
So before moving further let me brief you about what is CNC plotter machine is.


# VIDEO

https://youtu.be/Gm6bH3p6cNQ

ARDUINO PROJECT, CNC

How to make Arduino mini CNC plotter machine
Posted by sandeep on September 27, 2019
How to make Arduino Mini CNC plotter machine
How to make Arduino Mini CNC plotter machine

Hello friends in this post we will see how to make mini CNC plotter machine using old scrap DVD drives, arduino & L293D motor shield.
In fact in past I have build some arduino mini CNC plotter machine or drawing machine in past.
But those projects are not well documented and unclear so I got many request to make a detail in depth tutorial about how to make arduino based mini CNC plotter machine.
So in this post I an going to cover all points like hardware assembly, code for arduino, processing GUI, G-code generation etc.
So before moving further let me brief you about what is CNC plotter machine is.





# OVERVIEW


CNC plotter machine is basically a 2.5 axis CNC machine, it have two stepper motor on both X & Y axis and a servo motor at Z axis.
A pen is connected on Y-axis and Z-axis is used to make pun up & down.


As name suggest plotter machine obvious draw or plotting a drawing as per given instruction.
To give instruction to machine what to draw a special type of code called G-code is required.
Image will be converted to G-code with the help of special type of software.


afterwards this G-code sends to controller and controller commands motors how to move.
As result machine will draw image on paper.


Now lets we will see how to build such machine. starting with material list


# MATERIAL LIST

Sr No.	ITEM	QTY


> 1	Scrap DVD Drive	2


> 2	Arduino UNO	1


> 3	L293D MOTOR SHIELD	1


> 4	MINI SERVO MOTOR	1


> 5	5V 1Amps POWER ADAPTER	1


> 6	SOME WIRES FOR MOTOR CONNECTION	—-


> 7	NUT AND BOLTS AS REQUIRED	—-


# SOFTWARE LIST

> 1	[ARDUNIO IDE](https://www.arduino.cc/en/main/software)


> 2	[PROCESSING IDE](https://processing.org/download/)


> 3	[INKSCPAE VERSION 0.48.5](https://inkscape.org/release/inkscape-0.48/?latest=1)


Please download the software from above link, and install them on your PC.

## CODE AND LIBRARY

 > 1	[CNC CODE FOR ARDUINO](https://secureservercdn.net/198.71.233.37/k8u.855.myftpupload.com/wp-content/uploads/2019/09/cnc-code.zip)
 
 
> 2	[GCTRL PROCESSING CODE](https://secureservercdn.net/198.71.233.37/k8u.855.myftpupload.com/wp-content/uploads/2019/09/GCTRL.zip)


> 3	[AFMOTOR LIBRARY FOR ARDUINO](https://github.com/adafruit/Adafruit-Motor-Shield-library/archive/master.zip)


> 4	[Makerboat Gcode Inkscape extension](https://github.com/martymcguire/inkscape-unicorn)



“CNC CODE FOR ARDUINO” needs to be upload on arduino.
“GCTRL” needs to be open in processing software.
“AFMOTOR” library need to add in arduino IDE
how to do all this ? we’ll see further.


## MACHINE ASSEMBLY

Step 1.

![image](https://user-images.githubusercontent.com/19898602/130724853-fabf5ae7-5bb9-48cc-8f99-2f133cf932b7.png)


To make Arduino based mini CNC plotter machine obviously we need two scrap DVD drive.
I purchased this drive from local computer repairing shop in less then 1$ .
we’ll going to use its stepper motor along with sliding mechanism
here note that not all DVD drives have stepper motor in it. if the motor have 4 wires it means it is a stepper motor.
if you not found any 4 wire motor in DVD drive then it is use less.

## Step 2.


![image](https://user-images.githubusercontent.com/19898602/130724892-4a98f113-85b9-477f-8b69-0ddfbd9abb0c.png) ![image](https://user-images.githubusercontent.com/19898602/130724898-cb44f9a7-9165-4f22-89cb-0fcb2dd890ae.png)

![image](https://user-images.githubusercontent.com/19898602/130724908-96bafd99-8fc2-485a-8c8a-8131c8770d63.png)


I quickly unscrew the DVD drive case with the help of screw driver and by applying some force I take out the stepper motor mechanism from the DVD drive case.
In this way I have two stepper driver mechanism and two empty case of DVD drive.

## Step 3.


![image](https://user-images.githubusercontent.com/19898602/130724923-b06c8698-cd6b-4b07-b68c-1b15cde6b8c6.png) ![image](https://user-images.githubusercontent.com/19898602/130724930-14e822a3-4b7e-443d-8bc8-9fb5dc7e31fc.png)


![image](https://user-images.githubusercontent.com/19898602/130724939-d5146c20-5859-4270-ae6e-b57f8da0099c.png)


After taking out stepper motor mechanism I cut the default motor connector strip with the help of scissor.
then I bring some DuPont 4 wire of around 40 cm and cut it into 2 pieces one for each stepper motor connection.


Then I strip the wire carefully without damaging the copper strain of wire.
and solder it to the expose terminals of stepper motor.


 
## Step 4.

![image](https://user-images.githubusercontent.com/19898602/130724953-f3cb5b9f-3a9e-460a-841d-ff34d6fd9155.png) ![image](https://user-images.githubusercontent.com/19898602/130724963-2fa76e8a-90a8-42ca-a1d6-ecebbc5e558b.png)


## Step 5.


Here I have paint the the empty case of DVD drive using gray shade spray paint, this step is not compulsory its ok if you don’t want to paint them.


![image](https://user-images.githubusercontent.com/19898602/130724980-72bd661c-2cd7-4d8f-831c-96556b29700f.png) ![image](https://user-images.githubusercontent.com/19898602/130724997-ef29152f-4f79-4373-adcf-5ffba71bab5e.png)

![image](https://user-images.githubusercontent.com/19898602/130725002-4e147021-97a1-4519-a6d8-554e8b6ae10a.png)


Then I used a piece of 20 x 20 mm aluminium angle to make holder for X-axis and Y-axis .
I drill the 5mm hole on the aluminium piece and cut it into two piece of clamp, further I use this clamp to fix the both axis with the help of M5X10 nut and bolt.

## Step 6.


![image](https://user-images.githubusercontent.com/19898602/130725024-603e1c8e-5c70-4430-a5af-457db4c2740a.png) ![image](https://user-images.githubusercontent.com/19898602/130725032-90b8dc62-a2ac-4a6d-ae1e-fec97db768e6.png)


Now I am marking for hole on DVD drive case to make arrangement for mounting for both stepper motor mechanism.
I carefully drill the hole of 5mm with the help of drill machine.

![image](https://user-images.githubusercontent.com/19898602/130725047-ed4ab95b-42af-4ecd-9a75-7b4fe5c71ff2.png) ![image](https://user-images.githubusercontent.com/19898602/130725053-abbd97a4-7ee7-4461-af4b-d4a2a521bdba.png)

![image](https://user-images.githubusercontent.com/19898602/130725059-8d6796e4-2e54-4054-9e11-a3e72b40f72a.png)


After drilling the hole in DVD drive case I fix the four M4 X 60 nut bolts at the four corner of stepper motor mechanism.
Now I placed the stepper motor mechanism to its place and secure all four bolts with M4 nuts.

Step 8.

![image](https://user-images.githubusercontent.com/19898602/130725079-56096c28-87f9-44f7-a541-31a21207c85b.png)


![image](https://user-images.githubusercontent.com/19898602/130725097-3fad83d9-9519-4a45-8b2b-1938a9d8508d.png)


![image](https://user-images.githubusercontent.com/19898602/130725116-80854bc3-2ce3-4043-a077-b361d9c70fa2.png)


This the is most important step in making mini Arduino CNC plotter machine here we are making pen up and down mechanism.
First I take a compass and carefully remove its pen holder part.
then I used a simple pen with top and bottom openable.


first take out the refill of pen and cut about 2 cm part from the top of the refill.
now I place a spring at the top of the refill which I have salvage from other trigger type pen.


then I used a strong thread and tied it to the center of the refill and secure it with super glue on to its place.
now I make a small hole just above from the center of pen body.


Now I carefully place the refill inside the pen and passed thread outside from the hole.
In this way I made my pen up down mechanism, when I pull the thread pen refill push upward and when I release the thread refill went down.


and due to the spring attached at top of the refill pen tip will maintain a good friction with paper..
Pen is now placed in pen holder and glue it with super glue on the X-axis



![image](https://user-images.githubusercontent.com/19898602/130725134-9b820c5a-18a7-4ea9-86c7-d46e6f106be9.png)
![image](https://user-images.githubusercontent.com/19898602/130725146-b3237359-8467-4517-8f95-ae0439924b06.png)


I attached a mini servo at X-axis and tie the thread with the knob of mini servo motor.


## Step 9.
 ![MVI_0001 00_04_10_14 Still001](https://user-images.githubusercontent.com/19898602/130725538-5a571b08-60c7-4384-999f-682b909b96ce.jpg)
![A1](https://user-images.githubusercontent.com/19898602/122661273-072b8100-d1a6-11eb-83c0-a3c0f18c33e6.JPG)
![GG](https://user-images.githubusercontent.com/19898602/122661293-42c64b00-d1a6-11eb-88f6-bb288238f309.JPG)

Making such projects without PCB is night mare yes trust me
you cannot get wanted result and professional touch in your project if you ignore PCB
So some days back I have developed my Multipurpose PCB. and order it from [JLCPCB](https://jlcpcb.com/IAT )
This PCB is used to build wide range of arduino projects 

[JLCPCB](https://jlcpcb.com/IAT ) is offering affordable rates for quality PCB & if you are first time customer of [JLCPCB](https://jlcpcb.com/IAT )
there are some welcome offors for you so don't miss then visit now **[JLCPCB](https://jlcpcb.com/IAT )**

This PCB is specialy designe for CNC machine it have two L293D IC which control two stepper motors
and provision for micro servo motor



![image](https://user-images.githubusercontent.com/19898602/130725979-483863b4-c32e-418b-aa6b-54e3c817b589.png)

We are using Arduino UNO as a brain of CNC machine, as we know there is stepper motors used in CNC machine.
Stepper motors are not easy to control so here we are using a L293D motor shield to control our stepper motors and one servo motor is used for pen up down movement.

Before start wiring first we nee to the know the correct wire of stepper motor.
Our stepper motor have 4 wire and stepper motor have two coils means the a set of two wire is form one coil.

so we need to find out which two wires are from one coil, so here I am using multimeter keeping multimeter on continuity test.
I connect the mutimeter prob to the wires one by one, if I get continuity( few ohms) between any two wires means that both wires belong to single coil and rest two are from other coil.

# ARDUINO CODE


Hope you have downloaded the arduino code and library from above in post if not, don’t worry you can download it from the below links.
Arduino code
AFMotor Library
First of all we need to install AFMotor library in arduino IDE if you dont know how to add library just google it.

Now simple upload the code without changing anything

Here I am explaining some important part of code which may useful for you

Followings are the servo up down values Increase or decrease if required. if servo works in opposite direction switch the value of punZUp & penZDown values.


```cpp
// Servo position for Up and Down 
const int penZUp = 120;
const int penZDown = 50;
```


Below are the value to change the speed of cnc plotter machine youcan change the the value of StepDelay from 0 to 2,
0 is for maximum speed and 2 is for minimum speed, ideally keep it at 1.

```cpp
float StepInc = 1;
int StepDelay = 1;
int LineDelay =0;
int penDelay = 50;
```


If your plotting area is bigger then you can change the Xmax & Ymax value from here.

```cpp
float Xmin = 0;
float Xmax = 40;
float Ymin = 0;
float Ymax = 40;
float Zmin = 0;
float Zmax = 1;
```


![MVI_0001](https://user-images.githubusercontent.com/19898602/130726827-331c2686-1ed6-4844-9473-29e75d4c6b84.gif)




