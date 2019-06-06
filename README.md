# BoruvkaMST
>Finding the minimal spanning tree of a weighted graph using Baruvka's algorithm 

    Objective
        -Create a minimal spanning tree consisting of Vertices and Edges
        -Each vertex has an identifier and each edge has a weight (cost)
        -Tree cannot have any cycles
        -Must traverse the tree with the MINIMUM (Least sum) of edge weights
        -Can have multiple MSTs with the same sum of weights within the graph

    Algorithm
        -Start with a forest, where each tree is a vertex (node) of the graph and has an edge
        connecting to at least one other tree (node)
        -Find least weighted neighboring tree that does not create a cycle
        -Combine current tree (node) and least cost neighbor into one tree
        -Cycle through each node until each node is connected with its least cost neighbor
        -Must consider the combined trees (nodes) as a single tree (node) from now on
        -If all nodes have been cycled through and no MST has been created,
        cycle through each newly combined tree and find least cost neighbor of the new tree
        -Repeat the previous step until all the trees (nodes) in the forest are
        connected together to create one tree (MST)
