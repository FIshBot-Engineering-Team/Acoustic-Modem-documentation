# README: Acoustic Modem Setup & Documentation
## Project: Multi-modal Modem (Acoustic/Optical) for KnifeBot

### 1. Overview
This documentation details the initial testing and configuration phase for the acoustic communication system of the KnifeBot. The primary goal of this stage was to establish a baseline for long-range underwater acoustic sensing and reliable data transmission using specialized hydrophones and acoustic boards.

### 2. Preliminary Development Requirements
To replicate the setup and conduct initial bench testing, the following environment was established:

**Hardware:**
* **Primary Controller:** Raspberry Pi 5 (preferred) or Raspberry Pi Zero 2W.
* **Alternative Controllers:** ESP32 or STM32 (for modular testing).
* **Peripherals:** Monitor, Keyboard, and Mouse for local Pi configuration.
* **Acoustic Hardware:** Acoustic Modem boards and Hydrophones for signal acquisition.

**Software & OS:**
* **Development OS:** Windows 11 (Host) and Ubuntu 22.04+ (Linux environment).
* **Communication Tool:** PuTTY (Terminal Emulator) installed on both Windows and Linux systems.

---

### 3. Step-by-Step Setup Process

#### Step 1: Interface Protocol & Connection
Establish physical and logical connections between the controller and the acoustic board.
* Connect the device via the serial interface (e.g., UART via USB).
* Ensure proper grounding and power supply to avoid signal interference.

#### Step 2: Serial Configuration via PuTTY
Configure the serial communication parameters to ensure data synchronization:
* **Connection Type:** Serial
* **Serial Line:** `/dev/ttyUSB0` (Common Linux designation)
* **Speed (Baud Rate):** `115200`
* **Action:** Save the session for future use and click **Open** to launch the terminal.

#### Step 3: Frequency Tuning & Signal Verification
Acoustic environments require precise tuning for clarity:
* **Center Frequency:** Identify the optimal frequency with the lowest noise floor.
* **Hydrophone Calibration:** Verify that the hydrophones are capturing signals without clipping or excessive distortion.
* **Bidirectional Check:** Confirm that the modems can both send and receive "Handshake" packets.

#### Step 4: Initial Results
Our testing confirmed successful communication between two units. The terminal results in PuTTY verified:
* Stable data packet transmission.
* Consistent sound quality through the acoustic front-end.
* Successful recognition of the `/dev/ttyUSB0` port across multiple test units.

---

### 4. Integration Context
This acoustic setup serves as the low-frequency, long-range fallback for the KnifeBot. The next phase involves integrating the **Optical Modem** component to allow the system to switch between high-speed (optical) and high-reliability (acoustic) modes dynamically.

---
*Generated for the Acoustic Engineering Team*
*Version: 1.2*
