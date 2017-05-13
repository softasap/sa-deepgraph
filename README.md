sa-deepgraph
============

[![Build Status](https://travis-ci.org/softasap/sa-deepgraph.svg?branch=master)](https://travis-ci.org/softasap/sa-deepgraph)

DeepGraph is an open source Python implementation of a new network representation introduced https://arxiv.org/abs/1604.00971. Its purpose is to facilitate data analysis by interpreting data in terms of network theory.

The basis of this software package is Pandas, a fast and flexible data analysis tool for the Python programming language. Utilizing one of its primary data structures, the DataFrame, we represent objects (i.e. the nodes of a network) by one DataFrame, and their pairwise relations (i.e. the edges of a network) by another DataFrame.

One of the main features of DeepGraph is an efficient and scalable creation of edges. Given a set of nodes in the form of a DataFrame (or an on disc HDFStore), DeepGraph’s core class provides methods to iteratively compute pairwise relations between the nodes (e.g. similarity/distance measures) using arbitrary, user-defined functions on the nodes’ features. These methods provide arguments to parallelize the computation and control memory consumption, making them suitable for very large data-sets and adjustable to whatever hardware you have at hand (from netbooks to cluster architectures).

Furthermore, once a graph is constructed, DeepGraph allows you to partition its nodes, edges or the entire graph by the graph’s properties and labels, enabling the aggregation, computation and allocation of information on and between arbitrary groups of nodes. These methods also let you express elaborate queries on the information contained in a deep graph.

DeepGraph is not meant to replace or compete with already existing Python network libraries, such as NetworkX or graph_tool, but rather to combine and extend their capabilities with the merits of Pandas. For that matter, the core class of DeepGraph provides interfacing methods to convert to common network representations and graph objects of popular Python network packages.

Deepgraph also implements a number of useful plotting methods, including drawings on geographical map projections.

It’s also possible to represent multilayer networks by deep graphs. We’re thinking of implementing an interface to a suitable package dedicated to the analysis of multilayer networks.


See package details: https://deepgraph.readthedocs.io/


Example of usage (all parameters are optional)

Simple

```YAML
  roles:
    - {
        role: "sa-deepgraph"
      }
```

Advanced:

```YAML
  roles:
    - {
        role: "sa-deepgraph"
      }
```

Copyright and license
---------------------

Code licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) or the [MIT License] (http://opensource.org/licenses/MIT).

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

Join gitter discussion channel at [Gitter](https://gitter.im/softasap)
