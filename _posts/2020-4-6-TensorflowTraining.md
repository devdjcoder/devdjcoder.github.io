---
layout: post
title: Tensorflow Training
category: MachineLearning, Tensorflow

---

# Tensorflow Made Easy

I recently attended the UCL Deepmind Tensforlow lesture series before it got abrubptly ended by Covid19.  To continue this training I found the Tensforflow in 7hrs video blog which nicely breaks down machine learning models within tensorflow.  Here are links to the Jupyter web pages that can be run in CoLab so you can see a explanation of ML models.

📕 Module 2: Introduction to TensorFlow - https://colab.research.google.com/dri...

📗 Module 3: Core Learning Algorithms - https://colab.research.google.com/dri...

📘 Module 4: Neural Networks with TensorFlow - https://colab.research.google.com/dri...

📙 Module 5: Deep Computer Vision - https://colab.research.google.com/dri...

📔 Module 6: Natural Language Processing with RNNs -  https://colab.research.google.com/dri...

📒 Module 7: Reinforcement Learning -  https://colab.research.google.com/dri...

## Running Locally.

You can run the above notebooks either using CoLab resources or (like I do) run a local Jupyter Execution runtime using the following:

Pre-requisites
```bash

$python --version
3.x

$virtualenv --version
15.0.1

$pip3 --version
pip 19.1.1
```

Create a requirements file for the depdendencies required for the notebooks above.

```bash
jupyter_http_over_ws
wrapt>=1.11.1
google-cloud-core
requests<=2.21.0
six>=1.12.0
grpcio>=1.24.3
tensorflow>=2.x
keras

# Clash with Gym
# tensorflow_probability==0.8.0rc0
# cloudpickle=1.1.1

# GYM Has clash with tf_propbs
cloudpickle<1.4.0,>=1.2.0
gym

```

Create a VirtualVenv and run the following

```bash
$virtualenv venv
$source venv/bin/activate
(venv)$pip3 install -r requirements.txt
(venv)$jupyter serverextension enable --py jupyter_http_over_ws
(venv)$jupyter notebook \
  --NotebookApp.allow_origin='https://colab.research.google.com' \
  --port=8888 \
  --NotebookApp.port_retries=0

# Open the notebooks above and connect to the local runtime providing the url of the above output - ENJOY!!


```




