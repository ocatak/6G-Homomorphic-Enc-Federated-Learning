# Homomorphic Encryption with Federated Learning for Channel Estimation in AI Based 5G/6G Wireless Networks

## Overview

This repository contains a Python script for implementing Federated Learning (FL) for channel estimation using a deep learning model. The FL process involves training a model collaboratively across multiple clients without exchanging raw data.

## Getting Started

### Prerequisites

Make sure you have the required packages installed:

```bash
pip install pyfhel==3.1.0
pip install -q plot_keras_history
```

### Dataset

The code uses the [6G Channel Estimation Dataset](https://github.com/ocatak/6g-channel-estimation-dataset) available as `data.mat`. You can download it using the following command:

```bash
wget -q -O data.mat https://github.com/ocatak/6g-channel-estimation-dataset/blob/main/data.mat?raw=true
```

## Usage

### Google Colab Setup

If you are running this script on Google Colab, follow the setup instructions at the beginning of the script to mount your Google Drive.

```python
from google.colab import drive
drive.mount("/content/gdrive")
```

### Model Training

Adjust the hyperparameters (`HYPARAMETER_TUNING`, `TRAIN_MODEL`, etc.) as needed. Run the script to train the model.

```python
!python Channel_Estimation_FL_2.ipynb
```

### Results

The script generates visualizations of pilot signals and actual channels, as well as a model summary. The training history plot is also available but commented out.

## Federated Learning Process

The script demonstrates federated learning with a specified number of clients (`num_of_client_list`). The process involves training each client, encrypting the model weights, aggregating the models, and decrypting for evaluation.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Original script: [Colab Notebook](https://colab.research.google.com/drive/1ghsqfX0qyd-12gxrbB51u0Px0qF88m6F)
- Dataset: [6G Channel Estimation Dataset](https://github.com/ocatak/6g-channel-estimation-dataset)

Feel free to modify this README according to your project's specific details and requirements.

