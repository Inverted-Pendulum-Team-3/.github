Inverted Pendulum Robot 3

A two-wheeled self-balancing robot designed and built as part of the ECEN 403/404 senior capstone sequence. The robot leverages the inverted pendulum principle to maintain upright stability while carrying a 3 lb payload on a 65 cm pendulum, using real-time sensor feedback and a PID control algorithm running on a Raspberry Pi 4.

Overview

The system fuses data from a BNO085 IMU, two AMT10 rotary encoders, and two HC-SR04 ultrasonic sensors into a 100 Hz real-time pipeline via shared memory. A Sabertooth 2x12 motor controller drives two DC motors powered by a 22.2V LiPo battery, with a custom buck converter PCB providing regulated 5V and 3.3V logic rails. A Flask-based web application running on the Raspberry Pi enables remote monitoring, live sensor visualization, and real-time PID gain tuning over Wi-Fi.

The project originally explored a Soft Actor-Critic (SAC) reinforcement learning agent trained in a PyBullet simulation, which achieved a 99% balancing success rate in simulation. Due to real-world sensor noise and hardware latency constraints, the team transitioned to a classical PID controller for hardware deployment.

Key Features

- Real-time self-balancing via PID control
- 100 Hz sensor fusion pipeline using shared memory
- Web-based dashboard for live telemetry and gain tuning
- Ultrasonic obstacle detection for autonomous navigation (stretch goal)
- Custom PCB design for power regulation and logic level conversion

Hardware

- Raspberry Pi 4 (central compute)
- BNO085 IMU (pitch and angular rate)
- AMT10 rotary encoders (wheel velocity)
- HC-SR04 ultrasonic sensors (obstacle detection)
- Sabertooth 2x12 motor controller
- Zeee 6S 22.2V 6000mAh LiPo battery

Software
- Python-based codebase including PID control, sensor drivers, shared memory data fusion, and a Flask web server.
