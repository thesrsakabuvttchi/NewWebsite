---
title: "RCA-Sim: Reconfigurable Cycle-accurate Systolic Array Simulator"
description: "RCA-Sim is a specialized, cycle-accurate simulator for reconfigurable systolic arrays, designed to support research and development in approximate compute hardware for neural networks. RCA-Sim’s flexibility and extensiblity, allowing defenitions of custom P-units enables fine-grained testing, making it a valuable resource for hardware researchers focused on matrix multiplication efficiency."
heroImage: "/SystolicArray.png"
tags: ["C++", "Tensorflow", "Python"]
---

### Project Overview
RCA-Sim is a specialized, cycle-accurate simulator for reconfigurable systolic arrays, designed to support research and development in approximate compute hardware for neural networks. This tool allows users to test neural network accuracy within a hardware simulation, emulating the effects of custom P-Unit (Processing Unit) configurations and the impact of various approximation techniques. RCA-Sim’s flexibility enables fine-grained testing, making it a valuable resource for hardware researchers focused on matrix multiplication efficiency.

### Key Features

- **Cycle-Accurate Emulation**: RCA-Sim offers a high degree of accuracy in simulating hardware cycle-by-cycle, providing detailed metrics on data access, stall cycles, weight loading, and compute cycles. This helps users understand and evaluate performance and efficiency bottlenecks in systolic arrays.
  
- **Reconfigurable P-Units**: RCA-Sim includes options to configure systolic array P-Units, which enable testing of diverse hardware designs. Users can explore approximate computing scenarios by adjusting delays, truncating precision, or introducing other approximation methods to study trade-offs in accuracy and performance.

- **Customizable Systolic Array Configurations**: The simulator provides support for arbitrary systolic array dimensions and matrix sizes, allowing flexible experimentation. It can handle blocked matrix multiplication with automatic padding and splitting for matrix dimensions beyond the native array size.

- **Approximate Computation Support**: RCA-Sim is particularly suited for approximate computing research, where users can test custom hardware configurations to balance accuracy and power consumption. Features include multi-cycle delays, non-uniform delays, and bit-truncation for individual P-Units.

### Use Cases

- **Hardware Prototyping and Evaluation**: RCA-Sim is an invaluable tool for prototyping neural processing units (NPUs) and evaluating matrix multiplication performance on custom hardware. By allowing configuration of the P-Units and control over data flow within the systolic array, researchers can quickly assess the viability of different designs.
  
- **Neural Network Inference Testing**: The simulator is capable of running neural network inferences, allowing users to test models, including multi-layer perceptrons and deeper networks, within a cycle-accurate emulation environment. For example, when tested with quantized models trained on MNIST, RCA-Sim provided results matching hand-calculated values within floating-point error margins.

- **Approximate Hardware Research**: For researchers working with approximate computing, RCA-Sim enables testing of precision adjustments, such as truncating bits in P-Unit computations, to understand the trade-off between accuracy and performance. This feature is particularly useful for low-power devices that rely on approximate computation.

### Example Results

Using RCA-Sim, researchers can observe how approximation impacts model accuracy. For example, in a neural network model trained on MNIST, truncating the last two bits in P-Units reduced model accuracy from 89.36% to 88.46%, highlighting how sensitive different models are to hardware approximation. This functionality is highly beneficial for identifying model-hardware compatibility in approximate computing applications.

### Future Directions

The simulator is designed with scalability in mind, allowing for future expansions such as additional memory units, support for non-uniform delays, and more advanced scheduling algorithms. RCA-Sim could serve as the foundation for developing a fully reconfigurable NPU simulator, supporting a range of neural network models and hardware configurations.

### Conclusion
RCA-Sim provides a robust and adaptable platform for evaluating custom systolic arrays in the context of neural network inference. Its ability to emulate hardware cycles accurately and support approximate computation research makes it an ideal tool for researchers aiming to balance performance and accuracy in next-generation NPUs.
