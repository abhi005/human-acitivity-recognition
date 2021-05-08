# Human Acitivty Recognition
AN RNN based approach to recognize and classify the human activity recognition

# 1. Introcution
A Recurrent Neural Network (RNN) is a type of neural network that contains loops, allowing information to be stored within the network. In short, Recurrent Neural Networks use their reasoning from previous experiences to inform the upcoming events. Recurrent models are valuable in their ability to sequence vectors, which opens up the API to performing more complicated tasks. 

GRU Layer - As part of RNN architecture I am also using GRU layer for better runtime optimization. based on available runtime hardware and constraints, this layer will choose different implementations (cuDNN-based or pure-TensorFlow) to maximize the performance. If a GPU is available and all the arguments to the layer meet the requirement of the CuDNN kernel (see below for details), the layer will use a fast cuDNN implementation.

# 2. Data
The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. 

# 3. Model Architecture
Below is the RNN model architecture that I am following in this project
![Screenshot from 2021-05-08 20-13-27](https://user-images.githubusercontent.com/17639991/117543566-02b66900-b03b-11eb-8952-af92d8a1f90b.png)

# 4. Result & Analysis
![Screenshot from 2021-05-08 20-22-53](https://user-images.githubusercontent.com/17639991/117543607-33969e00-b03b-11eb-921d-df9383cbcaaa.png)
![Screenshot from 2021-05-08 20-23-22](https://user-images.githubusercontent.com/17639991/117543628-427d5080-b03b-11eb-9046-3a63d0adca37.png)

