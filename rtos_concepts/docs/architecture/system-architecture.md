# System Architecture

## Overview
This document describes the **high-level system architecture** assumed for the embedded software examples and test scenarios presented in this repository. The architecture reflects a **typical automotive ECU software stack**, focusing on **RTOS behavior, task interaction, and system-level design**, without exposing proprietary implementations.

---

## Architectural Goals
- Provide a **clear separation of concerns** between application logic, OS services, and hardware abstraction.
- Demonstrate **real-time behavior** and deterministic task execution.
- Support **testability and validation** of RTOS and AUTOSAR OS features.
- Maintain **scalability and portability** across different embedded platforms.

---

## High-Level Architecture
The system follows a **layered architecture model**, commonly used in automotive embedded systems.

```text
+--------------------------------------------------+
|               Application Layer                  |
|  - Application Tasks                             |
|  - Test Scenarios                                |
+--------------------------------------------------+
|             RTOS / AUTOSAR OS Layer              |
|  - Task Scheduler                                |
|  - Synchronization Mechanisms                    |
|  - ISR Management                                |
+--------------------------------------------------+
|          Hardware Abstraction Layer (HAL)         |
|  - Driver Interfaces (Abstracted)                |
|  - Mocked Peripherals                            |
+--------------------------------------------------+
|                 Hardware Layer                   |
|  - Microcontroller (Abstracted)                  |
+--------------------------------------------------+
