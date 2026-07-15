# myoware-emg-detector
![Status](https://img.shields.io/badge/status-done-green)

Project summary: Real-time EMG signal acquisition and visualization using a MyoWare 2.0 muscle sensor and Arduino Uno.

Project description: A surface electromyography (EMG) sensing system using a MyoWare 2.0 muscle sensor and Arduino Uno to capture and visualize real-time muscle activation signals. Implemented analog signal acquisition, serial data logging, and signal visualization to explore applications in prosthetics, rehabilitation monitoring, and human-machine interfaces. Documented full engineering process from requirements through testing in a version-controlled repository.

Parts and Instrumentation: 
- MyoWare 2.0 Muscle Sensor
- Arduino Uno Rev3
- Disposable Surface EMG/ECG/EKG Electrode Pads
- Breadboard
- Jumper Wires
- USB-A to USB-B data cable

How it works: A muscle contraction triggers motor unit action potentials, producing a 
microvolt-scale differential signal at the skin surface. The MyoWare 2.0 
amplifies, band-pass filters, rectifies, and envelope-detects this signal 
into a clean 0-5V analog output. The Arduino's 10-bit ADC samples this at 
~100Hz via analogRead(A0), converting it to a 0-1023 digital value sent 
over serial for visualization.

Results: First muscle signal acquisition on forearm flexor muscle. Signal scales 
consistently with contraction intensity — resting baseline of ~27-30 ADC 
counts rising to ~400-500 ADC counts at peak contraction.

![EMG Signal](hard%20contraction%201.png)

Future Work: 
- Software digital filtering (moving average) to reduce signal noise
- Electrode placement optimization to maximize signal amplitude
- Data logging to CSV via Python/pyserial
- Custom visualization dashboard
