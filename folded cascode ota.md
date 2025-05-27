## Folded Cascode Operational Transconductance Amplifier (OTA)

The Folded Cascode OTA modifies the telescopic structure by "folding" the current from the input pair into a different branch, improving voltage headroom. The design includes:
Differential input pair: Usually NMOS (for higher transconductance) that drives PMOS cascode devices.
Folding mechanism: The current from the input NMOS devices is folded into PMOS devices, which allows the circuit to avoid stacking all transistors vertically.
Cascode transistors: Maintain high output impedance and gain.
Output stage: Typically a current mirror or load that provides a single-ended output.
This design enhances output swing, common-mode input range, and power efficiency, making it ideal for low-voltage, low-power applications, while still offering moderate to high gain and bandwidth.
## circuit diagram
![image](https://github.com/user-attachments/assets/94b028e2-1c09-46c2-9fa9-b4c1e82b0ced)
•	Architecture: CMOS Folded Cascode Op-Amp
•	Technology: 180 nm CMOS
•	Supply Voltage (VDD): 1.8 V
•	Input Signal: 1mV (sine wave)
•	DC Gain: ≥ 60 dB
•	Unity Gain Bandwidth (UGBW): ~10 MHz
•	Phase Margin: ~60°

## Design Description
The proposed design is a two-stage CMOS operational amplifier based on a folded cascode architecture. The first stage consists of a differential input pair with active current mirrors to achieve high gain and common-mode rejection, while the second stage is a common-source amplifier that boosts output swing and drives the load. Frequency compensation is applied using a Miller capacitor to ensure stability and achieve the desired phase margin. Transistor dimensions (W/L ratios) and bias currents are carefully optimized to meet the specifications of 120 dB gain, 50 MHz bandwidth, 0.825 V output swing, and 8 mW power consumption under a 3.3 V supply. The entire design is implemented and analyzed using LTspice

 Open-Loop Gain (Aₒ):
Target = 120 dB → Aₒ = 10⁶ = gm × ro (stage 1) × gain (stage 2)
- Unity Gain Bandwidth (UGBW):
UGBW = gm / Cc → For gm = 1 mS, Cc = 20 pF → UGBW = 50 MHz
- Slew Rate (SR):
SR = I / Cc → For Cc = 20 pF, SR = 1 V/µs → I = 20 µA
- Power Consumption:
P = VDD × I = 3.3 V × 2.4 mA = 7.92 mW ≈ 8 mW
- Output Swing:
Max swing = VDD / 4 = 0.825 V
## result
![image](https://github.com/user-attachments/assets/8ab3c4e0-e0c4-479e-b0d4-d323236711a8)
![image](https://github.com/user-attachments/assets/f9056a5d-3eea-4691-8829-546afae11afe)
![WhatsApp Image 2025-05-27 at 11 14 28_fdb17f16](https://github.com/user-attachments/assets/5c60cb36-5e79-4977-84c1-296bed70f9b0)


##  conclusion
	Based on the final AC analysis in LTspice, the designed operational amplifier achieves a gain of approximately 60 dB, a unity-gain bandwidth close to 10 MHz, and with proper compensation (like the Miller capacitor), a phase margin around 60° is attainable. This indicates that the op-amp is stable, has high gain, and meets the desired frequency response specifications for general-purpose analog applications. Adjusting bias voltages (e.g., Vb3) and transistor W/L ratios was critical in achieving these parameters. 
