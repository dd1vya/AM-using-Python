# AM USING PYTHON

### Aim:
To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries.

### Apparatus Required:
Software: Python with NumPy and Matplotlib libraries
Hardware: Personal Computer

### Theory:
Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting
information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of
the message signal. The general form of an AM signal is:
<img width="745" height="575" alt="image" src="https://github.com/user-attachments/assets/4f3e7352-767d-4841-a0f2-f27a2cfa163e" />


### Program:
```
import numpy as np
import matplotlib.pyplot as plt

am=6.6
fm=554
ac=13.2
fc=5540
fs=55400
t=np.arange(0, 2/fm, 1/fs)

m = am * np.cos(2 * np.pi * fm * t)
plt.subplot(3,1,1)
plt.plot(t, m)

c = ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3,1,2)
plt.plot(t, c)

s = (ac + m) * np.cos(2 * np.pi * fc * t)
plt.subplot(3,1,3)
plt.plot(t,s)
plt.title("AM")


plt.tight_layout()
plt.show()
```

### Output Waveform:
<img width="630" height="469" alt="image" src="https://github.com/user-attachments/assets/484b8eba-ad2a-4682-8aa7-e8f0f526d6f4" />


### Tabular Column:

### Algorithm:
1. Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency.
2. Generate Time Axis: Create a time vector for the signal duration.
3. Generate Message Signal: Define the message signal as a cosine wave.
4. Generate Carrier Signal: Define the carrier signal as a cosine wave.
5. Modulate Signal: Apply the AM formula to obtain the modulated signal.
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

### Result:
The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots.
Thus AM is implemented using numPy and Matplotlib.
