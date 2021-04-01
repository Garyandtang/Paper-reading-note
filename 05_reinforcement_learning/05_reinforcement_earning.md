[toc]

# Reinforcement Learning

Some papers on reinforcement learning are archived here.

Good reference on reinforcement learning:

* [Stanford CS234](https://web.stanford.edu/class/cs234/): CS234 is always the best course for studying reinforcement learning which is recommended by all of my colleagues . Ashamed to say, I did not take this course.
* [DRL by Hung-yi Lee](https://www.youtube.com/watch?v=z95ZYgPgXOY&list=PLJV_el3uVTsODxQFgzMzPLa16h6B8kWM): great reinforcement learning course in Chinese by Prof. Hung-yi Lee from NTU.
* [introRL by Bolei Zhou](https://github.com/zhoubolei/introRL): Brief introduction to RL in Chinese by Prof. Bolei Zhou from CUHK. They provide many codes on RL algorithms in Python and Pytorch, which can be found [here](https://github.com/cuhkrlcourse/RLexample) .
* Note by Lil: 
  * [Deep reinforcement learning intro](https://lilianweng.github.io/lil-log/2018/02/19/a-long-peek-into-reinforcement-learning.html#key-concepts)
  * [Policy gradient Algorithms](https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html)
* Book: 
  * [Reinforcement Learning: An Introduction by Richard S. Sutton and Andrew G. Bartoi](https://web.stanford.edu/class/psych209/Readings/SuttonBartoIPRLBook2ndEd.pdf)

## SCC: an efficient deep reinforcement learning agent mastering the game of StarCraft II

[PDF](https://arxiv.org/pdf/2012.13169.pdf)                       																															      BY inspir.ai

Papers on mastering the game of StarCraft II with deep reinforcement learning, key idea is based on  AlphaStar [1], major differences are:

* Less data for training. 

* Modify the network architecture with group transformer, attention-based pooling.
* League training for more diversity

Did AlphaStar use Single-agent setting, imitation learning?

#### Key components

**Network Architectures for small games **

Single agent with reduce network to handle the sacrifice of 小兵.

Resnet to handle spatial  information.

Transformer to handle: 

LSTM/RNN to handle 

Self attention layer to make decisions. 



**Network Architectures for full games **

**Imitation Learning**

To learn from human experts. Use KL divergence during RL training, how to balance the treat off between imitation learning and reinforcement learning is by using different hyper parameter(调参)

**League training**

To my understanding, it is like self-confrontation during the training, to let agent become more diverse.

**Reward function**

* Sparse Win or Loss reward.
* strategy statistic z.  The strategy statistic z are extracted from human replays which encode constructed buildings and units present during a game.
* Try to use the StarCraft II Scoring mechanism  but it did not work well.

[1] O. Vinyals, I. Babuschkin, W. M. Czarnecki, M. Mathieu, A. Dudzik, J. Chung, D. H. Choi,R. Powell, T. Ewalds, P. Georgiev,et al., “Grandmaster level in starcraft ii using multi-agentreinforcement learning,”Nature, vol. 575, no. 7782, pp. 350–354, 2019.

[2] O. Vinyals, I. Babuschkin, J. Chung, M. Mathieu, M. Jaderberg, W. Czarnecki, A. Dudzik,A. Huang, P. Georgiev, R. Powell, T. Ewalds, D. Horgan, M. Kroiss, I. Danihelka, J. Agapiou,J. Oh, V. Dalibard, D. Choi, L. Sifre, Y. Sulsky, S. Vezhnevets, J. Molloy, T. Cai, D. Budden,T. Paine, C. Gulcehre, Z. Wang, T. Pfaff, T. Pohlen, D. Yogatama, J. Cohen, K. McKinney,O.  Smith,  T.  Schaul,  T.  Lillicrap,  C.  Apps,  K.  Kavukcuoglu,  D.  Hassabis,  and  D.  Silver,“AlphaStar: Mastering the Real-Time Strategy Game StarCraft II.”https://deepmind.com/blog/alphastar-mastering-real-time-strategy-game-starcraft-ii/, 2019.



