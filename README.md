# HyperLock: Privacy-Preserving Federated Learning with Encrypted Gradients

This project demonstrates a privacy-preserving federated learning setup using **TensorFlow**, **TenSEAL**, and **Optuna**. The implementation leverages homomorphic encryption to securely aggregate gradients from multiple clients without exposing their individual data. Hyperparameter optimization is performed using Optuna to maximize the model's accuracy.

## Features

- **Federated Learning**: Simulates multiple clients collaborating on training a global model without sharing raw data.
- **Privacy-Preserving Encryption**: Uses the TenSEAL library for homomorphic encryption to secure gradients during federated averaging.
- **Hyperparameter Optimization**: Integrates Optuna to optimize model hyperparameters such as the number of units in hidden layers and the learning rate.
- **MNIST Dataset**: Demonstrates the process using the MNIST dataset for digit classification.

---

## Prerequisites

Ensure the following dependencies are installed in your environment:

- Python 3.8 or later
- TensorFlow >= 2.6.0
- Optuna >= 3.0.0
- TenSEAL >= 0.3.0
- NumPy

Install dependencies with:

```bash
pip install tensorflow optuna tenseal numpy
```
## How It Works
### Workflow
Data Preparation: The MNIST dataset is preprocessed and split across simulated clients.

Encryption Initialization: A CKKS encryption context is created using TenSEAL.

Federated Learning:

  * Each client computes local gradients.

  * Gradients are encrypted and sent to the server.

  * The server decrypts and averages the gradients to update the global model.

  * Hyperparameter Optimization: Optuna searches for the best hyperparameters to maximize model accuracy.
    
# Performance
The project is designed to balance privacy and performance. Note that the use of encryption may increase computation and memory requirements. For better performance, ensure you have access to a GPU.

# Contributions
Contributions are welcome! Feel free to open an issue or submit a pull request.

# License
This project is licensed under the MIT License. See the LICENSE file for details.

# Acknowledgments
TensorFlow
TenSEAL
Optuna
MNIST Dataset
