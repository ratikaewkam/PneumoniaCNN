# PneumoniaCNN
Pneumonia Detection Using Convolutional Neural Network

### Idea
I want to build a neural network model that can predict pneumonia. I started by researching neural network architectures, such as AlexNet and VGG. These models use ReLU as their activation function. I wanted to take a different approach and achieve different results, so I began exploring other activation functions like ELU and GELU. Over the course of three months, I designed a new architecture multiple times. Finally, the results were promising.

---

### PXRVision Architecture
- Input (224x224 Grayscale)
- Conv7-s2-64 (ELU) + Conv5-s1-64 (GELU)
- Maxpool3-s2
- Conv3-s1-128 (ELU) + Conv3-s1-128 (GELU)
- Maxpool3-s2
- Conv3-s1-256 (ELU) + Conv3-s1-256 (GELU)
- Maxpool3-s2
- Conv3-s1-512 (ELU) + Conv3-s1-512 (GELU)
- Maxpool3-s2
- Conv3-s1-512 (ELU) + Conv3-s1-512 (GELU)
- Maxpool3-s2
- FC-4096 (ELU) + Dropout 0.5
- FC-4096 (GELU) + Dropout 0.5
- FC-1 (Sigmoid)

### Result
Highest accuracy : 94.87% (Test 5 times)

### References
[Dataset](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia) | 
[Code](https://www.kaggle.com/code/madz2000/pneumonia-detection-using-cnn-92-6-accuracy) | 
[VGG](https://arxiv.org/pdf/1409.1556) | 
[ELU](https://arxiv.org/pdf/1511.07289) | 
[GELU](https://arxiv.org/pdf/1606.08415)

---

Developed by [Rati Kaewkam](https://github.com/ratikaewkam)