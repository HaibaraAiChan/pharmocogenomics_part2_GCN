# pharmocogenomics_part2_GCN  
#### GCN+VAE (Graph Convolutional Network & AutoEncoder)   
![steps](images/steps.png)
#### Steps:  

    1. Data preprocess:
       generate sub graph for each target protein
        i) order all neighbors by distance through shortest path algorithm(igraph env python3.5 or 3.6)
        ii)get fixed bumber K neighbors (K needs adjustment by experiment)(env python3.7 igraph can plot())
    2. Preprocess all sub graph to matrix format (A,X,…)
    3. Each sub-graph as an instance, feeding to GCN Auto-encoder network
    4. Collect target protein node latent vector from Z matrix
