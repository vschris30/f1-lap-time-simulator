# 🏎️ Minimum Lap Time Simulator 

A physics-informed Python simulation that estimates the minimum achievable lap time for a Formula 1 car — specifically the **Red Bull Racing RB20 (2024)** — on a defined race circuit. This simulator models real-world forces such as aerodynamics, tire grip, ERS deployment, and braking dynamics to produce detailed lap analytics.

---

## 🎯 Objective

To simulate the fastest possible lap using:

- ✅ Aerodynamic downforce & drag modeling
- ✅ Traction-limited acceleration and braking zones
- ✅ Cornering limits based on curvature & grip
- ✅ Tire temperature & grip degradation
- ✅ ERS energy deployment and harvesting
- ✅ Sector time analysis and lap delta plots

## 🗺️ Track Input File (CSV Format)
Copy
Edit
Monaco_Track.csv
Column	Description
x_m, y_m	Centerline coordinates (meters)
w_tr_left_m	Track width to the left (meters)
w_tr_right_m	Track width to the right (meters)


## 📦 Project Overview

This simulator replicates a Formula 1 car's behavior over a racing lap using accurate physical modeling. It simulates:

- Aerodynamic downforce & drag
- Lateral and longitudinal dynamics
- Tire heating and grip degradation
- Energy Recovery System (ERS) deployment
- Braking performance & weight transfer
- Throttle and gear behavior
- Fuel burn and battery mass variation


---

## ⚙️ Car Modeled: Red Bull RB20 (2024)

| Component | Value |
|----------|-------|
| Power Unit | 850 kW (~900 bhp) hybrid V6 Turbo + ERS |
| Mass | 798 kg (FIA minimum) |
| Aerodynamics | Cd = 0.68, Cl = 3.2 |
| Peak Tire Grip | μ = 1.9 |
| Max Braking | 5.8 g |
| ERS Power | 160 kW with 4.5 MJ storage |
| Gearbox | 8-speed sequential |
| Dimensions | Wheelbase: 3.6 m, Width: 2.0 m |

---

## 🧠 Core Simulation Workflow

1. **Track Processing**: Import track data with centerline coordinates.
2. **Trajectory Smoothing**: Reduce curvature noise via filtering.
3. **Curvature Estimation**: Determine turning radii for every segment.
4. **Speed Profiling**:
   - Lateral grip-limited max speed
   - Forward acceleration (power-limited)
   - Backward deceleration (brake-limited)
5. **Thermal & Energy Modeling**:
   - Tire heating and degradation
   - ERS energy usage and recovery
   - Fuel burn and battery weight impact
6. **Lap Time Integration**: Distance-based time summation.
7. **Visualization**: Generate rich plots for analysis.

---

## 📊 Visual Outputs

| Plot                              | Description                              |
| --------------------------------- | ---------------------------------------- |
| 🟦 Speed vs Distance              | Braking zones and straights performance  |
| 🟩 Longitudinal Acceleration      | Shows throttle and brake balance         |
| 🌀 Lateral G-Force                | Cornering force and grip analysis        |
| 🔴 Tire Temperature Profile       | Thermal performance of tires             |
| ⚡ ERS Usage vs Distance           | Deployment and harvesting logic          |
| 🧲 Downforce vs Distance          | Aero load variations with speed          |
| 🟠 Grip Force Curve               | Tire friction availability vs usage      |
| ⏱️ Lap Time Delta / Sector Splits | Time gain/loss insight                   |
| 📐 Curvature Profile              | Track shape analysis                     |
| 🧪 Optimal vs Actual Speed        | Grip-limited vs theoretical speed        |
| 🗺️ Track Map Colored by Speed    | Visual lap path with performance overlay |
| 🛞 Grip Degradation               | Tire wear and performance drop           |
| 🚦 Throttle & Brake Zones         | Driving behavior per corner              |




