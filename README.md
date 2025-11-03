EXPT.NO.7 Amplitude Modulation and Demodulation using NumPy and Matplotlib Aim

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. Apparatus Required Software: Python with NumPy and Matplotlib libraries

Hardware: Personal Computer

Theory

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of the message signal. The general form of an AM signal is:

Algorithm

Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency.
Generate Time Axis: Create a time vector for the signal duration.
Generate Message Signal: Define the message signal as a cosine wave.
Generate Carrier Signal: Define the carrier signal as a cosine wave.
Modulate Signal: Apply the AM formula to obtain the modulated signal.
Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

program:

    import numpy as np
    import matplotlib.pyplot as plt
    Am = 4.6
    Ac = 9.2
    fm = 377
    fc = 3770
    fs = 37700
    t = np.arange(0, 2/fm, 1/fs)
    m = Am * np.cos(2 * np.pi * fm * t)
    plt.subplot(3, 1, 1)
    plt.plot(t, m)
    c = Ac * np.cos(2 * np.pi * fc * t)
    plt.subplot(3, 1, 2)
    plt.plot(t, c)
    s = (Ac + m) * np.cos(2 * np.pi * fc * t)
    plt.subplot(3, 1, 3)
    plt.plot(t, s)
    plt.tight_layout()
    plt.show()

output :

<img width="627" height="469" alt="ajac" src="https://github.com/user-attachments/assets/df2840b2-71f9-4149-a467-c23193f134a5" />

calculation:

![WhatsApp Image 2025-11-03 at 21 42 10_7d0b32d5](https://github.com/user-attachments/assets/a74dec8e-43bb-422a-8a6c-9b9d5463f7f9)

Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. Thus AM is implemented using numPy and Matplotlib.


