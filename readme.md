# Increasing naturaness of human-machine dialogue.
 
This project includes two network for reverse QA, namely, UCINet for the inference of  user's choices on options in machine-raised questions, and SAGNet for automatic answer generation.<br>

Setups
-------  
The requiring environment is as bellow:<br>
* python 3.8<br>
* tensorflow 1.15.0<br>

Running Explainable weighting framework on benchmark datasets (CIFAR-10 and CIFAR-100).
-------  
Here are two examples for training imbalanced and noisy data:<br>
ResNet32 on CIFAR10-LT with imbalanced factor of 10:<br>

`python main.py --dataset cifar10 --imbalanced_factor 10`

ResNet32 on noisy CIFAR10 with 20\% pair-flip noise:<br>
`python main.py --dataset cifar10 --corruption_type flip2 --corruption_ratio 0.2`

The default sample weighting network in the code is Neural Regression Tree with pruning. You can also use MLP as the sample weighting network. Both the two networks are in the file ``model.py".
