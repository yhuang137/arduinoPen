# Arduino Pen

## Motivation
During the covid-19 pandemic, many people have to work from home. For those who used to do heavy paperwork, the transition from paper to computer typing may not be smooth and easy. However, most of the stylus pens on the market only work on a touchscreen device, which don’t provide the physical feedback of writing on paper. Therefore, we would like to design an electronic pen that can write on the paper and transcribe handwritten characters into computer notes. 

## Goal
Our goal is to build a stylus pen on an Arduino Nano 33 BLE microcontroller, and utilize the machine learning skill to transcribe 0-9 digits and simple math operators (+, -, *, /, =)  written on a horizontal surface. 

## Technical Approach
An inertial measurement unit (IMU) tracks the pen location and motion, then the arduino transmits the signal of the movements via bluetooth to a computer.  By the reference of the paper The OnHW Dataset: Online Handwriting Recognition from IMU-Enhanced Ballpoint Pens with Machine Learning (FELIX OTT, 2020), the paper classified different handwriting digits and characters using different neural networks, and comes out that convolutional neural networks have the highest accuracy. Therefore, the motion signal will be processed and sent to a convolution neural network. 
Our project is composed of the procedures of data collection, signal processing, and deep learning neural networks. 


