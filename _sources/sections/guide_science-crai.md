# Science for an OGC Building Block for climate services

## Example CRAI (Climate Reconstruction AI)

[CRAI](https://github.com/FREVA-CLINT/climatereconstructionAI/tree/clint) is a state-of-the-art deep learning based inpainting technology to infill missing values in climate datasets.

## The method

The infilling algorithm is trained with complete climate datasets and masks defining realistic regions of missing observational data.

```{figure} /media/pconv-unet.png
```

As shown in the figure, the neural network has a U-net architecture and makes use of *partial convolutional layers* instead of standard convolution layers. A *partial convolutional layer* is a combination of two successive operations:

- a partial convolution:
$x'=\left\{\begin{array}{ll}\boldsymbol{W}^T\left(\boldsymbol{X}\odot\boldsymbol{M}\right) \frac{\text{sum}(\boldsymbol{1})}{\text{sum}(\boldsymbol{M})} +b, & \text{if sum}(\boldsymbol{M})>0 \\ 0, &\text{otherwise}\end{array}\right.$

- a mask update:
$m'=\left\{\begin{array}{ll}1, & \text{if sum}(\boldsymbol{M})>0 \\ 0, &\text{otherwise}\end{array}\right.$

where $\boldsymbol{W}$ are the convolution filter weights, $\boldsymbol{X}$ the feature values, $\boldsymbol{M}$ the binary mask values and $b$ the bias.

Compared to other inpainting methods [^1], the partial convolution technique offers several advantages:
- it operates robustly on irregular holes
- it can infill large holes
- it produces semantically meaningful predictions

[^1]: [Liu, G. *et al.*, *Computer Vision—ECCV 2018 Lecture Notes in Computer Science* 11215, 19-35 (2018)](https://doi.org/10.1007/978-3-030-01252-6_6)

## Installation

CRAI is written in Python and based on the PyTorch framework and the NVIDIA CUDA® Deep Neural Network library (cuDNN). It is licensed under the terms of the BSD 3-Clause.

Step 1: clone the branch of the repository:
```bash
git clone -b clint --single-branch https://github.com/FREVA-CLINT/climatereconstructionAI.git
```

Step 2: create en environment with all the required dependencies using Anaconda
```bash
conda env create -f environment.yml
```

Step3: activate the environment
```bash
conda activate crai
```

Step4: install the Python package using pip
```bash
pip install .
```

## Usage

The software can be used to:
- train a model (**training**)
- infill climate datasets using a trained model (**evaluation**)

It can be used as:
- a command line interface (CLI):
  - training:
  ```bash
  crai-train
  ```
  - evaluation:
  ```bash
  crai-evaluate
  ```
- a Python library:
  - training:
  ```python
  from climatereconstructionai import train
  train()
  ```
  - evaluation:
  ```python
  from climatereconstructionai import evaluate
  evaluate()
  ```

For more details about the execution and the input arguments, please have a look to the documentation and demo examples hosted in the [repository](https://github.com/FREVA-CLINT/climatereconstructionAI/tree/clint)
