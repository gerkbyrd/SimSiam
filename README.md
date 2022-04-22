# DD2412 Deep Learning, Advanced Course, Project

In this project, we present our re-implementation of the [SimSiam](https://arxiv.org/abs/2011.10566) paper in PyTorch.


You can find the report at [SimSiam REPORT](addlinkhere).

# Abstract
This project aims to reproduce the popular SimSiam method for unsupervised image representation learning and investigate its optimization process, beyond the experimental procedures presented in the original paper. We reproduce the main method and conduct our additional investigations in a downscaled setting, both for convenience and to validate SimSiam and how it compares to relevant baselines under a different setup than the default. Our exploratory optimization approach relies on testing different loss functions, algorithms, and regularization. In summary, we reproduce and validate the empirical explorations performed in the original paper, while finding interesting deviations from their results. Furthermore, we perform additional empirical studies surrounding the optimization scheme of SimSiam, which, to the best of our knowledge, cover previously unexplored themes. We also propose potential avenues for optimization-based methodological improvements. 

# Structure
All our experiments are presented as Jupyter notebooks for simplicity, and our code is organized as follows:

SimSiamMainCode.ipynb contains our main implementation of SimSiam. It is written with the empirical studies of the original paper in mind, thus users can modify flags as indicated in the corresponding cell to perform pre-training under the different configurations used for this part of the original paper.

SimSiamExperimentsCode.ipynb contains the code to run our proposed experiments on SimSiam's pre-training optimization scheme, just as in the case of the reproduction of the original paper's empirical studies, the experiment is defined by the user by making use of the flags in the adequate cell. Different combinations of the configurations can be used to go beyond our implementation.

SimSiamLinEval.ipynb contains the code to perform the linear classifier evaluation of a trained SimSiam model by importing the weights of its pre-trained encoder. Optimization settings for the classifier and its architecture can be modified as well.

SimSiamSequentialExperiments.ipynb this notebook merely contains code that facilitates the execution of different SimSiam empirical study experiments for background execution.

The relevant code to run the official MoCo implementation for our setting is available in the Baselines/Originals/moco-main/moco-main folder.This can be done cloning and the repository and from within said directory, run main_moco.py from terminal to pre-train a ResNet-18 using MoCo and then main_lincls.py to evaluate it. Parameters can be changed following the official implementation's instructions.

# Source Control

Python 3.8

Tensorflow 2.6.1

Torch 1.10.0

# Citation
@article{DBLP:journals/corr/abs-2011-10566,
  author    = {Xinlei Chen and
               Kaiming He},
  title     = {Exploring Simple Siamese Representation Learning},
  journal   = {CoRR},
  volume    = {abs/2011.10566},
  year      = {2020},
  url       = {https://arxiv.org/abs/2011.10566},
  eprinttype = {arXiv},
  eprint    = {2011.10566},
  timestamp = {Wed, 25 Nov 2020 16:34:14 +0100},
  biburl    = {https://dblp.org/rec/journals/corr/abs-2011-10566.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}


#References for later:

https://arxiv.org/abs/2102.06191

https://www.robots.ox.ac.uk/~vedaldi/assets/pubs/bertinetto16fully.pdf
