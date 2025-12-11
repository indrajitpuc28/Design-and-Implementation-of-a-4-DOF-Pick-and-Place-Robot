🤖 4-DOF Pick and Place Robotic Arm  
**Low-Cost | Arduino-Based | Bluetooth Controlled**

A functional, low-budget **4-DOF articulated robotic arm** designed for simple industrial operations such as gripping, lifting, placing, and releasing objects. Built using easily available components, this system aims to make basic automation accessible for small-scale industries and educational purposes.

---

## 📌 Introduction  
Modern robotics stems from the concept of *“robot”*—derived from the Czech word **“robota”** (forced labor). Today, robots automate repetitive, hazardous, and high-precision tasks in industries. However, **SMEs often avoid automation due to high cost and complex maintenance**.  

This project provides a **low-cost robotic solution** using off-the-shelf parts, making automation simple and affordable.

---

## 🔧 Features  
- **4 Degrees of Freedom (DOF)**  
- **Bluetooth tele-operation** via HC-05  
- **Arduino Uno as main controller**  
- **Servo motor actuation** for smooth motion  
- **Adjustable motion limits** via code edits  
- **Lightweight structure** suitable for small workloads  
- **Ideal for education, research & prototypes**

---

## 🏗️ System Overview  

### **Hardware Components**
- Arduino Uno  
- HC-05 Bluetooth Module  
- L298N / L28n Motor Driver  
- High-Torque Servo Motors (Base, Shoulder, Elbow)  
- Micro Servo Motors (Wrist, Gripper)  
- Aluminum / Acrylic frame  

### **Mechanical Design**
- Shoulder rotation  
- Elbow movement  
- Wrist rotation  
- Parallel-jaw gripper  

---

## 📱 Control System  
A custom mobile app (MIT App Inventor) sends commands wirelessly:  
- Command → HC-05 → Arduino → Motor Driver → Servos  
- Each joint receives independent control signals  
- Gripper uses toggle (open/close) logic  

---

## 🧠 Software  
- Arduino IDE for microcontroller programming  
- PWM-based servo control  
- Customizable angle limits for each joint  
- Serial communication with HC-05  

---

## 📊 Performance  
- Designed to lift small lightweight objects  
- Smooth operation using servo-based actuation  
- Customizable movement ranges  
- Suitable for student projects and basic automation tasks  

---

## 📎 Files Included  
- Full Report (PDF)  
- Circuit Diagram  
- CAD Design Details  
- Arduino Code  
- App Interface Logic  

---

## 📘 Reference  
CircuitDigest – *Bluetooth Controlled Pick and Place Robotic Arm*

---

"""

output_path = "/mnt/data/README.md"
pypandoc.convert_text(readme_text, 'md', format='md', outputfile=output_path, extra_args=['--standalone'])

output_path
import pypandoc

readme_text = """# 🤖 4-DOF Pick and Place Robotic Arm  
**Low-Cost | Arduino-Based | Bluetooth Controlled**

![My Robotic Arm](images/robotic_arm.jpg)

A functional, low-budget **4-DOF articulated robotic arm** designed for simple industrial operations. This README now includes an **image section** and a **JSON configuration example**.

---

## 📌 Introduction  
Modern robotics stems from the concept of *“robot”*—derived from the Czech word **“robota”** (forced labor). Today, robots automate repetitive, hazardous, and high-precision tasks.  
This project provides a **low-cost robotic solution** ideal for SMEs, students, and researchers.

---

{
  "servo_limits": {
    "base": { "min": 0, "max": 180 },
    "shoulder": { "min": 20, "max": 160 },
    "elbow": { "min": 10, "max": 170 },
    "wrist": { "min": 0, "max": 180 },
    "gripper": { "open": 60, "close": 150 }
  },
  "bluetooth": {
    "module": "HC-05",
    "baud_rate": 9600
  },
  "app_commands": {
    "up": "U",
    "down": "D",
    "left": "L",
    "right": "R",
    "grip_toggle": "G"
  }
}
{
  "servo_limits": {
    "base": { "min": 0, "max": 180 },
    "shoulder": { "min": 20, "max": 160 },
    "elbow": { "min": 10, "max": 170 },
    "wrist": { "min": 0, "max": 180 },
    "gripper": { "open": 60, "close": 150 }
  },
  "bluetooth": {
    "module": "HC-05",
    "baud_rate": 9600
  },
  "app_commands": {
    "up": "U",
    "down": "D",
    "left": "L",
    "right": "R",
    "grip_toggle": "G"
  }
}
