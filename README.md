# Overview
I trained a convolutional neural network on CIFAR-10 Dataset
CIFAR-10 datasets is a collection of 60,000 images and 10 classes, with each class containing 6,000 images. The classes include:
airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck
The dataset is divided into 50,000 training images and 10,000 test images.

## 📄 Link to dataset:
https://www.kaggle.com/c/cifar-10

## 💻 Link to colab notebook:
https://colab.research.google.com/drive/1gGyManhq4t8z0AJF3UhbG0ba2KCaoS0r#scrollTo=6uxgdkh7lXh4

## 🤖 The model
A sequential model is used, as follows:
 Model: "sequential_1"
<table style="border-collapse: collapse; width: 100%; font-family: monospace;">
  <thead>
    <tr style="background-color: #f0f0f0;">
      <th style="border: 1px solid #ddd; padding: 12px; text-align: left;">Layer (type)</th>
      <th style="border: 1px solid #ddd; padding: 12px; text-align: center;">Output Shape</th>
      <th style="border: 1px solid #ddd; padding: 12px; text-align: right;">Param #</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">conv2d_6 (Conv2D)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 32, 32, 32)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">896</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">conv2d_7 (Conv2D)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 32, 32, 32)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">9,248</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">max_pooling2d_3 (MaxPooling2D)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 16, 16, 32)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">0</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">dropout_4 (Dropout)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 16, 16, 32)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">0</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">conv2d_8 (Conv2D)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 16, 16, 64)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">18,496</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">conv2d_9 (Conv2D)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 16, 16, 64)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">36,928</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">max_pooling2d_4 (MaxPooling2D)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 8, 8, 64)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">0</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">dropout_5 (Dropout)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 8, 8, 64)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">0</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">conv2d_10 (Conv2D)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 8, 8, 128)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">73,856</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">conv2d_11 (Conv2D)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 8, 8, 128)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">147,584</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">max_pooling2d_5 (MaxPooling2D)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 4, 4, 128)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">0</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">dropout_6 (Dropout)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 4, 4, 128)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">0</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">flatten_1 (Flatten)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 2048)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">0</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">dense_2 (Dense)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 512)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">1,049,088</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">dropout_7 (Dropout)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 512)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">0</td>
    </tr>
    <tr>
      <td style="border: 1px solid #ddd; padding: 12px;">dense_3 (Dense)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: center;">(None, 10)</td>
      <td style="border: 1px solid #ddd; padding: 12px; text-align: right;">5,130</td>
    </tr>
  </tbody>
</table>
 Total params: 1,341,226 (5.12 MB)

 Trainable params: 1,341,226 (5.12 MB)

 Non-trainable params: 0 (0.00 B)

## 📈 Results
The model is trained using 40 epochs with batch size = 64 and a callback with early stopping 
with min_delta = 0.02 and patience = 3.
<img width="547" height="413" alt="download" src="https://github.com/user-attachments/assets/1ed72e6f-6ef2-4d8c-8bcc-a379483c9577" />

