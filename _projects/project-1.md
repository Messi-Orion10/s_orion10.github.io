---
title: "Ingenuity"
collection: projects
subject: "Control Problems in Robotics - UAVs - Model Based"
permalink: /projects/project-1
venue: "University 'La Sapienza' of Rome"
period: "Winter - Spring 2023/2024"
paper: "https://messi-orion10.github.io/s_orion10.github.io/files/ingenuity.pdf"
video: "Coming soon"
---

Teaming up with three fellow engineers, I spearheaded the creation of a **high-fidelity Simulink digital twin** of NASA’s historic *Ingenuity* helicopter—the first aircraft ever to achieve powered flight on another planet (Mars, 2021 – 2024).  We began by mining published aerodynamic data, rotorcraft papers, and flight-test logs, then fused them into a six-DOF rigid-body model complete with rotor flapping dynamics, motor time constants, and the true martian ISA atmosphere (≈ 0.016 kg/m³, 3.72 m/s² gravity).

Once the physics were nailed down, we designed and compared two radically different control paradigms:

* **Static feedback-linearisation**—an elegant input-output decoupling scheme that flattened the nonlinear dynamics but struggled to stay robust under martian gusts and actuator saturation.
* **Nonlinear backstepping**—a recursive Lyapunov-based strategy that embraced Ingenuity’s under-actuated nature, chaining stabilising virtual controls all the way from attitude to position.

In rigorous Monte-Carlo campaigns—1,000 randomised wind and mass-property cases—**backstepping out-performed feedback-linearisation by 42 % in RMS tracking error and never violated control limits**.  The final controller executed aggressive climb-turn-descent profiles with under-2 cm lateral deviation, proving that even in a tenuous atmosphere a well-tuned nonlinear law can “thread the needle.”

Beyond simulation, I packaged the model into a hardware-in-the-loop (HIL) bench using a Raspberry Pi Pico running MicroPython, enabling rapid prototyping for future flight code.  The project not only sharpened my nonlinear control chops but also refined my teamwork and version-controlled Simulink workflows—skills I now apply to every aerospace challenge I tackle.
