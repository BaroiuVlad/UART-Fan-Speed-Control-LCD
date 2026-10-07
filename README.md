# STM32 UART Fan Speed Controller with LCD Display

A microcontroller-based system designed to control and monitor the speed of a cooling fan via UART serial communication, featuring real-time data display on an LCD screen.

---

## 🚀 Features
* **UART Serial Communication:** Receive commands/data from a PC or another microcontroller to adjust fan speed.
* **PWM Fan Control:** Precise speed regulation using Pulse Width Modulation (PWM).
* **LCD Interface:** Real-time visualization of current fan status, speed level, or RPM.
* **STM32 Ecosystem:** Built using standard HAL libraries for reliability and portability.

---

## 🛠️ Hardware Requirements
* **Microcontroller:** STM32 Development Board (e.g., STM32F103C8T6 / Nucleo)
* **Actuator/Load:** DC Fan (PWM compatible or driven via transistor/MOSFET)
* **Display:** LCD Screen (e.g., 16x2 I2C or Parallel LCD)
* **Communication:** USB-to-UART bridge (or built-in ST-Link VCP)
* **Power Supply:** Appropriate voltage source for the fan and MCU

---

## 📌 Pinout Configuration
| Periferic / Pin | Funcție STM32 | Descriere |
| :--- | :--- | :--- |
| **USARTx TX / RX** | PA9 / PA10 *(Exemplu)* | Conectare UART pentru comenzi externe |
| **TIMx_CHy (PWM)** | PA8 *(Exemplu)* | Semnal PWM pentru controlul turației ventilatorului |
| **I2C / GPIOs** | PB6, PB7 *(Exemplu)* | Linii de date pentru afișajul LCD |

---

## 💻 Software & Tools
* **IDE:** STM32CubeIDE / Keil uVision
* **Configurator:** STM32CubeMX
* **Language:** C

---

## ⚙️ How It Works
1. **Serial Input:** The system listens on the UART interface for incoming speed commands (e.g., characters or numeric values).
2. **Processing:** The STM32 parses the received data and updates the internal PWM duty cycle.
3. **Feedback:** The LCD displays the updated parameters in real time, confirming the action to the user.

---

## 📝 Usage / Getting Started
1. Clone the repository:
   ```bash
   git clone [https://github.com/USERNAME/stm32-uart-fan-control.git](https://github.com/USERNAME/stm32-uart-fan-control.git)
