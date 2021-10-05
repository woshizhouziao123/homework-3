BL40A2010 Introduction to IoT-Based Systems
Assignment 3, 04.10.2021
Author:Zhouziao
(1) Compute the following for a ring topology of $N\geq3$ nodes considering that the network in unweighted and the links are directed. The result will give these number as a function of $N$.

Answer:

(a) Degree of nodes: 2 regardless of N


(b) Adjacent matrix:![7f5c7c30a681775ae99dedbdcf23f73](https://user-images.githubusercontent.com/91326706/135942776-04e6aaff-94c5-40d6-a3d0-472fa45b296c.png)


(c) Diameter:N/2

(d) Clustering coefficient of the nodes:$0$ regardless of $N$.


(2) Use NetworkX to draw and analyze a ring topology with 5 nodes. Verify if the results previously obtained are valid.

![2e7a72133ffe5c255c77ca931453ac4](https://user-images.githubusercontent.com/91326706/135942876-14b150d4-71d8-438d-9f7a-6ae8c88deab0.png)
![59f890cd9167b5708f40822e5516dd8](https://user-images.githubusercontent.com/91326706/135942929-f99ec112-7c77-4095-97d6-c8a7b79c586e.png)
![image](https://user-images.githubusercontent.com/91326706/135942965-72147454-8972-44e2-a27c-3aae05069907.png)
![fa4223e8c50e10d5528c97fe1798bc0](https://user-images.githubusercontent.com/91326706/135943000-06717601-2389-43fa-865d-4c8e465ac79f.png)
![image](https://user-images.githubusercontent.com/91326706/135943073-a5b2bdc4-59ee-40bb-a2b8-53b40f15762f.png)



(3) Analyze the ring topology with size 20 ($N=20$) as a communication network (i.e. how data travel to a point to another in the network) based on the node degree, the network diamenter and the cluster coefficient.

Answer::From question 1, The ring with n = 20 is a communication network, and each node is connected to only two adjacent nodes. This means that when you need to communicate with other nodes, you need to go through more nodes (up to N / 2). Since the topology is not clustered (only connected with neighbors), the attack on links or edges is unstable.


(4) Consider the ring network from the previous question. The network performance depends on its diameter. As a designer, you can add one new node in the network (and an unlimited number of links that this node is part) . Justify your decision and evaluate how much better the network is. Generalize this finding as a function of $N$.

Hint: Follow Exercise 1 approach to generalize the finding.

Answer:Since the network is a ring, the add node must be connected to its right side and left side node so it still is a ring, an edge of the network must be broken to insert a new node,but now with $N=21$. We can generalize this by saying that to maintain the network diameter equals to N/2, the new node must join the ring, creating a complete graph of N+1 nodes
