
# Adversarial Immunization
**This repository is our Pytorch implementation of our paper:**

**[Adversarial Immunization
for Certifiable Robustness on Graphs](https://arxiv.org/abs/2007.09647)** 

By Shuchang Tao, Huawei Shen, Qi Cao, Liang Hou and Xueqi Cheng

**Published at WSDM 2021**



## Introduction

Despite achieving strong performance in semi-supervised node classification task, graph neural networks (GNNs) are vulnerable to adversarial attacks, similar to other deep learning models. Existing researches focus on developing either robust GNN models or attack detection methods against adversarial attacks on graphs. However, little research attention is paid to the potential and practice of immunization to adversarial attacks on graphs. 

In this paper, we propose and formulate the **graph adversarial immunization** problem, i.e., vaccinating an affordable fraction of node pairs, connected or unconnected, to improve the certifiable robustness of graph against any admissible adversarial attack. 



<img src="./imgs/immunization_karate.png" />

Figure shows effect of adversarial immunization on Karate club network. Colors differentiate nodes in two classes. We use two bars to represent node’s robustness before and after immunization. The node is certified as robust (red), when its robustness > 0, otherwise as non-robust (pink). Purple circle indicates the node that becomes robust through immunization. The red edges are immune edges.



## AdvImmune

We further propose an effective algorithm, called AdvImmune, which optimizes with meta-gradient in a discrete way to circumvent the computationally expensive combinatorial optimization when solving the adversarial immunization problem. 

<img src="./imgs/AdvImmune.png" />

The training and test process of AdvImmune.



## Requirements

- pytorch 
- scipy
- numpy
- numba
- cvxpy



## Usage
***Example Usage***

`python -u main.py --dataset citeseer --scenario rem `

For detailed description of all parameters, you can run

`python -u main.py --help`



## Cite

If you would like to use our code, please cite:
```
@inproceedings{tao2021advimmune,
  title={Adversarial Immunization for Certifiable Robustness on Graphs},
  author={Shuchang Tao and Huawei Shen and Qi Cao and Liang Hou and Xueqi Cheng.},
  booktitle={Proceedings of the 14th ACM International Conference on Web Search and Data Mining},
  series={WSDM'21},
  year={2021},
  pages = {698-706}
}
```
