# Pinball automation


This project is about turning an old classic pinball machince, into an automatic pinball beast. It's done by ball detecting sensors
above the flippers, and an Arduino (Nano) activating the flippers via relays.



## Usefull information

### 3D print info:

**Sensor holder**


- Body depth: 10 mm.
- Body height: 7 mm.
- Body lenght: is defined by number number of repeats.

- Divider (the wall between each sensor): 3 mm.

- Screw hole size: 3 mm.

- Cut out length (for sensor): 11 mm.
- Cut out height (for sensor): 5 mm.

### Notes

- The atmega chips only supports internal pull up resistors not pull down

- Diodes used: 1N914

- Arduino used: Arduino nano

- Sensors used: TCRT5000 Module

## To do

- ~~Put pull down resistor on multi sensor board~~
- Find a solution so that you dont accidentally place sensor incorrectly
into multi sensor board
- Find a solution to the sensors activating each other
- Try out other IR senors (Maybe they are rated for longer distances)
- Add OpenScad files for sensor tube
- Make another multi sensor board. With only 4 sensors.
- Make the other side of the pinball machine automatic.

## Log:

### June 20th

- Started on the second multi sensor board. this time only with 4 sensors
with more space between them (3-8 mm). We have found this to be the best
solution.
- Finished the second multi sensor board.
- Build a piece of tree to hold the other sensor board on the flipper machine
- Modified src/pinball.ino to work with both the left and rigth flipper.
this functinality has been there before, but during testing only the right
flipper was active in the src code.
- Tested it out to see it works (It does)
- It could be upgraded, but only using 8 sensors todays results were perfect
the sensors saved the ball about 11 times at max.
- Finished the project and packed it town.
- In the future this project will probably not be updated. Cause we will
be working on other things. I will though probably upload some images of the 
circuits, a photo and a video of the pinball beast operating in the future
- Walked off into the summer sun with the great sattisfaction of having 
worked on this project for a long time and seing it working and calling it
done (for now)

### June 6th

- Printed out 5 more sensor tubes.
- We decided to stick with 4 sensors on one side. To avoid a problem where
the sensors get stuck. These sensor have sensor tubes on them.
- We got it working with 4 sensors on the board. 
**Important**
These 4 sensor work better with sensor tubes on them.

**PROBLEM:**
- We could not make 7 sensor work together. They keep activating each other
We think the cause can be something called hysteresis (google hysteresis
comparator if you dont know what it is).

### May 16th

- Printed 2 sensor tubes (sensor tubes are small rectangular 3d printed objects
which sit on the sensors led module. The goal of the tube is to prevent light
from one sensor reaching another).
OpenScad files for the sensor tubes are coming soon.

- Cut out a new piece of tree to hold the multi sensor board on the
pinball machine and drilled holds for the multi sensor board.
- Added Line sensor (Model number: TCRT5000) datasheet to link to README
- [TCRT5000 Datasheet](https://www.vishay.com/docs/83760/tcrt5000.pdf)

- Added image of line sensor to repo 

**PROBLEM:**
- We found the sensor activating each while testing it on pinball
we are working on a 3D printed object that blocks the light from one sensor
reaching another sensor on the multi sensor board.
- Tobias found the datasheet for the line sensors.
  - The sensors are rated for a distance between 0.2 mm - 15 mm.
  - Their peak distance is 2.5 mm.
  - Our sensors are 33 mm from the playfield of the pinball machine



### May 9th

- Finished multi sensor board
- Put pull down resistor on multi sensor board
- multi sensor board is now fully functional
- We had a problem with the multi sensor board but it was due to a loose connection
- Openscad files for sensor holder and breadboard holder were added to the repository

### May 2nd

- Almost done with multi sensor board
- No problems

### April 25th

- Single sensor works.


**PROBLEMS:**

- Tobias ruined one of the sensors by placing it incorrectly in the multi sensor board. This problem needs to be solved.
- Multi sensor board with diodes dosnt work (Symptom: swithes on and off relay when sensor is not active).

**SOLVED:**

- The multi sensor board now works. We concluded that a pull down resistor is needed, the problem did not occure with just one sensor because,
with only one sensor there were no diode in the way. with the diodes, when no power was coming from the sensor output, the pin was just floating
- We still need to find a solution so that you dont accidentally place the sensor into the multi sensor board incorrectly



