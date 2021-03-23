[toc]

# Learning

Some papers on learning are recorded here.

## Backprop KF: Learning Discriminative Deterministic State Estimators
[PDF](https://papers.nips.cc/paper/2016/file/697e382cfd25b07a3e62275d3ee132b3-Paper.pdf)                                                         By Tuomas Haarnoja, Anurag Ajay, Sergey Levine, Pieter Abbeel Guang-Zhong Yang

This paper draws a connection between discriminative probabilistic state estimators (like Kalman filter) and recurrent computation graphs (like RNN). And train an end-to-end model to handle state estimation problem with raw image as input. The results show significant improvement over both standard generative methods and standard recurrent neural networks.

* Generate model aims to estimate the **distribution** over state observation sequences $o_{1:T}$ as originating from some underlying hidden state $x_{1:T}$. It is hard to handle rich sensory observations like images. **Joint distribution** or $P(X|Y=y)$

* A discriminative model is a model of the conditional probability of the target Y, given an observation x, symbolically, P ( Y | X = x ). **Conditional distribution**

I think it is nothing special. To my understanding on this paper, it just learn a feature detector and  combines it with Kalman filter for state estimation.
$$
\nabla_{\theta} \mathcal{L}(\theta) = \sum_{t=1}^T\frac{dz_t}{d\theta}\frac{ds_t}{dz_t}\frac{d\mathcal{L}}{ds_t}
$$
![Pipleline](img/backprob_KF.png)

