# Graph-Analytics

The purpose of this repository is to replicate several Graph algorithms to perform classification and make a comparison in performance. 

1. Simple MLP: 2 Fully Connected layer.
2. GCN: State-of-the-art paper "Semi-Supervised Classification with Graph Convolutional Networks" by Kipf and Welling [1](https://arxiv.org/abs/1609.02907)
3. GfNN: Evaluates performance of the study "Revisiting Graph Neural Networks: All We Have is Low-Pass Filters" by Hoang NT, et al [2](https://arxiv.org/abs/1905.09550)
4. GAT: Graph Attention Network is one of the most accurate models for classifying graph networks. Peter Veličković, et al. [3](https://arxiv.org/abs/1710.10903)
5. Scattering GCN: Overcoming Oversmoothness in Graph Convolutional Networks. Min, et al. took advantage of the low-pass filter a vanilla GCN produces and implemented a band-pass filter to keep as much high frequency from the signal as possible and applicates a residual neural network to normalize the frequencie of the two filters. [4](https://arxiv.org/abs/2003.08414)
