# Arduino Pen
<br />

## Motivation
During the covid-19 pandemic, many people have to work from home. For those who used to do heavy paperwork, the transition from paper to computer typing may not be smooth and easy. However, most of the stylus pens on the market only work on a touchscreen device, which don’t provide the physical feedback of writing on paper. Therefore, we would like to design an electronic pen that can write on the paper and transcribe handwritten characters into computer notes.
<br />
<br />

## Goal
Our goal is to build a stylus pen on an Arduino Nano 33 BLE microcontroller, and utilize the machine learning skill to transcribe 0-9 digits and simple math operators (+, -, *, /, =)  written on a horizontal surface. 
<br />
<br />

## Stretch Goal
All team members are right-handed, so our system lacks the training data of left-handed writing motions. If time allows, we would like to make our design work well with left-handed people. 
<br />
<br />

## Technical Approach
An inertial measurement unit (IMU) tracks the pen location and motion, then the arduino transmits the signal of the movements via bluetooth to a computer.  By the reference of the paper The OnHW Dataset: Online Handwriting Recognition from IMU-Enhanced Ballpoint Pens with Machine Learning (FELIX OTT, 2020), the paper classified different handwriting digits and characters using different neural networks, and comes out that convolutional neural networks have the highest accuracy. Therefore, the motion signal will be processed and sent to a convolution neural network. 
Our project is composed of the procedures of data collection, signal processing, and deep learning neural networks. 
<br />
<br />

**Data collection:** We will write each digit and operator in different styles, and different pen-holding gestures, which means that we can imitate the MNIST data sets,  then we collect the raw data from the IMU.
**Communication:** We will use bluetooth to transmit messages between Arduino and computer. 
**Signal processing:** We will filter and transform the raw motion data to an imaginary “image”. 
**Neural Network:** the CNN will classify the handwritten characters based on the “image” input. 
<br />
<br />

## Literature Review
https://dl.acm.org/doi/pdf/10.1145/3411842

## Milestones
**Week 5:** Successfully set up the hardware (IMU) and software (Python) environment. Build up wireless communication between the device and computer.  
**Week 7:** Collect data and train a robust neural network to process writing motion data. 
**Week 9:** Finalize the design and prepare the video presentation. 
