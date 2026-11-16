# Deep Learning Lab Practicals (SPPU BE IT, LP-IV)

Ready-to-run Jupyter notebooks for all six Deep Learning practicals. Each notebook gives a plain-words explanation of **what we are doing**, the code split into cells with notes, "poke" cells to see what's happening inside, a **break-it** experiment, and the **viva answers**.

📄 **[DL-Practicals-Study-Guide.pdf](DL-Practicals-Study-Guide.pdf)** is the whole thing as one document: basics glossary, line-by-line explanations, viva answers and a one-page cheat sheet.

| # | Practical | Notebook | Open in Colab |
|---|---|---|---|
| 1 | Study of DL packages (TensorFlow, Keras, PyTorch, Theano) | [P1](notebooks/P1_Study_of_Packages.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Tinker1988/dl-lab-practicals/blob/main/notebooks/P1_Study_of_Packages.ipynb) |
| 2 | Feedforward neural network on MNIST (SGD) | [P2](notebooks/P2_Feedforward_NN_MNIST.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Tinker1988/dl-lab-practicals/blob/main/notebooks/P2_Feedforward_NN_MNIST.ipynb) |
| 3 | CNN image classification on MNIST | [P3](notebooks/P3_CNN_MNIST.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Tinker1988/dl-lab-practicals/blob/main/notebooks/P3_CNN_MNIST.ipynb) |
| 4 | Autoencoder anomaly detection on ECG | [P4](notebooks/P4_Autoencoder_Anomaly_ECG.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Tinker1988/dl-lab-practicals/blob/main/notebooks/P4_Autoencoder_Anomaly_ECG.ipynb) |
| 5 | Continuous Bag of Words (CBOW) | [P5](notebooks/P5_CBOW_Word_Embeddings.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Tinker1988/dl-lab-practicals/blob/main/notebooks/P5_CBOW_Word_Embeddings.ipynb) |
| 6 | Transfer learning with VGG16 on CIFAR-10 | [P6](notebooks/P6_Transfer_Learning_VGG16.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Tinker1988/dl-lab-practicals/blob/main/notebooks/P6_Transfer_Learning_VGG16.ipynb) |

## Run in Google Colab
Click a badge above, then choose **Runtime → Change runtime type → T4 GPU** and run the cells from top to bottom. Nothing needs installing.

## Run locally in Jupyter
```bash
pip install -r requirements.txt
jupyter notebook
```
Or, in the first cell of a notebook: `%pip install tensorflow numpy pandas matplotlib scikit-learn`, then **Kernel → Restart Kernel**.

> The notebooks download their data (MNIST, CIFAR-10, the ECG CSV and the VGG16 ImageNet weights), so they need internet the first time they run. P6 is slow without a GPU.

## The shared skeleton
Every coded practical follows the same steps, and usually only the **model** block changes:

```
imports → load → preprocess → MODEL → compile → fit → evaluate → plot / predict
```
