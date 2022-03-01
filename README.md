# Generating-Fourier-Basis

## Introduction

Nearly all of the time, the basis that we work in is the eigenbasis of the σ̂ <sup>z</sup> operator. To go from the computational basis to the Fourier basis for any use case, we use the QFT (quantum Fourier Transform) operator. However, sometimes it might not be possible to use conditional Rotational gates to apply QFT. For this purpose, we will create the QFT operation from scratch by training a variational circuit.

![Ciruit used to create QFT](circuit.png)

This is the circuit used to create QFT operator 

## What is Quantum Fourier Transform(QFT)?

The Fourier transform occurs in many different versions throughout classical computing, in areas ranging from signal processing to data compression to complexity theory. The quantum Fourier transform (QFT) is the quantum implementation of the discrete Fourier transform over the amplitudes of a wavefunction. It is part of many quantum algorithms, most notably Shor's factoring algorithm and quantum phase estimation.

The discrete Fourier transform acts on a vector (x<sub>0</sub>,...,x<sub>N−1</sub>) and maps it to the vector (y<sub>0</sub>,...,y<sub>N−1</sub>) according to the formula

<img src="https://latex.codecogs.com/png.image?\dpi{110}&space;\bg_white&space;y_k=\frac{1}{\sqrt{N}}\sum_{j=0}^{N-1}x_j\omega_{N}^{jk}" title="\bg_white y_k=\frac{1}{\sqrt{N}}\sum_{j=0}^{N-1}x_j\omega_{N}^{jk}" />

where <img src="https://latex.codecogs.com/png.image?\dpi{110}&space;\bg_white&space;\inline&space;\omega_{N}^{jk}&space;=&space;e^{2\pi&space;i\frac{jk}{N}}" title="\bg_white \inline \omega_{N}^{jk} = e^{2\pi i\frac{jk}{N}}" />

Similarly, the quantum Fourier transform acts on a quantum state 

