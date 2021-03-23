#  A collection of SSL pretext tasks used in GNNs
Categorization and summarization of the state-of-the-art Self-supervised Learning (SSL) on Graph Neural Networks (GNNs).


# Contents
- __[Categorization](#Categorization)__
- __[Summarization](#Summarization)__
  - __[Node-level](#Node-level)__
    - [Node-structure-based](#Node-structure-based)
    - [Node-feature-based](#Node-feature-based)
    - [Node-hybrid](#Node-hybrid)
  - __[Graph-level](#Graph-level)__
    - [Graph-structure-based](#Graph-structure-based)
    - [Graph-feature-based](#Graph-feature-based)
    - [Graph-hybrid](#Graph-hybrid)
  - [Node-graph-level](#Node-graph-level)
- __[Application](#Application)__
- __[Reference](#Reference)__


# Categorization
Pretext tasks are constructed by leveraging different types of supervision information coming from different components of graphs. Based on the components that generate the supervision information, pretext tasks that are prevalent in the literature are categorized into node-level, graph-level and node-graph level. In completing node-level and graph-level pretext tasks, three types of information can be leveraged: graph structure, node features, or hybrid, where the latter combines the information from node features, graph structure, and even information from the known training labels. We summarize the categorization of pretext tasks as a tree where each leaf node represents a specific type of pretext tasks in the following figure while also including the corresponding [**references**](ssl_category_tree.pdf).
![category_tree](images/ssl_category_tree.png)

# Summarization
## Node-level
For node-level pretext tasks, methods have been developed to use easily-accessible data to generate pseudo labels for each node or relationships for each pair of nodes. In this way, the GNNs are then trained to be predictive of the %generated 
pseudo labels or to keep the equivalence between the node embeddings and the original node relationships.

#### Node-structure-based
Different nodes have different structure properties in graph topology, which can be measured by the node degree, centrality, node partition, etc. Thus, for structure-based pretext tasks at the node-level, we expect to align node embeddings extracted from the GNNs with their structure properties, in an attempt to ensure this information is preserved while GNNs learn the node embeddings.

#### Node-feature-based
Node features are another important information that can be leveraged to provide extra supervision.

#### Node-hybrid
Instead of employing only the topology or only the feature information as the extra supervision, some pretext tasks combine them together as a hybrid supervision, or even utilize information from the known training labels.

## Graph-level
After having just presented the node-level SSL pretext tasks, in this section we focus on the graph-level SSL pretext tasks where we desire the node embeddings coming from the GNNs to encode information of graph-level properties.

#### Graph-structure-based

#### Graph-feature-based
Typically, graphs does not come with any feature information and here the graph-level features refer to the graph embeddings obtained after applying a pooling layer on all node embeddings from GNNs.

#### Graph-hybrid



### Node-graph-level
All the above pretext tasks are designed based on either the node or the graph level supervision. However, there is another final line of research combining these two sources of supervision to design pretext tasks, which we summarize in this section.

## Application

## Reference

* [COAD: Contrastive Pre-training with Adversarial Fine-tuning for Zero-shot Expert Linking](https://arxiv.org/pdf/2012.11336.pdf) (Arxiv 2020) [[**Summary**]]().
* [Distance-wise Graph Contrastive Learning](https://arxiv.org/pdf/2012.07437.pdf) (Arxiv 2020) [[**Summary**]]().
* [Pre-Training Graph Neural Networks for Cold-Start Users and Items Representation](https://arxiv.org/pdf/2012.07064.pdf) (WSDM 2021) [[**Summary**]]() [[**Code**]](https://github.com/jerryhao66/Pretrain-Recsys).
* [Deep Graph Contrastive Representation Learning](https://arxiv.org/pdf/2006.04131.pdf) (Arxiv 2020) [[**Summary**]]() [[**Code**]](https://github.com/CRIPAC-DIG/GRACE).
* [Graph Contrastive Learning with Adaptive Augmentation](https://arxiv.org/pdf/2010.14945.pdf) (WWW 2021) [[**Summary**]]()
* [Self-supervised Training of Graph Convolutional Networks](https://arxiv.org/pdf/2006.02380.pdf) (Arxiv 2020) [[**Summary**]]()
* [Deep Graph Informax](https://arxiv.org/pdf/1809.10341.pdf) (ICLR 2019) [[**Summary**]]() [[**Code**]](https://github.com/PetarV-/DGI).
* [SLAPS: Self-Supervision Improves Structure Learning for Graph Neural Networks](https://openreview.net/pdf?id=a5KvtsZ14ev) (Openreview 2020) [[**Summary**]]().
* [Self-supervised Graph-level Representation Learning with Local and Global Structure](https://openreview.net/pdf?id=DAaaaqPv9-q) (Openreview 2020) [[**Summary**]]().
* [Contrastive Multi-View Representation Learning on Graphs](https://arxiv.org/pdf/2006.05582.pdf) (ICML 2020) [[**Summary**]]() [[**Code**]](https://github.com/kavehhassani/mvgrl).
* [Self-supervised Learning on Graphs: Deep Insights and New Direction](https://arxiv.org/pdf/2006.10141.pdf) (Arxiv 2020) [[**Summary**]]() [[**Code**]](https://github.com/ChandlerBang/SelfTask-GNN).
* [When Does Self-Supervision Help Graph Convolutional Networks?](https://arxiv.org/pdf/2006.09136.pdf) (ICML 2020) [[**Summary**]]() [[**Code**]](https://github.com/Shen-Lab/SS-GCNs).
* [Graph-Based Neural Network Models with Multiple Self-Supervised Auxiliary Tasks](https://openreview.net/pdf?id=hnJSgY7p33a) (Openreview 2020) [[**Summary**]]().
* [Self-Supervised Graph Representation Learning via Global Context Prediction](https://arxiv.org/pdf/2003.01604.pdf) (Openreview 2020) [[**Summary**]]().
* [Multi-Stage Self-Supervised Learning for Graph Convolutional Networks on Graphs with Few Labels](https://arxiv.org/pdf/1902.11038.pdf) (AAAI 2020) [[**Summary**]]().
* [Strategies for Pre-training Graph Neural Networks](https://arxiv.org/pdf/1905.12265.pdf) (ICLR 2020) [[**Summary**]]() [[**Code**]](https://github.com/snap-stanford/pretrain-gnns/).
* [How to Find Your Friendly Neighborhood: Graph Attention Design with Self-Supervision](https://openreview.net/pdf?id=Wi5KUNlqWty) (ICLR 2021) [[**Summary**]]().
* [Pre-Training Graph Neural Networks for Generic Structural Feature Extraction](https://arxiv.org/pdf/1905.13728.pdf) (ICLR 2019 workshop) [[**Summary**]]().
* [ Can Graph Neural Networks Go "Online"? An Analysis of Pretraining and Inference](https://arxiv.org/pdf/1905.06018.pdf) (ICLR 2019 workshop) [[**Summary**]]().
* [ Motif-Driven Contrastive Learning of Graph Representations](https://arxiv.org/pdf/2012.12533.pdf) (Openreview 2020) [[**Summary**]]().
* [ GCC: Graph Contrastive Coding for Graph Neural Network Pre-Training](https://arxiv.org/pdf/2006.09963.pdf) (KDD 2020) [[**Summary**]]() [[**Code**]](https://github.com/THUDM/GCC).
* [ GPT-GNN: Generative Pre-Training of Graph Neural Networks](https://arxiv.org/pdf/2006.15437.pdf) (KDD 2020) [[**Summary**]]() [[**Code**]](https://github.com/acbull/GPT-GNN).
* [ TopoTER: Unsupervised Learning of Topology Transformation Equivariant Representations](https://openreview.net/pdf?id=9az9VKjOx00) (Openreview 2020) [[**Summary**]]().
* [ Graph-based, Self-Supervised Program Repair from Diagnostic Feedback](https://arxiv.org/pdf/2005.10636.pdf) (ICML 2020) [[**Summary**]]().
