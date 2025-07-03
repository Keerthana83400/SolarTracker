🌞 Solar Tracker Control System
This project implements a solar tracking system that dynamically orients a solar panel to follow the sun's position using a PID-controlled motor. It leverages Simulink, Simscape Multibody, and Simscape Electrical for modeling the mechanics, electrical motor, and control logic.

📁 Repository Contents
File	Description
SolarTracker.slx	Simulink model of the solar tracker
solar_tracker_setup.m	Initializes variables like irradiance, panel area, PID values
sun_position_algorithm.mlx	Calculates realistic solar position using location and time
SolarTracker.zip	Compressed version of the full simulation project
README.md	Project overview and instructions

✅ Features
🌐 Location-based solar irradiance modeling (Hyderabad example)

⚙️ Simscape Multibody: Models real-world mechanical rotation of the panel

🔌 Simscape Electrical: Simulates a motor driving the panel

🧠 PID Controller: Ensures precise tracking of the sun’s path

📊 Scope Outputs: Visualize panel angle, sun position, and power generation

🗂️ Clean project structure for easy simulation and sharing

⚙️ How It Works
Sun Position Algorithm: Calculates solar elevation for 24 hours using time and latitude.

Irradiance Modeling: Uses elevation to determine realistic solar irradiance curve.

Power Calculation: Uses panel area and efficiency to compute power.

PID Controller: Adjusts motor signal to track the optimal panel orientation.

Simulation: Shows real-time panel behavior and power output in Simulink.

🛠️ How to Run the Project
Open MATLAB and run:

matlab
Copy
Edit
solar_tracker_setup
Open Simulink, then open SolarTracker.slx.

In the "From Workspace" block, ensure irradiance_data is the variable name.

Click Run to simulate. Observe:

PowerScope: Solar power output

PIDScope: PID controller output

Panel Angle: Actual vs. desired sun angle

📈 Future Enhancements
Dual or triple axis tracking system

Real solar position API or SPA library

Machine learning-based trajectory prediction

Battery storage and inverter integration

Fault detection and automatic recovery
