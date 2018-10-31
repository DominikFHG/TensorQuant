<p align="center">

    ![TensorQuant](docs/TQ_Logo.svg?raw=true "TensorQuant")
</p>

# TensorQuant

## Features

* A toolbox for TensorFlow

* Investigate the effects of Quantization on a Deep Neural Network

* Use it with any user defined topology

* Applicable during inference and training

* Quantization on different levels (weights, activations, gradients)

* Choose different quantization for every layer

## Overview

TensorQuant is a toolbox for TensorFlow, which allows to investigate the effects of various quantization methods on deep neural networks. Its original purpose is to emulate custom numerical formats in Deep Neural Networks.
No changes to the local TensorFlow version are required and it is highly compatible between TensorFlow versions.

Given a model of a DNN written in TensorFlow, the user needs to specify a dictionary which maps layer IDs to quantization methods. After some minor modifications to the original model description, TensorQuant can quantize the model using any user-defined methods or one provided with the toolbox.

![Workflow](docs/TensorQuant_Overview.svg?raw=true "Workflow")

TensorQuant quantizes operators and variables by looping in additional nodes in the computational graph. Those insertions can be made to a very deep level, which effectively allows to emulate custom numerical formats, for example fixed-point formats.

![Looping In Quantization Nodes](docs/loop_in.png?raw=true "Looping In Quantization Nodes")

Quantization can be applied not only during inference, but also during training. This way, it is possible to train models with arbitrary numerical formats, for examples with binary, ternary or mixed precision weights.

## Links

* https://github.com/cc-hpc-itwm/TensorQuant  

* https://www.itwm.fraunhofer.de/en/departments/hpc/data-analysis-and-machine-learning/tensorquant-simulation-deep-learning-models.html

## Papers
* https://arxiv.org/abs/1710.05758  
* https://arxiv.org/abs/1808.08784

## Authors
Dominik Loroch (Fraunhofer ITWM)

![Fraunhofer](docs/fraunhofer.png?raw=true "Fraunhofer Logo")

Please reference to [this](https://arxiv.org/abs/1710.05758) paper.
