# Real-Time-Cashew-Kernel-Classification-Using-Deep-Learning


This project presents an automated, cost-effective solution for grading
cashew kernels in real time. We address the inefficiencies of
traditional manual grading, which is often slow and inconsistent due to
factors like human fatigue and varying light conditions. Our system uses
a combination of computer vision, deep learning, and embedded hardware
to improve the speed, accuracy, and reliability of the grading process.

## The Problem

Cashew kernels are graded for commercial value based on their shape,
size, and surface quality. Manual grading is a slow, subjective process
prone to human error, which affects both product quality and pricing.
With the growing demand for high-quality, export-grade kernels, there is
a clear need for an automated and scalable solution.

## Our Solution

Our automated grading system provides an end-to-end solution for this
challenge. The system's core is an intelligent classification pipeline
that operates in a real-time loop.

-   **Image Acquisition:** Cashew kernels are fed onto a conveyor belt
    one by one. A top-mounted webcam captures high-resolution images as
    the kernels move.

-   **Real-Time Classification:** The images are sent to a Raspberry Pi,
    which uses a pre-trained YOLOv5s deep learning model to classify the
    kernels into three commercial grades: W180, W300, and W500. The
    model was trained on a custom dataset created by capturing images
    under various lighting conditions to enhance its robustness in
    real-world environments.

-   **Automated Sorting:** The Raspberry Pi sends classification outputs
    to an Arduino Uno via a serial interface (UART). The Arduino then
    activates stepper motors and mechanical flaps to physically sort the
    kernels into their respective bins.

## Key Outcomes

-   **High Accuracy:** The system achieved a classification accuracy of
    over 93% and a physical sorting accuracy of 94--96% for the three
    target classes.

-   **Real-Time Performance:** The system performs real-time inference
    at 5 frames per second (FPS) on a low-cost Raspberry Pi. This is
    twice the throughput of traditional manual grading methods.

-   **Cost-Effective and Scalable:** By combining an AI-based detection
    model with low-cost embedded modules, the solution is both
    affordable and scalable for industrial applications, significantly
    reducing operational costs and labor dependency.
