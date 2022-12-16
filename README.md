# Neural Style Transfer

These python notebooks contain the code to run our experiments for neural style transfer

## Contributors
  - Zihao Deng (zihaoden@seas.upenn.edu)
  - Xuanmin Zhu (xuanminz@seas.upenn.edu)


# Code for running the experiments on Image style transfer

We have all the code for doing image style transfer and the corresponding experiments in the notebook ``neural_style_transfer.ipynb``
This notebook contains the additional steps to work on neural style transfer on videos ``NeuralStyleTransfer_video.ipynb``

## Structure of the code framework
We have structured the code into sections, and the overall framework is shown below. Note that you do not need to install any packages and all of the libraries we have used are already installed in a default Colab environment. But you will need to connect to a GPU runtime in order for the code to work.

```
Imports and Preprocess
CNN Models
Style Loss
Content Loss
Model with Loss
  ├──VGG19
  ├──AlexNet
  ├──ResNet
Neural Style Transfer
Experiments
  ├──Image Evaluation Metric
  ├──Experiment: CNN Model
  |    ├──VGG19
  |    ├──AlexNet
  |    ├──ResNet
  ├──Experiment: Loss Function
  |    ├──L1 Loss
  |    ├──Smooth L1 Loss
  |    ├──Huber Loss
  |    ├──Restore MSE Content Loss
  ├──Experiment: Optimizer
       ├──Adam
       ├──SGD
       ├──Restore LBFGS optimizer
AMP
Generate Beautiful Image

```
Code for running the experiments on Image style transfer
```
For the video neural style transfer, the retained structure consists of:
```
Loading script with tools to compute optical flow
Naive implementation
Total variation loss
Incorporate TVLoss into the base model

along with the scripts to generate the output and compute the optical flow. The optical flow script is from a public repo, and the instruction to generate image frames and optical flow is as stated on the README.md of that repo.
You can easily run the code sequentially to reproduce all the results.
But you will need to upload your own images and make sure the file names matches strings in the notebook.
