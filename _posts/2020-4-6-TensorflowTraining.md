---
layout: post
title: Tensorflow Training Made Easy
category: MachineLearning, Tensorflow
---

I recently attended the UCL Deepmind [Tensorflow lecture series](http://www.csml.ucl.ac.uk/events/lunch_talks) before it got abrubptly ended by Covid19.  To continue this training I found the curated Tensforflow notebooks that explans the ML landscape as a series of modules within Tensorflow.  Here are links:

[📕 Module 2: Introduction to TensorFlow](https://colab.research.google.com/drive/1F_EWVKa8rbMXi3_fG0w7AtcscFq7Hi7B#forceEdit=true&sandboxMode=true)

[📗 Module 3: Core Learning Algorithms](https://colab.research.google.com/drive/15Cyy2H7nT40sGR7TBN5wBvgTd57mVKay#forceEdit=true&sandboxMode=true)

[📘 Module 4: Neural Networks with TensorFlow](https://colab.research.google.com/drive/1m2cg3D1x3j5vrFc-Cu0gMvc48gWyCOuG#forceEdit=true&sandboxMode=true)

[📙 Module 5: Deep Computer Vision](https://colab.research.google.com/drive/1ZZXnCjFEOkp_KdNcNabd14yok0BAIuwS#forceEdit=true&sandboxMode=true)

[📔 Module 6: Natural Language Processing with RNNs](https://colab.research.google.com/drive/1ysEKrw_LE2jMndo1snrZUh5w87LQsCxk#forceEdit=true&sandboxMode=true)

[📒 Module 7: Reinforcement Learning](https://colab.research.google.com/drive/1IlrlS3bB8t1Gd5Pogol4MIwUxlAjhWOQ#forceEdit=true&sandboxMode=true)

## Running Locally.

You can run the above notebooks either using CoLab resources or (like I do) run a local Jupyter Execution runtime using the following:

Pre-requisites
```
$python --version
3.x

$virtualenv --version
15.0.1

$pip3 --version
pip 19.1.1
```

Create a requirements file for the depdendencies required for the notebooks above.

```
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

```
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




