---
title: "Scalable Estimation of Signed Exponential Random Graph Models with Local Dependence (WiP)"
authors:
  - Marc Schalberger
  - Cornelius Fritz
date: "2024-06-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: |
  Network analysis methods traditionally focus on binary edges, where relationships are either positive (e.g., alliances, friendships) or negative (e.g., rivalries, conflicts). However, in many real-life scenarios, these two types of relationships can occur simultaneously and are, hence, better characterized by signed interactions of cooperation, neutrality, or conflict.

  Concurrently, the advent of social media has brought increased attention to this area, as the inclusion of negative ties has proven to enrich analysis in polarized discussions. Nowadays, most networks are observed digitally, generating vast amounts of data.

  Signed network extensions exist for Stochastic Block Models (SBM) and Exponential Family Random Graph Models (ERGM), but they have inherent shortcomings. While the SBM can represent cohesive subgroups among the nodes, it implies conditional independence for the formation of ties between nodes, which is unrealistic for networks exhibiting more dependence among edges. On the other hand, ERGMs offer more flexibility in modeling a variety of network properties. However, the assumption of global dependence (i.e., each edge may depend on every other edge) makes them infeasible and unrealistic for large networks. Additionally, the estimation process, which is often based on Markov Chain Monte Carlo methods, often fails due to the complexity and size of the data, as larger networks can lead to degenerate models with poor sampling properties and longer mixing times.

  We fill the resulting methodological gap by combining the strengths of both models while simultaneously addressing their respective weaknesses, introducing local dependence based on non-overlapping neighborhoods. Our model assumes that each node is only aware of the activities within its neighborhood. Consequently, the formation of within-neighborhood edges can be characterized by a more complex ERGM, while between-neighborhood edges are not affected by endogenous effects (i.e., internal and structural influences within a network) that rely on knowledge of neighboring areas. For example, in a social network, individuals may form friendships within their immediate circle without being influenced by the entire network.
  To enable large-scale estimation of our novel model extension, we rely on a two-step estimation approach. In the first step, the network is decomposed into sub-networks by approximating the likelihood of the model with an SBM for signed networks. This step is carried out with the help of a variational approximation and computationally fast MM updates. In the second step, the parameters are estimated given the previously estimated block structure with known methods for ERGMs. Thereby, we enable the estimation of signed ERGMs under local dependencies for large signed networks encompassing thousands of nodes.
  
  To demonstrate the computational advantage of this method, we apply it to both synthetic and real data. We consider a signed Wikipedia network with over 2,000 nodes, where Wikipedia editors undo (negative) or redo (positive) the contributions of other editors. This dataset is particularly suitable for a model that assumes local dependency, as contributors are likely to possess knowledge limited to their focus areas, and through our analysis, we successfully identified these focus areas.
---
