# 🌞 Solar Tracker Simulation (MATLAB Simulink)

This project simulates a solar panel tracking system using MATLAB Simulink. The goal is to maximize solar energy harvesting by dynamically adjusting the panel angle using a PID-controlled motor model, based on the sun’s position calculated from time and latitude.

---

## 📁 Project Files

| File | Description |
| `SolarTracker.slx` | The main Simulink model |
| `solar_tracker_script.m` / `.mlx` | MATLAB script to initialize parameters and run the simulation |
| `README.md` | Project documentation |

---

## ⚙️ Features

- ☀️ Realistic solar irradiance model using latitude (Hyderabad) and time of day  
- 🧮 Dynamic power calculation based on panel area and efficiency  
- 🎯 PID controller to track optimal panel angle  
- 🔁 Motor delay simulated using transfer function `1/(0.5s + 1)`  
- 📊 Scope outputs for visualizing power and panel angle

---

## 🧪 How to Run

1. Open `solar_tracker_script.m` in MATLAB.
2. Run the script to initialize the workspace and launch the model.
3. In Simulink, press **Run** to simulate a full day (86400 seconds).
4. Open the scopes to view:
   - Power output over the day
   - Panel angle tracking response

---

## 📈 Sample Output (Optional)

You can log and plot panel angle (`theta`) and power output in MATLAB using:

```matlab
theta = simOut.logsout.getElement('theta');
plot(theta.Values.Time / 3600, theta.Values.Data);
xlabel('Time (hours)'); ylabel('Panel Angle (rad)');
