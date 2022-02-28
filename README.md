# Graph-Analytics

The purpose of this repository is to replicate several Graph algorithms to perform classification and make a comparison in performance. 

1. Simple MLP: 2 Fully Connected layer.
2. GCN: State-of-the-art paper "Semi-Supervised Classification with Graph Convolutional Networks" by Kipf and Welling [1](https://arxiv.org/abs/1609.02907). GCNs perform convolutions by making use of both the signal and the graph structure by taking into account the adjacency matrix. It also normalize the latter by using the so called "Re-normalization trick". The formula is: A = D^(-1/2)AD^(-1/2) with A also considering its self loops. Code based on Jackie Loong explanation [5](https://github.com/dragen1860)

3. GfNN: Evaluates performance of the study "Revisiting Graph Neural Networks: All We Have is Low-Pass Filters" by Hoang NT, et al [2](https://arxiv.org/abs/1905.09550). Validates why a Vanilla GCN is in effect a low-pass filter and explains why re-using the adjacency matrix during training is not optimal. Hence, GfNN performs feature augmentation, mixing the graph structure with the signal before training, making the model faster and accurate.

4. GAT: Graph Attention Network is one of the most accurate models for classifying graph networks [3](https://arxiv.org/abs/1710.10903). Peter Veličković, et al. adapted well-known Attention mechanismsn proven effective in areas such as image processing. This model assigns an adaptive weight according to the importance of neighbouring nodes features during the aggregation step in GCNs. It is possible to create a multi-head GAT. In simple words, it is an ensemble of GATs in each convolution.
6. Scattering GCN: Overcoming Oversmoothness in Graph Convolutional Networks. Min, et al. [4](https://arxiv.org/abs/2003.08414). took advantage of the low-pass filter a vanilla GCN produces and implemented a band-pass filter to keep as much high frequency from the signal as possible and applicates a residual neural network to normalize the frequencie of the two filters. 
