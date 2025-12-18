

# TwinCAT FIFO Implementation (PLC)

## Overview

This repository contains a **TwinCAT 3 PLC project** implementing a **FIFO (First-In, First-Out) register system** using **Function Blocks, Interfaces, and Object-Oriented concepts**.

The project demonstrates:

* FIFO data handling
* Use of TwinCAT **Interfaces (IF_*)**
* Separation of logic into reusable Function Blocks
* Push / Pick (Put / Get) mechanisms
* Test and example programs

This is intended as a **learning and reference project** for TwinCAT PLC developers.

---

## Project Structure

### PLC Objects (POUs)

#### FIFO Implementations

* **`FB_FIFO`**
  Basic FIFO implementation using registers.

* **`FB_FIFO_1`**
  Variant of FIFO logic (alternative implementation or evolution).

* **`FB_FIFO_OOP`**
  Object-oriented FIFO implementation using interfaces for abstraction.

---

#### Interfaces

* **`IF_Register`**
  Base interface defining register behavior.

* **`IF_EmptyRegister`**
  Interface for checking and getting empty registers.

* **`IF_FillRegister`**
  Interface for putting data into registers.

These interfaces allow loose coupling between FIFO logic and register handling.

---

#### Push / Pick Logic

* **`FB_Pusher_Itf`**
  Handles pushing data into the FIFO via interfaces.

* **`FB_Picker_Itf`**
  Handles picking (getting) data from the FIFO.

* **`SR_Push_and_pick_ITF (PRG)`**
  Example program showing push and pick behavior using interfaces.

---

#### Programs

* **`MAIN (PRG)`**
  Main PLC program entry point.

* **`SR_FIFO (PRG)`**
  FIFO test program.

* **`RandomGenerator`**
  Generates test data for FIFO operations.

---

## Key Features

* FIFO register handling
* Clear separation of concerns
* Interface-based design
* Reusable and extendable function blocks
* Suitable for simulation and real PLC logic

---

## Requirements

* **TwinCAT 3**
* **Visual Studio (TwinCAT XAE)**
  (Version depends on your TwinCAT installation)

---

## How to Open the Project

1. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   ```
2. Open the `.sln` file in **Visual Studio (TwinCAT XAE)**.
3. Activate the TwinCAT configuration.
4. Build and run in **Simulation Mode** or on a real PLC.

---

## Git Notes

This repository excludes generated and temporary files using `.gitignore`, including:

* `bin/`, `obj/`
* `.vs/`
* `_TcTemp/`
* Compiled TwinCAT artifacts

Only **source code and configuration files** are tracked.

---

## Learning Goals

This project is useful if you want to learn:

* FIFO implementation in PLC
* TwinCAT interfaces (`IF_*`)
* Object-oriented PLC programming
* Clean project organization in TwinCAT

---

## License

This project is provided for educational purposes.
Add a license if you plan to share or reuse commercially.

---

If you want, next we can:

* Tighten this README to **professional open-source style**
* Add **diagrams explaining FIFO flow**
* Create a **GitHub-friendly folder layout explanation**
* Or add comments directly inside your FBs explaining the design logic

This is already a solid learning project—now it looks like one too.
