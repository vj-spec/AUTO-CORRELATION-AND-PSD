# AUTO-CORRELATION-AND-PSD

## **Aim**
Write a program for **Autocorrelation** and **Power Spectral Density (PSD)** of signals in **Scilab** and verify the **Wiener–Khinchin relation**.

---

## **Equipments Needed**
- Computer with **Intel i3 processor** (or higher)  
- **Scilab** software

---

## **Theory**
The **Wiener–Khinchin theorem** states that:  
> The Power Spectral Density (PSD) of a wide-sense stationary random process is the **Fourier Transform** of its **autocorrelation function**.
<img width="466" height="74" alt="image" src="https://github.com/user-attachments/assets/f7c7673b-e086-4231-b8b4-4a677a3f7d0c" />

This relationship bridges the **time-domain correlation** and **frequency-domain power** representations of a signal.

---

## **Algorithm**
1. **Load or Define the Signal:** Input your time-domain signal.  
2. **Compute Autocorrelation:** Calculate the autocorrelation function of the signal.  
3. **Compute Power Spectral Density (PSD):**  
   Estimate the PSD using either:  
   - Fourier Transform of the autocorrelation function, or  
   - Methods like Welch’s periodogram.  
4. **Plot Results:** Visualize both the autocorrelation function and PSD.

---

## **Procedure**
1. Refer to the algorithm and write the code for the experiment.  
2. Open **Scilab** on your system.  
3. Type your code in a **new editor**.  
4. **Save** the file.  
5. **Execute** the code.  
6. If any errors occur, **debug and re-run** the program.  
7. Verify the generated waveform using **tabulation** and **model waveform** comparison.

---

## **Program (Scilab Code)**

```scilab
clc
clear all; 
t=0:0.01:2*%pi;
x=7*sin(2*t);
subplot(3,2,1);
plot(x);
au=xcorr(x,x);
subplot(3,2,2);
plot(au);
v=fft(au);
subplot(3,2,3);
plot(abs(v));
fw=fft(x);
subplot(3,2,4);
plot(fw);
fw2=(abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
```
---
## **Output:**
<img width="758" height="720" alt="image" src="https://github.com/user-attachments/assets/bb5c138f-55fa-4786-8ea3-cfb03c3b6f79" />

![WhatsApp Image 2025-11-25 at 13 30 15_df098720](https://github.com/user-attachments/assets/caf1039e-d3d3-4c2b-a0dc-f31867eb9f5d)

---

## **Result:**
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.

---
