# 📷 FPGA-Based Real-Time Camera System  
### 🚀 Real-Time Video Capture & VGA Display using OV7670 on Basys 3 FPGA  

![FPGA](https://img.shields.io/badge/FPGA-Artix--7-blue)
![Language](https://img.shields.io/badge/Language-Verilog-orange)
![Tool](https://img.shields.io/badge/Tool-Xilinx%20Vivado-purple)
![Protocol](https://img.shields.io/badge/Protocol-SCCB%20%7C%20I2C-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Experience](https://img.shields.io/badge/Internship-NIT%20Rourkela-red)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📌 Overview  
This project implements a **high-performance real-time video acquisition and display pipeline** on FPGA using the **Basys 3 (Artix-7)** platform and **OV7670 camera module**. The system captures live image data, processes it on hardware, and outputs it to a **VGA display with minimal latency**.

Developed during my **Summer Internship at NIT Rourkela (May – July 2025)** under **Prof. Dr. Ayas Kanta Swain**, this project demonstrates strong fundamentals in **FPGA design, digital systems, and real-time image processing**.

---

## 🎯 Key Highlights  

- 📸 Real-time video capture using OV7670 camera  
- 🎥 VGA output (640×480 @ 60Hz)  
- ⚡ Fully hardware-accelerated pipeline (low latency)  
- 🔄 Asynchronous FIFO for clock domain crossing  
- 🎛️ Brightness & contrast control  
- 🌗 Grayscale image processing  
- 🔧 SCCB (I2C-like) camera configuration  
- 🎨 RGB565 → RGB444 conversion  
- 🧠 BRAM-based frame buffering  

---

## 🧠 System Architecture  

```
OV7670 Camera → Capture Module → FIFO (BRAM) → VGA Controller → Display
                        ↓
                SCCB Configuration
```

---

## 🛠️ Hardware Used  

- Basys 3 FPGA Board (Xilinx Artix-7)  
- OV7670 Camera Module (No FIFO)  
- VGA Monitor  
- Connecting Wires  

---

## 💻 Tech Stack  

- **HDL:** Verilog  
- **Toolchain:** Xilinx Vivado  
- **Protocols:** SCCB (I2C-like), GPIO  
- **Clock Domains:**  
  - Camera: 24 MHz  
  - VGA: 25 MHz  

---

## 📂 Project Structure  

```
FPGA-Camera-System/
│── src/
│   ├── top_module.v
│   ├── camera_capture.v
│   ├── sccb_config.v
│   ├── vga_controller.v
│   ├── fifo_buffer.v
│   ├── rgb_converter.v
│   ├── image_processing.v
│   └── clock_generator.v
│
│── constraints/
│   └── basys3.xdc
│
│── docs/
│   └── system_architecture.png
│
│── README.md
```

---

## ⚙️ Working Flow  

### 🔹 Camera Initialization  
- OV7670 configured via SCCB protocol  
- Set to RGB565 format  

### 🔹 Image Capture  
- Pixel data captured using PCLK  
- VSYNC & HREF ensure frame integrity  

### 🔹 Clock Domain Crossing  
- FIFO handles 24 MHz → 25 MHz mismatch  
- Prevents tearing and data loss  

### 🔹 Image Processing  
- RGB conversion (565 → 444)  
- Optional grayscale & brightness tuning  

### 🔹 VGA Output  
- Generates HSYNC & VSYNC  
- Displays stable real-time frames  

---

## 📊 Performance  

| Feature | Value |
|--------|------|
| Resolution | 640 × 480 |
| Refresh Rate | 60 Hz |
| Pixel Clock | 25 MHz |
| Latency | Very Low (Hardware Pipeline) |

---

## 🔍 Core Modules  

- **Camera Capture:** Handles pixel acquisition  
- **SCCB Controller:** Configures camera registers  
- **FIFO (BRAM):** Ensures smooth data transfer  
- **VGA Controller:** Generates display signals  
- **Image Processing:** Enhances video output  

---

## 🚧 Challenges & Solutions  

| Challenge | Solution |
|----------|---------|
| Clock mismatch | Asynchronous FIFO |
| SCCB debugging | FSM-based controller |
| Frame tearing | Proper buffering |
| Signal instability | Timing optimization |

---

## 📸 Results  

✔️ Real-time VGA video output  
✔️ Stable frame display  
✔️ Hardware-level image processing achieved  

---

## 📚 Learning Outcomes  

- FPGA-based system design  
- Real-time video processing  
- Verilog HDL development  
- Camera interfacing  
- Clock domain crossing  
- Hardware debugging  

---

## 🔮 Future Scope  

- Edge detection on FPGA  
- HDMI output integration  
- Higher resolution support  
- AI-based vision system (FPGA + SoC)  

---

## 👨‍💻 Author  

**Ratnakar Sahoo**  
B.Tech, Electronics & Telecommunication Engineering  
Veer Surendra Sai University of Technology (VSSUT), Burla  

📍 Internship: NIT Rourkela (May – July 2025)  
📍 Domain: FPGA | Embedded Systems | Computer Vision  

---

## ⭐ Portfolio Description (For Resume / LinkedIn)  

**FPGA-Based Real-Time Camera System | NIT Rourkela Internship (May–July 2025)**  
Designed and implemented a real-time video processing pipeline on Basys 3 FPGA using the OV7670 camera. Developed Verilog modules for image capture, SCCB configuration, asynchronous FIFO buffering, and VGA display. Achieved low-latency hardware-based image processing with brightness control and grayscale conversion, demonstrating strong expertise in FPGA design, digital systems, and real-time embedded vision applications.

---

## 📜 License  

MIT License  

---

## 🙏 Acknowledgement  

Special thanks to **Prof. Dr. Ayas Kanta Swain (NIT Rourkela)** for mentorship and guidance.

---

⭐ *If you found this project interesting, consider giving it a star!*  
