# Cubic Equation Solver using Neural Networks

This project demonstrates how to use a neural network to estimate a real root of a cubic equation of the form:

ax³ + bx² + cx + d = 0


It applies Stochastic Gradient Descent (SGD) and the Rectified Linear Unit (ReLU) activation function to approximate solutions through supervised learning. The model is trained on synthetic data and evaluated based on loss minimization.

## Features

- Predicts a real root of a cubic polynomial using a trained neural network.
- Streamlit web interface for interactive input and real-time predictions.
- Visualizes training loss over time.
- Clean and modular Python code using PyTorch.

## Project Structure

| File         | Description                               |
|--------------|-------------------------------------------|
| `model.py`   | Defines the `PolySolver` PyTorch model    |
| `train.py`   | Trains the model and saves weights        |
| `model.pth`  | Trained model weights                     |
| `app.py`     | Streamlit application for user interface  |
| `loss_plot.png` | Loss visualization during training     |

## Setup Instructions

### Installation

Install required packages:

```bash
pip install -r requirements.txt

### For Colab Users

If you're using Google Colab, you need to install additional dependencies and expose the Streamlit app using `ngrok`.

Install the required packages:

```bash
pip install streamlit pyngrok

Then run the following in a Colab cell to start the app:

```python
from pyngrok import ngrok
!streamlit run app.py &> /dev/null &
public_url = ngrok.connect(port=8501)
print("Streamlit app is live at:", public_url)
