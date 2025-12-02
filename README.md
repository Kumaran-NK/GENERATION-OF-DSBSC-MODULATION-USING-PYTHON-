
---

# **DSB-SC Modulation Using Python**

## **AIM**

To implement and analyze **Double Sideband Suppressed Carrier (DSB-SC)** modulation using Python’s NumPy and Matplotlib libraries.

---

## **EQUIPMENTS REQUIRED**

### **Software**

* Python 3.x
* NumPy
* Matplotlib

### **Hardware**

* Personal Computer

---

## **ALGORITHM**

1. **Initialize Parameters**
   Set values for:

   * Carrier frequency
   * Message frequency
   * Sampling frequency
   * Signal duration

2. **Generate Time Axis**
   Create a time vector using NumPy.

3. **Generate Message Signal**
   Define the message signal as a cosine wave.

4. **Compute the Integral of the Message Signal**
   Calculate cumulative integral using NumPy functions (if required).

5. **Generate DSB-SC Signal**
   Apply the DSB-SC formula:
   [
   s(t) = m(t) \cdot c(t)
   ]

6. **Plot the Signals**
   Use Matplotlib to plot:

   * Message Signal
   * Carrier Signal
   * Modulated Signal

---

## **PROGRAM (Python)**

```python
import numpy as np
import matplotlib.pyplot as plt

# Parameters
fm = 5        # Message frequency
fc = 50       # Carrier frequency
fs = 1000     # Sampling frequency
t = np.arange(0, 1, 1/fs)

# Message signal
m = np.cos(2 * np.pi * fm * t)

# Carrier signal
c = np.cos(2 * np.pi * fc * t)

# DSB-SC Modulated signal
s = m * c

# Plotting
plt.figure(figsize=(12, 8))

plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.title("Message Signal")
plt.xlabel("Time (s)")
plt.ylabel("Amplitude")

plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.title("Carrier Signal")
plt.xlabel("Time (s)")
plt.ylabel("Amplitude")

plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.title("DSB-SC Modulated Signal")
plt.xlabel("Time (s)")
plt.ylabel("Amplitude")

plt.tight_layout()
plt.show()
```

---

## **OUTPUT GRAPH**
<img width="825" height="531" alt="image" src="https://github.com/user-attachments/assets/fc4433b3-f598-4855-be01-21c16c4f2134" />


---

## **TABULAR COLUMN**

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/a4fa5674-4b4a-454c-8eb9-b83a0342e4b4" />


---

## **RESULT**

Thus, the **DSB-SC AM Modulation** was successfully generated and analyzed using Python.

---
