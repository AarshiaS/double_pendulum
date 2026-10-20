# double_pendulum
# Double Pendulum Simulation

An interactive, browser-based double pendulum simulation that explores **chaotic motion, nonlinear dynamics, and sensitivity to initial conditions**. Built using HTML, CSS, JavaScript, and HTML5 Canvas, the project numerically solves the coupled equations of motion and visualizes the results in real time.

## Features

- **Live animation:** Watch a double pendulum move and trace the path of its second bob.
- **Interactive controls:** Drag either bob to change its starting angle, or adjust both initial angles using sliders.
- **Customizable physics:** Change both masses, rod lengths, gravity, and damping.
- **Numerical methods:** Compare fourth-order Runge–Kutta (RK4) and Euler integration, with selectable time steps.
- **Chaos comparison:** Simulate two pendulums with a tiny initial angular offset and observe how their motion diverges.
- **Real-time readouts:** View elapsed simulation time, angles, angular velocities, total energy, and energy drift.
- **Live plots:** Explore total, kinetic, and potential energy over time; angle versus angular velocity in phase space; and the logarithmic divergence between two pendulums.
- **Six presets:** Gentle, Wild, Chaos test, Nearly upright, Normal mode 1, and Normal mode 2.
- **Responsive interface:** Adapts to different screen sizes and supports light and dark color schemes.

## Getting Started

No installation, build process, or backend is required.

1. Download or clone this repository.
2. Open `double_pendulum.html` in a modern web browser.
3. Experiment with the presets and controls.

The simulation is contained in a single HTML file. An internet connection may be needed to load the optional Google Fonts.

## How to Use

1. Use **Play/Pause** to control the animation and **Reset** to restart from the selected initial conditions.
2. Select a preset or drag a pendulum bob to change its starting position.
3. Adjust masses, lengths, gravity, damping, and starting angles using the controls.
4. Switch between **RK4** and **Euler** or change the time step to compare numerical behavior.
5. Enable **Compare two pendulums** (or select **Chaos test**) to visualize sensitivity to a small difference in starting angles. Change the angular offset in degrees to experiment further.
6. Observe the energy, phase-space, and divergence plots below the animation.

## Physics and Numerical Methods

A double pendulum consists of two masses connected by rigid rods, with the second rod attached to the first mass. Its coupled, nonlinear equations of motion can produce complex and chaotic behavior: nearly identical initial conditions may lead to very different trajectories over time.

The simulation represents its state using the two angles and two angular velocities:

`[θ₁, θ₂, ω₁, ω₂]`

It calculates angular accelerations from the equations of motion and advances the state with either:

- **RK4 (default):** A fourth-order Runge–Kutta numerical integration method.
- **Euler:** A simpler integration method, useful for observing the effect of numerical error and energy drift.

The energy graph displays kinetic energy (T), potential energy (V), and their sum (E). For the ideal undamped system, total mechanical energy should remain approximately constant; damping causes it to decrease.

### Model Assumptions

- Rigid, massless rods and point masses
- Frictionless joints and no air resistance
- Constant gravitational acceleration
- Optional damping torque proportional to angular velocity
- Zero potential energy when both bobs hang vertically downward

## Technologies Used

| Technology | Purpose |
| --- | --- |
| HTML5 | Page structure and controls |
| CSS3 | Responsive layout and light/dark themes |
| JavaScript | Physics calculations, interaction, and animation |
| HTML5 Canvas | Pendulum rendering and live graphs |

No external JavaScript libraries are required.

## Project Structure

```text
Double-Pendulum-Simulation/
├── double_pendulum.html   # Simulation, styling, physics, and visualizations
└── README.md              # Project documentation
```

## Educational Purpose

This project provides a visual way to explore nonlinear mechanics, chaotic systems, energy conservation, numerical integration, phase-space trajectories, and sensitivity to initial conditions.
