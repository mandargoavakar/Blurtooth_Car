# Blurtooth_Car
ESP32_Bluetooth_Car.ino, is an Arduino sketch designed for controlling a Bluetooth-enabled robotic car using an ESP32 microcontroller. This code leverages the capabilities of the ESP32 to interface with motors and receive commands via Bluetooth, specifically from a gamepad.
Key Components
Motor Control
The sketch defines two motors: a right motor and a left motor. The motor control is facilitated through the following pins:
Right Motor Pins:
Enable Pin: 22
Direction Pins: 16 (forward), 17 (reverse)
Left Motor Pins:
Enable Pin: 23
Direction Pins: 18 (forward), 19 (reverse)
PWM Configuration
The code sets up Pulse Width Modulation (PWM) for speed control:
Maximum Speed: Defined as 255.
Frequency: Set at 1 kHz.
Resolution: Configured to 8 bits.
Functions
rotateMotor(int rightMotorSpeed, int leftMotorSpeed): This function controls the direction and speed of both motors based on the input speed values. It uses digital writes to set the appropriate pins high or low, effectively controlling motor rotation.
setUpPinModes(): Initializes the pin modes for motor control, setting them as outputs and configuring PWM channels for speed control.
setup(): This function is called once at startup. It sets up pin modes and initializes the Bluetooth connection using the Dabble library.
loop(): The main loop continuously processes input from the gamepad. Depending on which button is pressed (up, down, left, or right), it adjusts the motor speeds accordingly to move the car in the desired direction.
Gamepad Integration
The sketch utilizes a gamepad interface through the Dabble library, allowing for intuitive control of the robotic car. The car can move forward, backward, and turn left or right based on user inputs.
