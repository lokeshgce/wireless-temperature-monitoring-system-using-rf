# wireless-temperature-monitoring-system-using-rf
Wireless Temperature Monitoring: An LM35 signal is converted to frequency via LM331, sent over RF, then reconstructed by a second LM331. A dual-PCB KiCad design for precise, remote analog sensing.


Wireless data transmitting System Using RF (Without Microcontroller):
    1. This project demonstrates a wireless transmission of  data without using a microcontroller. 
    2. Instead of digital processing, the system uses analog signal conversion techniques 
    3. RF communication to transmit data from a transmitter unit to a receiver unit.
    4. The main goal of the project is to show that simple data, such as temperature, can be transmitted wirelessly using analog electronics without the complexity of microcontroller-based systems.

System Architecture

The system consists of two main sections:
     1. Transmitter Section
     2. Receiver Section

Data is sent the transmitter side, converted into a frequency signal, transmitted through RF communication, and then converted back into voltage at the receiver side to display the data.

Transmitter:
LM358 – Voltage buffer
LM331 – Voltage to frequency conversion
433 MHz ASK RF Transmitter Module – Wireless transmission
Antenna – RF signal radiation

Receiver: 
433 MHz ASK RF Receiver Module – Receives RF signal
74HC14 – Signal conditioning
LM331 – Frequency to voltage conversion
Voltmeter – Output display

Lm358 voltage buffer:
<img width="651" height="390" alt="image" src="https://github.com/user-attachments/assets/0e05abd8-f3e5-48fd-9aae-eee2bfdfec04" />

A voltage buffer amplifier is used to transform a voltage signal with high output impedance from a first circuit into an identical voltage with low impedance for a second circuit.


Lm331 IC    :     voltage – frequency & frequency to voltage 

<img width="1067" height="385" alt="image" src="https://github.com/user-attachments/assets/0efb68c0-225a-456e-9f77-87265144b5b2" />


The LM331 is a precision monolithic IC that converts an analog voltage (0–10V) into a proportional frequency (0–10kHz) or vice versa, operating on a single 5V to 40V supply.

It produce output voltage proportional to input frequency and vice versa.


433 MHz ASK RF Transmitter Module:

Working:

It uses Amplitude Shift Keying (ASK)
A transmitter converts digital data into radio waves, while a receiver converts them back
Adding a 173 mm long single-core wire as an antenna improve its performance


<img width="667" height="374" alt="image" src="https://github.com/user-attachments/assets/c25c5a4b-59b2-415f-b5f0-8e5515d920a8" />

IC 74hc14  Schimitt Trigger : 

<img width="925" height="517" alt="image" src="https://github.com/user-attachments/assets/cf1fdce3-f2c6-43b8-97ef-7c7e6f377f6b" />

It transforms noisy or slow-changing input signals into clean, sharp digital pulses.

Transmitting the temperature sensor value as data using this method:

<img width="204" height="262" alt="image" src="https://github.com/user-attachments/assets/414f47e7-97fc-405f-a449-453bf24b2327" />

Working of transmitter: 
     1. The LM35 senses temperature and produces an analog voltage proportional to temperature.
     2. The LM358 acts as a buffer amplifier to stabilize the sensor signal.
     3. The LM331 converts the analog voltage into a corresponding frequency signal.
     4. This frequency signal is fed into the RF transmitter module.
     5. The transmitter sends the signal wirelessly using a 433 MHz radio frequency signal.

Working of Receiver:

      The RF receiver module captures the transmitted signal.
      The received signal may contain noise, so the 74HC14 Schmitt trigger cleans and reshapes the signal into stable pulses.
      The LM331 converts the received frequency signal back into an analog voltage.
      The output voltage is displayed on a voltmeter, which corresponds to the measured temperature.

Working Principle:

      The system works based on signal conversion techniques:

      Temperature → Voltage → Frequency → RF Transmission → Frequency →     	Voltage → Display
<img width="1547" height="844" alt="image" src="https://github.com/user-attachments/assets/052603ab-de8f-4bb2-8e33-84008a54b235" />






