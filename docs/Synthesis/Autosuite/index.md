---
title: Autosuite
layout: home
parent: Synthesis
---


# AutoSuite – Basic Guide

A concise introduction to the core areas of **AutoSuite**: the **Editor** (Configuration, Zone, Task), **Simulation**, **Executor**, and **Driver Manager**. Image placeholders are included below—replace them with your actual screenshots.

---

## 1. Editor

### Configuration Section
- Defines the **overall experiment setup** (drivers, parameters, global settings).
- Serves as the **blueprint** of the experiment prior to execution.
- Central place to ensure hardware and software options are correctly selected.
<!-- Image: AutoSuite Configuration section -->
![AutoSuite Configuration](assets/img/INSERT_autosuite_configuration.png)

### Zone Section
- Organizes **physical/logical areas** where tasks will run (e.g., instruments, reactors, platform modules).
- Each **Zone** corresponds to a specific experimental unit and owns its timeline.
- Helps visualize task allocation across equipment.
<!-- Image: AutoSuite Zone section -->
![AutoSuite Zones](assets/img/INSERT_autosuite_zones.png)

### Task Section
- Defines the **sequence of operations** (dosing, stirring, heating, etc.).
- Each **Task** is an actionable step executed by a specific driver.
- Tasks are arranged in the **timeline** within a Zone.
<!-- Image: AutoSuite Task section -->
![AutoSuite Tasks](assets/img/INSERT_autosuite_tasks.png)

---

## 2. Simulation
- Runs a **virtual dry-run** of the configured workflow.
- Detects **errors, missing links, or driver conflicts** before execution.
- Ensures the workflow is **logically consistent** and resources are available.
<!-- Image: AutoSuite Simulation window -->
![AutoSuite Simulation](assets/img/INSERT_autosuite_simulation.png)

---

## 3. Executor
- Handles **real-time execution** of the experiment.
- Reads configuration and tasks, then **dispatches commands** to hardware.
- Shows **live progress**, statuses, and feedback from instruments.
<!-- Image: AutoSuite Executor interface -->
![AutoSuite Executor](assets/img/INSERT_autosuite_executor.png)

---

## 4. Driver Manager
- Utility for **configuring and controlling device drivers**.
- Allows manual **connect/disconnect/reset** of drivers and quick diagnostics.
- Useful for **troubleshooting** or controlling equipment **outside** a running experiment.
<!-- Image: AutoSuite Driver Manager panel -->
![AutoSuite Driver Manager](assets/img/INSERT_autosuite_driver_manager.png)

---