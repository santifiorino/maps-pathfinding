# Comparing Algorithms: A* vs Dijkstra on the City's Map

This repository contains the code used in the YouTube video titled __"Comparing Algorithms: A* vs Dijkstra, on the city's map"__. The video provides a visual comparison between the A* and Dijkstra algorithms in the context of finding paths on a city map represented as a graph.

[**Watch it here!**](https://youtu.be/oMgfGkFSgI0) (it's in spanish).

![paragit](https://github.com/santifiorino/maps_pathfinding/assets/94584235/6741cab4-477d-4241-9d0f-8c8b9465b5b6)

## Introduction
The experiments conducted in the video can be easily reproduced by adding some image-saving logic to this notebook, ensuring that it saves each intermediate frame rather than just the final one. I opted against incorporating a comprehensive printing mechanism in the notebook to avoid unnecessary complexity and maintain clarity. However, if desired, implementing this feature is straightforward. The experiments conducted in the video are as follows:

### Experiment 1: Pathfinding Efficiency
The first experiment focuses on comparing the efficiency of A* and Dijkstra algorithms. We measure the number of iterations each algorithm takes to find a path, and then analyze the distance, speed, and time of the reconstructed path. The visualization in the video illustrates the expansion of the algorithms from the origin to the destination, highlighting the roads considered during the process.

The conclusion drawn from this experiment is that although Dijkstra may take more iterations and yield a slightly longer path, it finds the absolute fastest path. On the other hand, A* is faster to execute but may not always produce the optimal path.

### Experiment 2: Road Usage Analysis
In the second experiment, we conduct a deeper analysis of road usage by running an algorithm multiple times from random starting points. Each time the algorithm is run, we increment a counter for each road of the found path. Then we can plot a heatmap to see which roads were used the most by each algorithm.

The heatmap analysis reveals interesting observations. Dijkstra algorithm exhibits a tendency to prioritize highways and major roads due to their potential for faster routes to the destination. Conversely, A* algorithm might choose unconventional paths, prioritizing efficiency in reaching the destination during its execution. As a result, it may disregard deviations towards highways or main roads, despite their potential for faster travel, as they could lengthen the path. 

## How to use
This code relies on the osmnx library. Please refer to [the osmnx documentation](https://osmnx.readthedocs.io/en/stable/) for installation instructions and detailed usage guidelines. Once installed, you can utilize all the functionalities provided in the notebook to reproduce the experiments conducted in the video and explore further analyses.
