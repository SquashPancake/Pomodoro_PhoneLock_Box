# 📦 Phone Focus Pomodoro Lock Box (Arduino)


## 🎯 Overview
A physical Pomodoro-style focus box that locks your phone away during study sessions.  
Once your phone is placed inside, the box automatically locks using a micro servo motor.  
After the focus timer ends, a code is displayed, and only the correct button input will unlock the lid.

This project enforces focus **physically**, not digitally.

---

## 💡 Core Idea
- 📵 Remove phone distractions by locking the device away
- ⏱️ Use time as the unlock condition
- 🧠 Simple logic, physical feedback, no apps required

---

## ⚙️ How It Works
1. 📱 Phone is placed inside the box  
2. 📡 Ultrasonic sensor detects the phone  
3. ⏳ Countdown timer starts  
4. 🔒 Servo rotates and locks the lid  
5. ⌛ Pomodoro timer runs  
6. 🔢 Unlock code appears on the display  
7. 🔘 Correct button sequence is pressed  
8. 🔓 Servo unlocks the lid  

---

## ✨ Features
- 📡 Automatic phone detection
- 🔒 Servo-controlled physical lock
- ⏲️ Pomodoro-style countdown timer
- 🔢 Code-based unlock system
- 🖥️ Display feedback
- 🔘 Button-based input

---

## 🧰 Components Used
- Arduino (any compatible board)
- Ultrasonic distance sensor
- Micro servo motor
- Display module
- Push buttons
- Power supply
- Wooden box
- Wooden ice cream sticks

---

## 🏗️ Step-by-Step Build Guide

### 🔧 Part 1: Servo Locking Mechanism (Physical Build)

This is the **core mechanical system** of the project.

#### What You Are Building
A **physical latch** that prevents the box lid from opening once the servo rotates into position.

#### Steps
1. 🪵 Use wooden ice cream sticks to build an **extra latch** attached to the box lid  
2. 📦 Secure the servo motor to the inside wall of the box  
3. 🔄 Position the servo arm so that:
   - When the lid closes, the servo arm can rotate **above the ice cream stick latch**
   - This blocks the lid from opening
4. 🔒 When the servo rotates into the locking position, the lid is physically trapped  
5. 🔓 When the servo rotates back, the latch is released and the lid opens

💡 **Tip:**  
Test the servo angles manually before final mounting to ensure:
- One angle = locked
- One angle = unlocked

---

### 🔌 Part 2: Wiring (Electronics)

For wiring:
- 📐 Follow the provided schematic
- 🔗 Connect:
  - Ultrasonic sensor to Arduino input pins
  - Servo motor to a PWM pin
  - Buttons to digital input pins
  - Display to the appropriate interface (I2C / SPI / parallel)

⚠️ Ensure common ground between all components.

---

### 🧠 Part 3: Logic & Code Behavior

The Arduino controls the system using **state-based logic**.

#### Logic Flow
1. 🟢 Idle state (box unlocked)
2. 📡 Phone detected → start timer
3. 🔒 Servo locks lid
4. ⏳ Countdown state
5. ⌛ Timer finishes
6. 🔢 Unlock code displayed
7. 🔘 Button input checked
8. 🔓 Correct code → unlock servo
9. 🔄 Return to idle state

---

## 🧩 System Architecture

### Inputs
- 📡 Ultrasonic sensor  
- 🔘 Push buttons  

### Processing
- 🧠 Arduino microcontroller  
- ⏱️ Timer logic  
- 🔁 State management  

### Outputs
- 🖥️ Display (status, countdown, unlock code)  
- 🔒 Servo motor (lock / unlock)

---

## 🗂️ Code Structure
Main code responsibilities:
- Ultrasonic distance detection
- Timer handling
- Servo control
- Button input reading
- Display updates
- State-based system flow

Arduino code is located in: code folder


--------------------------------------------

## ⚠️ Limitations
- Ultrasonic sensor may false-trigger
- Unlock code is not encrypted
- No session history storage
- Fixed physical design

---

## 🚀 Possible Improvements
- 🔢 Keypad instead of buttons
- 📊 Session tracking and statistics
- 🔋 Battery-powered version
- 📱 App or Bluetooth integration
- 🔐 Stronger locking mechanism

---

## 🧪 Purpose of This Project
This project was built as:
- A hands-on Arduino systems integration exercise
- A physical approach to focus enforcement
- Practice combining sensors, actuators, and UI components

---

## 📜 License
Open for learning, experimentation, and iteration.
