# driver_state_detection

This repository contains the code for a deep learning project that aims to detect driver state in real-time. The project was developed by Oussama Naji, Latifa El Bouga, and Soulala Achraf.

## Project Overview

The goal of this project is to develop a model that can detect the state of the driver in real-time using a camera. The model is trained on the state farm dataset which contains images of drivers in 10 different classes:

Item 1 : c0: safe driving
c1: texting - right
c2: talking on the phone - right
c3: texting - left
c4: talking on the phone - left
c5: operating the radio
c6: drinking
c7: reaching behind
c8: hair and makeup
c9: talking to passenger
We used the VGG16 model as a feature extractor and fine-tuned it by adding a GlobalAveragePooling2D layer and a dense layer with 10 neurons, each representing a class, and softmax activation function. The model was trained using the categorical cross-entropy loss function and the RMSprop optimizer. We achieved a test accuracy of 99.0858% and a test F1-score of 99.0856%.

## Deployment

We used a flutter application for the deployment of the model. The application allows the user to either import an image for prediction or to do real-time prediction using the device's camera. The interface is easy to use and the application also saves the sessions of the real-time prediction in a Firebase NoSQL database. The application also provides a barplot to visualize data and time spent by the driver while driving in each class.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
