# FM-using-Python

# Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

# Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
# Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



# Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

# Program

```
import numpy as np
import matplotlib.pyplot as plt

Am=3.8
Ac=7.6
fc=3220
fm=322
fs=32200
beta=3.9
t=np.arange(0, 2/fm, 1/fs)
m=Am* np.cos(2*np.pi*fm*t)

c=Ac* np.cos(2*3.14*fc*t)

efm=Ac*np.cos((2*np.pi*fc*t)+beta*np.sin(2*np.pi*fm*t))

plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.show()

plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.show()

plt.subplot(3, 1, 3)
plt.plot(t,efm)
plt.show()
```

# Output Waveform

<img width="739" height="579" alt="image" src="https://github.com/user-attachments/assets/4ee37199-2d3c-44c8-b1fa-f75b45932dc7" />


## Tabular Column

![WhatsApp Image 2025-10-23 at 22 13 40_505841f5](https://github.com/user-attachments/assets/81e1756a-a17c-4254-993a-79803af81666)


## Calculation

![WhatsApp Image 2025-10-23 at 22 13 41_0ea9c4e4](https://github.com/user-attachments/assets/adde5616-2b29-400f-90d2-cb9325311de1)

## Result

The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.

