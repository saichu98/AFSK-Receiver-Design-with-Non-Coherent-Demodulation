# AFSK Receiver Design with Non-Coherent Demodulation


## Overview
This project focuses on implementing an AFSK (Audio Frequency Shift Keying) receiver using non-coherent demodulation. The main learning objectives include signal analysis, RF filtering, and handling noisy conditions. The assignment is divided into two parts: RF signal analysis using GQRX and MATLAB, followed by signal processing to filter and demodulate the AFSK signal.

## Learning Objectives:
- Implement an AFSK receiver with non-coherent demodulation
- Analyze and interpret RF spectrum measurements
- Design and apply filters to extract signals under noisy conditions

## Tools Used:
- **GQRX** for RF signal analysis
- **MATLAB** for signal processing and filtering
- **GNU Radio**

---

## Instructions

### Part 1: RF Signal Analysis in GQRX

1. **Open GQRX**: Play the provided recording `gqrx_20221119_195628_904000000_2000000_fc.raw`.
2. **Visualize the signal**: Adjust GQRX settings to view the transmitted signal in both the spectrum and spectrogram.
3. **Identify Center Frequency**: Understand the center frequency of the AFSK signal.
4. **Demodulation**: Use AM demodulation in GQRX and record the audio containing the FSK tones.
5. **Data Rate Estimation**: Listen to the tones and estimate the data rate in bits per second.

### Part 2: RF Signal Analysis in MATLAB

1. **Load Samples**: Read the `.raw` file into MATLAB and discard the imaginary part of the signal.
2. **Plot the Spectrum**: Plot the magnitude spectrum and spectrogram, zooming in to identify the frequency band of interest.

### Part 3: Noise Reduction with BPF

1. **Design a Band-Pass Filter**: Create an FIR filter with a passband matching the frequencies identified earlier.
2. **Filter the Signal**: Apply the filter to the received signal.
3. **Plot Results**: Plot the filtered signal and its spectrum.

### Part 4: Non-Coherent Demodulation and AFSK Tone Detection

1. **Down-conversion**: Compute the magnitude of the filtered signal and reduce its sampling rate.
2. **Tone Identification**: Plot the spectrogram and identify the start and end of the AFSK tones.
3. **Design Filters**: Create two band-pass filters for each tone and apply them to the signal.
4. **Plot Results**: Plot the filtered signals corresponding to the FSK tones.

### Part 5: Bits Detection

1. **Low-Pass Filtering**: Design a low-pass filter with a cutoff frequency of 20 Hz and apply it to the signals.
2. **Extract Bits**: Use the filtered signals to detect the bit sequence.
3. **Submit Screenshots**: Plot of the processed signals.

---
