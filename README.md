# Quantum-Neural-Network-QNN-for-Image-Classification
A Quantum Neural Network (QNN) is a machine-learning model that uses quantum circuits instead of classical layers to learn patterns from data. For image classification, the input image is first preprocessed and encoded into quantum states using techniques like angle encoding or amplitude encoding.

Goal: Use quantum systems to learn patterns from small images.

Why small images?

Because today’s quantum computers have very few qubits, so we start with 4×4 (16-pixel) images

🔹 2. Problem Statement

Build a hybrid classical–quantum model that classifies 4×4 grayscale images using a small quantum circuit.

Input: 4×4 grayscale image → 16 features

Output: Probability that the image belongs to class 0 or 1
 
 our output belongs to class 1

 ![alt text](image.png)

🔹 3. Why Use Quantum ML?

Quantum layers may:

i . Encode 16 features into a 4-qubit quantum state efficiently

we have entered a 16 pixel values:

1 1 0 0 1 0 0 0 0 0 0 1 0 0 1 1

ii . Use superposition + entanglement to capture correlations

iii . Potentially learn patterns that are difficult for classical models

🔹 4. Dataset Used

A synthetic 4×4 image dataset

Two classes:

Class 0 → bright area in top-left

Class 1 → bright area in bottom-right

Small, clean, ideal for quantum experiments

🔹 5. QNN Architecture (Simple + Effective)
A. Feature Encoding Layer

16 pixels → 4 qubits

Each qubit encodes 4 pixels (summed into rotation angle)

Encoding uses Ry(angle)

B. Variational Quantum Layer

Trainable parameters θ

Applied using Rx gates

C. Entanglement Layer

A chain of CNOT gates

Allows qubits to share information

Creates quantum correlations between features

D. Measurement

Measure Z expectation value (⟨Z⟩) of each qubit

Produces a 4-dimensional feature vector

E. Classical Output Layer

Linear combination:

logit = w · exps + b

Apply sigmoid → probability of class 1

🔹 6. Training

Use COBYLA optimizer (gradient-free)

Input: parameters θ + classical weights w + bias b

Loss: binary cross-entropy

Train on a small subset (80 samples) → runs fast on a laptop.

🔹 7. Advantages of Your Approach

Fully quantum-based neural network

Uses only Qiskit + SciPy

Very clean, minimal code

Easy to present + demonstrate

🔹 8. Limitations (Mention in Presentation)

Quantum simulation is slow for large numbers of qubits

Real quantum computers have high noise

Works only for tiny images

Not yet better than classical CNNs

(But still extremely good for research + learning.)

🔹 9. Applications

Even though QNNs are early-stage, they show potential for:

Medical imaging (tiny grayscale scans)

Pattern recognition

Quantum feature extraction

Quantum-enhanced ML research











