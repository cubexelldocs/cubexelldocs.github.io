# CubeSolver Camp

An educational Java-based Rubik’s Cube solving robot project built for teaching students how to design, program, and run a physical cube-solving system.

This project was used in a robotics/cubing camp to guide students through:

* Java fundamentals
* Robot control (stepper motors)
* Cube representation and simulation
* Solving using the Old Pochmann method
* (Optional) Computer vision for cube scanning

---

## 🚀 Features

* Full Rubik’s Cube simulation using 3D arrays
* Implementation of Old Pochmann (OP) solving method
* Robot control interface for executing moves
* Vision pipeline (RGB → Lab → classification)
* Example workflows for teaching and learning

---

## 📦 Getting Started

### Prerequisites

* Java (recommended: 17+)
* Gradle (or use included wrapper)

### Run the project

```bash
./gradlew run --args="O Y N"
```

### Arguments

```
ARG1 - Solve method
  B = Beginner
  O = Old Pochmann
  K = Kociemba

ARG2 - Use vision
  Y = Yes
  N = No

ARG3 - Auto-tune colors
  Y = Yes
  N = No
```

Example:

```bash
./gradlew run --args="O Y N"
```

---

## 🧠 How It Works

### Cube Representation

The cube is stored as a 3D array:

```
char[][][] cubeColors;
```

Each face is a 3×3 matrix, and the cube contains 6 faces.

---

### Solving Method: Old Pochmann

The solver:

1. Solves edges using a buffer method
2. Solves corners using a similar cycle-based approach

Core idea:

* Move a piece to buffer
* Apply swap algorithm
* Undo setup moves
* Repeat

---

### Robot Control

Stepper motors execute moves physically.
Prebuilt motor control classes are included so students can focus on logic.

---

### Vision System (Optional)

Pipeline:

1. Capture image
2. Segment cube squares
3. Convert RGB → Lab
4. Compute average color
5. Classify using distance metric
6. Return cube state

---

## 📁 Project Structure

```
cubesolver/
├── core/          # Cube logic, solving algorithms
├── robot/         # Robot + motor control
├── vision/        # Image processing + color detection
├── examples/      # Example usage (Main.java)
├── docs/          # Slides and teaching materials
```

---

## 🎓 Educational Use

This project is designed for:

* Robotics teams (FTC, FRC)
* Programming camps
* Students learning algorithms + hardware integration

---

## 🤝 Contributing

We welcome contributions!

1. Fork the repo
2. Create a branch
3. Make changes
4. Submit a pull request

Please keep code clear and well-documented since this is an educational project.

---

## 📜 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

Built for CubeSolver Camp 2025.
