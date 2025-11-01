# Face Detection and Tracking - Arduino + Micro:Bit App  
### 🔗 Try the App  
👉 [**Open Live App**](https://roboticschools.github.io/Face-Detection-and-Tracking-App/)  

---

## 📖 Overview  
This project combines **AI-based face detection** with **Arduino** and **BBC Micro:Bit** to enable face and gesture-controlled robotics — all from your browser!  
The app uses **MediaPipe FaceMesh** to detect your **eyes, mouth, and head movement**, and sends real-time data to **either Arduino (via Web Serial)** or **Micro:Bit (via Web Bluetooth)**.  
No external software or installations needed — just open the link, connect your board, and start controlling your projects using facial expressions and head movements.  

---

## ⚙️ Features  
✅ Real-time face and head tracking using **MediaPipe FaceMesh**  
✅ Works with both **Arduino** and **BBC Micro:Bit**  
✅ Automatically hides the other board’s connect button once connected  
✅ Sends live tracking data through **Serial (Arduino)** or **Bluetooth (Micro:Bit)**  
✅ Smooth and stable detection using filtering and hysteresis  
✅ Simple payload format for easy integration with your own projects  

---

## 📡 Data Format  
The app sends data in this format:  

`L,R,M,F,H,V`

| Field | Description | Example |
|--------|--------------|----------|
| `L` | Left eye open (1) / closed (0) | `L1` |
| `R` | Right eye open (1) / closed (0) | `R1` |
| `M` | Mouth open (1) / closed (0) | `M0` |
| `F` | Face visible (1) / not visible (0) | `F1` |
| `H` | Horizontal head direction: -1 (Left), 0 (Center), 1 (Right) | `H0` |
| `V` | Vertical head direction: -1 (Up), 0 (Center), 1 (Down) | `V0` |

**Example Message:**  
### L1,R1,M0,F1,H0,V0  

➡️ Left eye open, Right eye open, Mouth closed, Face detected, Head centered horizontally and vertically.  
