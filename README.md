# vae-bss
  
A PyTorch model of the variational auto-encoder for unsupervised blind source separation, with training and evaluation programs, as described in

* J. Neri, R. Badeau, P. Depalle, “**Unsupervised Blind Source Separation with Variational Auto-Encoders**”, 29th European Signal Processing Conference (EUSIPCO), Dublin, Ireland, August 2021.

 Author: Julian Neri

## Instructions

### Installation

Install the python packages listed in the "requirements.txt" file in the main directory of this repository.
You can do so by executing the following command:

1. Open the unix shell (terminal for mac users)
2. Change working directory to 'vae-bss-master'
3. Execute this command: pip install -r requirements.txt

### Usage

Run either the "evaluate.py" or "train.py" files.
* For example, enter this command in terminal: python3 evaluate.py

**evaluate.py** uses a pre-trained (unsupervised) variational auto-encoder to separate the mixed MNIST handwritten digit images.
Results for K = 2, 3, 4 assumed sources are saved in the results directory.

**train.py** trains a VAE model on MNIST data, demonstrating the training procedure described in our paper.
The number of epochs for training / testing is defined in "argparser.py". The other arguments defined in that file allow you to try different hyperparameters and settings for model training / specification, such as the dimension of the latent space, the prior probability, and the batch size.

Either program will first download the MNIST data and prepare it as training and testing data sets. Note that it will only do this once, as the datset will be saved in a directory that will be recalled for subsequent use.

