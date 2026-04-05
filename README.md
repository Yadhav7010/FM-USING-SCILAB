# FM

EXP NO: 4    GENERATION AND DETECTION OF FM

---

## AIM:
To write a program for Frequency Modulation and Demodulation using SCILAB and to observe and measure the frequency deviation and the modulation index of FM.

---

## EQUIPMENTS REQUIRED
- Computer with i3 Processor  
- SCI LAB  

---

## THEORY:
Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal.

### Frequency Deviation Δf and Modulation Index mf:
The frequency deviation Δf represents the maximum shift between the modulated signal frequency, over and under the frequency of the carrier.

We define modulation index mf as the ratio between Δf and the modulating frequency:  
m = Δf / fm  

### Frequency Modulation Generation:
The circuits used to generate frequency modulation must vary the frequency of a high frequency signal (carrier) as a function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.

---

## ALGORITHM

1. Define Parameters:
   - Fs: Sampling frequency  
   - T: Duration of the signal  
   - Fc: Carrier frequency  
   - Fm: Frequency of the modulating signal  
   - Beta: Modulation index  

2. Generate Signals:
   - Modulating signal  
   - Carrier signal  
   - FM modulated signal  

3. FM Modulation:
   - Modulate carrier with message signal  

4. FM Demodulation:
   - Differentiation  
   - Envelope Detection  
   - Low-pass Filtering  

5. Visualization:
   - Plot all signals  

---

## PROCEDURE
- Refer Algorithms and write code for the experiment  
- Open SCILAB in System  
- Type your code in New Editor  
- Save the file  
- Execute the code  
- If any error, correct it and execute again  
- Verify the generated waveform using Tabulation and Model Waveform  

---

## MODEL GRAPH
<img width="512" height="365" src="https://github.com/user-attachments/assets/acd787bd-5281-4f1b-802f-1aa39fac9189" />

---

## PROGRAM
```scilab
clc;
clear;
close;

// Modulation index
B  = 5.6;

// Parameters
Ac = 36.2;        // Carrier amplitude
Am = 18.1;        // Message amplitude
Fc = 6460;        // Carrier frequency (Hz)
Fm = 646;         // Message frequency (Hz)
Fs = 56700;       // Sampling frequency (Hz)

// Time vector
T  = 0:1/Fs:2/Fm;

// Message signal
em = Am * cos(2 * %pi * Fm * T);
subplot(3,1,1);
plot(T, em);
xtitle("Message Signal");
xgrid();

// Carrier signal
ec = Ac * cos(2 * %pi * Fc * T);
subplot(3,1,2);
plot(T, ec);
xtitle("Carrier Signal");
xgrid();

// FM signal
efm = Ac * cos(2 * %pi * Fc * T + B * sin(2 * %pi * Fm * T));
subplot(3,1,3);
plot(T, efm);
xtitle("Frequency Modulated Signal");
xgrid();
```

---

## OUTPUT WAVEFORM
<img width="1917" height="1194" src="https://github.com/user-attachments/assets/846a9015-831c-4cba-94bb-6fd9b7d44709" />

---

## TABULATION
<img width="1158" height="735" src="https://github.com/user-attachments/assets/f005daa6-2070-41b1-bfb4-51e07f04c660" />

---

## RESULT:
Thus, the frequency modulation and demodulation is successfully done and the output is experimentally verified.
<img width="1079" height="653" alt="image" src="https://github.com/user-attachments/assets/90470bb2-599f-4998-8f6d-f5cb14850073" />

