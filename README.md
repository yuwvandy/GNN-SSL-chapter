#  A collection of SSL pretext tasks used in GNNs
Categorization and summarization of the state-of-the-art Self-supervised Learning (SSL) on Graph Neural Networks (GNNs).

For more details, please refer to **our book chapter (link coming soon)**. If you find this useful and use it in your research, please temporarily cite our work as follows:
![heatmap_citeseer](https://user-images.githubusercontent.com/53798810/131776213-bab0ebb8-f603-491b-9256-abbd2c92c99b.png)

    @inproceedings{wang2021gnnssl,
     author = {Wang, Yu and Jin, Wei and Derr, Tyler},
     title = {Graph Neural Networks: Self-supervised Learning},
     year = {2021}
    }



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
  - __[Node-graph-level](#Node-graph-level)__
- __[Application](#Application)__
- __[Reference](#Reference)__


# Categorization
Pretext tasks are constructed by leveraging different types of supervision information coming from different components of graphs. Based on the components that generate the supervision information, pretext tasks that are prevalent in the literature are categorized into node-level, graph-level and node-graph level. In completing node-level and graph-level pretext tasks, three types of information can be leveraged: graph structure, node features, or hybrid, where the latter combines the information from node features, graph structure, and even information from the known training labels. We summarize the categorization of pretext tasks as a tree where each leaf node represents a specific type of pretext tasks in the following figure while also including the corresponding [**references**](ssl_category_tree.pdf).
![category_tree](images/ssl_category_tree.png)

## Acknowledge
For an up-to-date list of SSL GNN papers, please refer to [**awesome-self-supervised-gnn**](https://github.com/ChandlerBang/awesome-self-supervised-gnn).
