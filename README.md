# FGSM Adversarial
This project implements the FGSM method for generating adversarial noise based on the paper [Explaining and Harnessing Adversarial Examples](https://arxiv.org/abs/1412.6572) by Goodfellow, Shlens, and Szegedy.</br>
## Mechanics
The general idea is fairly straightforward, where we define the adversarial example as: 
```math
\large \bar{x} = x + \epsilon\cdot\text{sign}({\displaystyle \nabla_x}~J(\theta,x,y))
```
Where $J(\theta,x,y)$ is the loss, $x$ is the input image, $y$ is the category label, and $\epsilon$ is the intensity of the perturbation.</br></br>
In essence, we are taking backwards gradient descent and maximizing the loss instead of minimizing it.</br>
## Sample
Here's a sample of an adversarial attack using the pre-trained **resnext101_32x8d** model from PyTorch on ImageNet. </br></br>
![image](https://github.com/XDDz123/fgsm-adversarial/assets/20507222/2029c803-c1bb-4bbc-aafa-6878ba476d3e)

