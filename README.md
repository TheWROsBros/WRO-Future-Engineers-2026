# WRO-Future-Engineers-2026

Documentation / Dokumentacija / Documentazione

![Mishek](IMG_Front.jpeg)

## Team

**WROsBros**

## Members

All team members were actively involved in the design, construction, programming, and testing of our robot, **Mishek**. Throughout the project, team members frequently changed roles and collaborated on different tasks.

Team members:

- Noa Markulin
- Jakov Gršeta
- Marko Mihalić

## Vehicle

Initially, we experimented with a 3D-printed chassis. However, it proved to be unreliable and difficult to maintain. Therefore, we redesigned the vehicle using LEGO components.

The final vehicle, called **Mishek**, was mainly assembled by Jakov Gršeta and is capable of autonomous navigation, obstacle avoidance, and parking maneuvers.

## Competition

### Open Challenge

**Objective:** The vehicle must successfully complete three laps on the track.

### Obstacle Challenge

**Objective:** The autonomous vehicle must complete three laps around the track while following all competition rules.

During the laps, the vehicle must correctly navigate around the traffic signs:

- Red traffic signs must be passed on the right side.
- Green traffic signs must be passed on the left side.

After completing the required laps, the vehicle must perform the parking mission. On the final lap, it must autonomously park in the designated parking area.

The vehicle must avoid collisions with walls, traffic signs, obstacles, and parking boundaries throughout the run.

## Mechanical Design

The robot is built according to the WRO Future Engineers rules. It uses a single motor to drive the rear wheels and a separate motor to steer the front wheels.

## Dimensions and Specifications

- Length: 30 cm
- Width: 16 cm
- Weight: 0.6 kg

## Hardware

- Controller: LEGO SPIKE Prime Hub
- Distance Sensors: LEGO SPIKE Prime Distance Sensors
- Color Sensor: LEGO ColorDistance Sensor
- Driving Motor: LEGO Large Angular Motor
- Steering Motor: LEGO Medium Angular Motor

## Software

### 1. Wiring Diagram / Port Assignment

| Component | Device Type | Port | Function |
|-----------|-------------|------|----------|
| Distance Sensor | LEGO SPIKE Prime Distance Sensor | B | Side obstacle detection |
| Distance & Color Sensor | LEGO ColorDistance Sensor | C | Front obstacle detection and distance measurement |
| Driving Motor | LEGO Large Angular Motor | D | Rear-axle propulsion and velocity control |
| Steering Motor | LEGO Medium Angular Motor | E | Controls the steering angle of the front wheels |
| Distance Sensor | LEGO SPIKE Prime Distance Sensor | F | Side obstacle detection |

### 2. Sensor Selection and Placement

The side-mounted distance sensors are positioned near the rear section of the vehicle. They are used to measure the distance from nearby walls and obstacles and can detect objects up to approximately 2 meters away.

The ColorDistance Sensor is mounted at the front of the vehicle and is used for obstacle identification and parking detection.

### 3. Obstacle and Parking Logic

#### Obstacle Avoidance

When an obstacle is detected within approximately 10 cm, the ColorDistance Sensor evaluates its RGB values.

- If red is the dominant color, the vehicle passes the obstacle on the right side.
- If green is the dominant color, the vehicle passes the obstacle on the left side.

#### Parking Mission

The software maintains an internal lap counter. After completing the required laps, the vehicle begins searching for the designated parking area.

Once the parking marker is detected, the robot stops and switches to a dedicated parking routine designed to position the vehicle inside the parking zone.

### 4. Navigation Algorithm

The robot uses two ultrasonic sensors mounted on the sides of the vehicle to estimate its position relative to the walls.

During normal driving, the software continuously compares the distance measured by both sensors and adjusts the steering angle to keep the vehicle centered on the track.

When a side wall is no longer detected, the robot recognizes an approaching corner and initiates a 90-degree turn using data from the built-in IMU.

## Development

### First Prototype

Our first prototype was built using 3D-printed parts. Although the design was promising, steering accuracy and overall reliability were insufficient for competition use.

![Old Back](IMG_OldBack.jpg)

![Old Left](IMG_OldLeft.jpg)

![Old Right](IMG_OldRight.jpg)

![Old Top](IMG_OldUpper.jpg)

### Second Prototype

We developed a larger and improved 3D-printed vehicle with better wheel geometry and smoother movement.

Unfortunately, persistent communication issues between the robot and our computer prevented reliable testing and further development. Despite multiple troubleshooting attempts, including updating to Windows 11, the problems remained unresolved.

### 3D Model

![3D Front](IMG_3DFront.jpeg)

![3D Back](IMG_3DBack.jpeg)

![3D Left](IMG_3DLeft.jpeg)

![3D Right](IMG_3DRight.jpeg)

![3D Top](IMG_3DUpper.jpeg)

### Final Robot

As a result, we decided to build an entirely new LEGO-based vehicle named **Mishek**.

The final robot provides significantly improved reliability, easier maintenance, and better integration with the LEGO SPIKE Prime ecosystem.

![Front View](IMG_Front.jpeg)

![Rear View](IMG_Back.jpeg)

![Left Side](IMG_Left.jpeg)

![Right Side](IMG_Right.jpeg)

![Top View](IMG_Upper.jpeg)

## Testing

The robot was tested on multiple track layouts to improve navigation accuracy, corner detection, obstacle avoidance, and parking performance.

Testing focused on:

- Maintaining a centered position on the track
- Detecting corners using side distance sensors
- Correctly identifying red and green obstacles
- Executing consistent 90-degree turns
- Performing autonomous parking maneuvers

## Future Improvements

- More accurate obstacle recognition
- Improved turning precision
- Faster lap completion times
- More reliable parking performance
- Enhanced navigation algorithms
