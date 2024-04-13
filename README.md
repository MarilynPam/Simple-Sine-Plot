##sine wave
import numpy as np
import matplotlib.pyplot as plt

#define the sine wave function
def sine_wave(frequency, length, sample_rate):
    x = np.linspace(0, length, int(sample_rate * length))
    y = np.sin(frequency * 2 * np.pi * x)
    return x, y

#define the main function to plot the sine wave
def main():
    frequency = 10 #frequency in Hz
    length = 1 #length of time in seconds
    sample_rate = 1000 #sample rate in Hz

    x, y = sine_wave(frequency, length, sample_rate)

    plt.plot(x, y)
    plt.show()

#call the main function
if __name__ == "__main__":
    main()
    
