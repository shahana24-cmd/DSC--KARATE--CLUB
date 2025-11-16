# DSC--KARATE--CLUB
- Introduction

This project investigates community detection in the Karate Club graph using recursive spectral modularity partitioning. The approach identifies meaningful community boundaries by repeatedly splitting the graph based on the leading eigenvector of the modularity matrix. After each split, we evaluate how node importance changes by computing standard network metrics. This helps reveal which nodes remain structurally central and how the evolving community structure influences the connectivity patterns in the network.

- Summary of the Tasks

This assignment involves implementing a multi-community detection workflow using spectral modularity:
1. Recursive Spectral Modularity Partitioning
The modularity matrix is computed and used to split the graph by the sign of its leading eigenvector. The process is recursively repeated on each sub-community until no further modularity gain is possible.

2. Graph Visualization After Each Split
At every stage, the graph is visualized using a fixed layout, and each identified community is assigned a unique color to clearly show how the network evolves.

3. Calculation of Node Metrics
After each split, four NetworkX metrics are computed:
degree centrality,betweenness centrality,closeness centrality,clustering coefficient.
These values capture the structural role of each node in the network.

4. Plotting Metric Evolution
The metric values are tracked across iterations and plotted to show how each node’s importance changes as more communities are formed.

- Discussion

Across the recursive splits, the major hub and bridge nodes—especially the instructor and administrator—remain central, maintaining high degree, betweenness, and closeness scores. Their consistent importance arises from their role in connecting different parts of the network and appearing on many shortest paths. Community structure strongly shapes the metrics: interior nodes show high clustering but lower betweenness, while boundary nodes experience higher betweenness and more variation as communities separate. As the graph is subdivided, central nodes continue to dominate information flow, while peripheral nodes become less influential.

- Conclusion

Through recursive spectral modularity partitioning, this project reveals the underlying community structure of the Karate Club graph and demonstrates how node roles shift with each split. Visualizations and metric tracking clearly show that key hubs remain structurally central throughout the process, while other nodes change in importance depending on their community’s composition. This combination of modularity-based partitioning and network analysis provides meaningful insight into how community boundaries influence node connectivity and centrality within social networks.
