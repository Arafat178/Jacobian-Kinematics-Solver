# Jacobian Kinematics Solver

A web-based step-by-step solver for robotic manipulator kinematics using Denavit-Hartenberg (D-H) parameters.

It computes:

* Forward Kinematics
* Jacobian Matrix
* Inverse Jacobian / Pseudoinverse
* Joint Velocities for a desired end-effector differential motion
* Singularity Detection
* PDF Export of the full solution

Built with pure HTML, CSS, and JavaScript. No installation required.

---

## Live Features

*  Supports **1 to 6 DOF** serial robots
*  Supports **Revolute** and **Prismatic** joints
*  Accepts **Standard D-H Parameters**
*  Works with **Degrees** or **Radians**
*  Shows **step-by-step mathematical derivation**
*  Displays matrices using **MathJax**
*  Automatically uses:

  * Standard inverse for non-singular 6×6 Jacobians
  * Moore-Penrose pseudoinverse for singular or non-square Jacobians
*  Detects singularities
*  Export complete solution to PDF
*  Dark/Light mode

---

##  Mathematical Capabilities

### 1. Forward Kinematics

Computes the homogeneous transformation matrix:

{}^0T_n=A_1A_2\cdots A_n

### 2. Jacobian Matrix

Constructs the manipulator Jacobian:

J\in\mathbb{R}^{6\times n}

### 3. Inverse Differential Kinematics

Solves:

\dot{q}=J^{-1}D\quad\text{or}\quad\dot{q}=J^{+}D

where

D=[dx;dy;dz;\delta x;\delta y;\delta z]^T

---


## Technologies Used

* HTML5
* CSS3
* JavaScript (Vanilla)
* [Math.js](https://mathjs.org?utm_source=chatgpt.com)
* [MathJax](https://www.mathjax.org?utm_source=chatgpt.com)
* [html2pdf.js](https://ekoopmans.github.io/html2pdf.js/?utm_source=chatgpt.com)

---

##  How to Use

1. Download or clone this repository.
2. Open `DHtoJacob.html` in any modern web browser.
3. Select the number of joints (1–6).
4. Enter the D-H parameters.
5. Choose angle unit (Degree or Radian).
6. Enter the desired differential motion.
7. Click **Solve Step by Step**.
8. Optionally export the results to PDF.

---

## 📸 Output Includes

* Input D-H table
* Individual transformation matrices `A_i`
* Forward kinematics matrix `{}^0T_n`
* Intermediate matrices for Jacobian construction
* Jacobian columns
* Full Jacobian matrix
* Desired differential motion vector
* Inverse Jacobian or pseudoinverse
* Final joint velocities

---

##  Notes

* The solver is highly accurate for most serial manipulators.
* Supports both square and non-square Jacobians.
* Automatically handles singular configurations using the Moore-Penrose pseudoinverse.
* Current implementation works best for educational and research purposes.

---

##  Applications

* Robotics coursework
* Kinematics assignments
* Jacobian analysis
* Singularity studies
* Differential motion control
* Academic demonstrations

---



##  Author

**Arafat**
Mechanical Engineering Student
