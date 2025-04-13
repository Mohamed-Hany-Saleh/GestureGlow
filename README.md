# ✨ GestureGlow

## 📌 Overview
**GestureGlow** is a computer vision-based project that detects hand gestures (number of fingers raised) to control LEDs connected to an Arduino board. It combines real-time hand tracking using OpenCV with hardware control via pyFirmata.

## 🎯 Features
- Detects hand gestures from 0 to 5 fingers.
- Displays the detected number on the video feed.
- Lights up LEDs on Arduino according to the number of fingers raised.
- Real-time processing with high detection accuracy.

## 🖥️ Technologies Used
- Python 3
- OpenCV
- [cvzone](https://github.com/cvzone/cvzone)
- pyFirmata
- Arduino Uno

## 🛠️ Hardware Required
- Arduino Uno
- 5 LEDs
- Resistors (220Ω)
- Breadboard
- Jumper wires
- USB Cable

## ⚙️ Arduino Pin Configuration
| Finger Count | Active LED Pins |
|--------------|-----------------|
| 0            | None            |
| 1            | D7              |
| 2            | D7, D9          |
| 3            | D7, D9, D10     |
| 4            | D7, D9, D10, D11|
| 5            | D7, D9, D10, D11, D12 |

## 📂 Project Structure
GestureGlow/ ├── main.py # Handles video capture and gesture detection ├── controller.py # Arduino LED control logic └── README.md # Project documentation

markdown
Copy
Edit

## ▶️ How to Run
1. Connect your Arduino board to your PC via USB.
2. Open the Arduino IDE, go to **File > Examples > Firmata > StandardFirmata**, and upload it to your board.
3. Install the required Python libraries:
   ```bash
   pip install opencv-python cvzone pyfirmata
Make sure the COM port in controller.py matches your Arduino port (e.g., 'COM3').

Run the main script:

bash
Copy
Edit
python main.py
To exit the program, press the k key.

📷 How It Works
The webcam captures a video feed.

The cvzone module detects the hand and determines which fingers are up.

According to the finger count, the corresponding LEDs are turned ON/OFF via Arduino.

📽️ Demo

https://github.com/user-attachments/assets/eaf4b7a4-60c0-478a-9583-be71aa0af5a3



🔮 Future Improvements
Add GUI to display real-time feedback and control.

Extend to recognize custom hand gestures.

Add support for wireless control (e.g., Bluetooth).

🧠 Author
Mohamed Hany Saleh
###[GitHub Profile](https://github.com/Mohamed-Hany-Saleh)  
###[LinkedIn](https://www.linkedin.com/in/mohammad-hany12/)
