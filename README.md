🤖 Maze Solver/ Meshmerise /Autobot
A self-navigating robot designed to solve line-based mazes using infrared sensors and a logical path-finding algorithm.

🛠 Hardware Components
Microcontroller: ESP32

Sensors: QTR-8A IR array

Motors: 2x N20 Micro Gear Motors

Motor Driver: TB6612FNG

Power: 3s Lipo Battery

📐 Circuitry
The brain of the bot connects the sensors to the motor driver via the microcontroller.

🧠 How it Works
This bot uses a Line Following base with Maze Solving Logic:

Line Following: Uses PID control (or simple thresholding) to stay on the black line.

Intersection Handling: When the bot hits a junction (T-junction, Dead end, or Cross), it follows the LSRB or RSLB (Right first, then straight, left then back) algorithm.

Optimization: It simplifies the traverseed path and finds out the shortest path and uses it for the final run

💻 Software Setup
Environment: Built using the Arduino IDE / VS Code PlatformIO.

Libraries: * QTRSensors (if using Pololu sensors), Sprkfun library for Tb6612fng

Upload:

Open MazeSolver.ino in your IDE.

Select your board and port.

Click Upload.

![Circuit Diagram](./circuit.png)
