# Op-amp-based-electronic-stethoscope
This project involves designing an electronic stethoscope that leverages **TL072**, **LM741**, and **LM386** op-amps to amplify and filter heart and lung sounds. The system enhances auscultation by improving signal clarity and reducing noise, enabling heartbeat impulses to be instantly displayed on a screen for easier anomaly detection. Additionally, it provides loud auditory replication of the detected signals for more effective diagnosis.

# Chest Piece & Mic
The stethoscope chest piece is connected to an electret mic with the help of a rubber tube. When the chest piece is placed against the patient’s chest, it provides physical amplification to the heartbeat signals, and the electret mic converts these sound signals into electrical signals.

# Pre-Amplification Stage (TL072 Dual Op-Amp)
**U1a: Low-Noise Microphone Preamp**  
The first op-amp, **U1a**, operates as a low-noise microphone preamp. The high output impedance of the drain of the FET inside the electret microphone results in an effective input resistance of about **20 kilo ohms**, yielding a gain of approximately **2.35**. A capacitor (**C2**, 10 micro farads) is used to pass very low frequency heartbeat sounds.

**U1b: Sallen-Key Butterworth Low-Pass Filter**  
The second op-amp, **U1b**, functions as a low-noise Sallen-Key Butterworth low-pass filter with a cutoff frequency of about **103 Hz**. It provides a gain of around **1.6** and produces a sharp Butterworth response.

# Amplification Stage (UA741)
The **UA741** amplifier provides a gain of **71** to produce a clear display of the heartbeat signals on the screen. It is also used to power an **LED** that blinks whenever the mic detects sound signals.

# Audio Amplification Stage (LM386)
The final stage uses an **LM386** audio amplifier. This power amplifier IC has built-in biasing and inputs that are referred to ground, and it provides a gain of **20**. It can drive any type of headphones or speakers, including low impedance (**8 ohm**) ones.






