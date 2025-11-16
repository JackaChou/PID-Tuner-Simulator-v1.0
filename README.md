# PID Tuner Simulator v0.9.0

An interactive, web-based PID tuning simulator with a response optimization auto-tuner. This platform is specifically designed for educational purposes in process control, automation, and related engineering courses.

Developed by **Wenjin Zhou** from Taiyuan University of Technology.

---

## Features

- **Real-time Dynamic Simulation**: Simulate closed-loop PID control and visualize SP, PV, and OP curves dynamically.
- **Manual PID Tuning**: Freely adjust Kc, Ti, and Td parameters to intuitively understand their effects on control performance.
- **One-Click Auto-Tuning**: Utilizes a sophisticated **Response Optimization** algorithm to automatically find the optimal PI parameters for the current process.
- **Switchable Process Models**: Supports two classic process models:
  - **First-Order Process**: `G(s) = 1 / (5s + 1)`
  - **Second-Order Underdamped Process**: `G(s) = 25 / (s² + 3s + 25)`
- **Dead Time Simulation**: Allows setting a process dead time (delay) to study its critical impact on system stability.
- **Purely Web-Based**: Built with standard HTML, CSS, and JavaScript. No installation or plugins are required. It can be easily embedded into digital textbooks, online courses, or presentations.

## How to Use

### A. Manual Simulation

1.  **Set Parameters**: In the "Simulation Input" area, configure the controller parameters (Kc, Ti, Td), select a process model, and set the dead time (Delay).
2.  **Run Simulation**: Click the **"Run Simulation (Manual)"** button to perform a simulation with the current parameters. The results will be plotted in the output area.

### B. Auto-Tuning (Response Optimization)

1.  **Set Process**: Select the desired process model and dead time.
2.  **Start Auto-Tuning**: Click the **"Auto-Tune"** button.
3.  **Observe**: The system will automatically perform a two-stage optimization:
    - **Stage 1**: Identify an approximate process model.
    - **Stage 2**: Run an iterative numerical optimization to find the best PI parameters that minimize a comprehensive cost function (based on ITAE, overshoot, settling time, etc.).
4.  **Get Results**: The optimized `Kc` and `Ti` values will be automatically filled into the input fields, and a new simulation will run to display the excellent control performance.

## For Educators

This tool is designed to be seamlessly integrated into digital learning environments. It transforms static textbook graphs into a hands-on "virtual lab," enhancing student engagement and providing a deeper understanding of PID control theory and practice.

## License & Copyright

&copy; 2023 Wenjin Zhou, Taiyuan University of Technology. All Rights Reserved.

This software is intended for educational and demonstrational purposes only. Commercial use is prohibited without permission.
