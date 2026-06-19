# WRO-Future-Engineers-2026
Documentation / Dokumentacija / Documentazione
## Team
WROsBros
## Members
While all team members were equally involved in the creation and programming of our robot called Mishek, we were not all for the same things, but we changed roles over time. Members of our team include Noah Markulin, Jakov Gršeta and Marko Mihalić
## Vehicle
First we used 3D printed robots, which showed that it did not work, later we mmade a new one. Our robot Mishko was built mainly by Jakov Gršeta and made out of LEGO bricks. It is capable of moving forward and turning. Also, hard but possible there is a chance it can do parallel parking and avoid obstacles by recongnizing color.
## Competition
1. Open challange
   OBJECTIVE: The vehicle must successfully finish 3 laps on the track.
   
2. Obstacle challange
   
OBJECTIVE: The objective of the challenge is for the autonomous vehicle to complete three laps around the track while following all competition rules.

During the laps, the vehicle must correctly navigate around the traffic signs:
- Red traffic signs must be passed on the right side.
- Green traffic signs must be passed on the left side.

After completing the required laps, the vehicle must perform the parking mission. On the final lap, it must autonomously park in the designated parking spot.
The vehicle must avoid collisions with walls, traffic signs, and parking boundaries while completing the course.


## Mechanical Design

The robot is built according to the WRO Future Engineers rules. It uses a single engine to drive the rear wheels, and with the front wheels it turns using a different engine.
## Dimensions and specifications
Lenght: 30 cm
Width: 16 cm
Weight: 0.6 kg

## Hardware
Controller: LEGO SPIKE Prime Hub
Distance Sensor: LEGO Distance Sensor
Color sensor: LEGO Color Sensor
Driving Motor: LEGO Motor
Steering Motor: LEGO Motor

## Software
# 1. WIRING DIAGRAM / PORT ASSIGNMENT

   
| Component | Device Type | Port | Function |
|-----------|-------------|------|----------|
| Distance Sensor | LEGO SPIKE Prime Distance Sensor | B | Side obstacle detection |
| Distance & Color Sensor | LEGO ColorDistance Sensor | C | Front obstacle detection and distance measurement |
| Driving Motor | LEGO Large Angular Motor | D | Rear-axle propulsion and velocity control |
| Steering Motor | LEGO Medium Angular Motor | E | Controls the steering angle of the front wheels |
| Distance Sensor | LEGO SPIKE Prime Distance Sensor | F | Side obstacle detection |

# 2. Sensor Selection & Placement

We placed the side sensors on the back side near the rear bumper, which can detect obstacles up to 2 meters on each side.

DistanceColor sensor is placed on the back side of the vehicle.

# 3. Obstacle and Parking Logic

Red and Green pillars: When the obstacle is detected within 10 cm, the color sensor evaluates its RGB signature. If the red value is dominant, the motor will immediately steer right, if the green value is dominant, it will steer to the right.

Parking Mission: The software maintans an internal lap counter and upon entering the 3rd, the color scanning begins for the magenta parking barrier. Once it detects that the robot halts and switches to a program designed to park it.



## Development





