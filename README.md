# OOP - EX3: Making a Directed Weighted Graph (in python)
<br /> 

![open_pic](https://user-images.githubusercontent.com/68643157/147391303-35a6433e-de51-49cc-abb9-091a5af02333.jpg)

**Done by Arieh Norton and Leead Jacobowitz** 
  <br />
  
  ### In this assingment, we were challenged to create a directed weighted graph OOP and to visulise it as a plot using python. 
  
  

## The main idea of the code <br />

We have two base classes that are objects, Gnode and edge.
To create a Gnode you need to give it a key and location in tuple form. The object has two size parmeters and tag. 
Size for edges in and size for edges out. 
The next stage of our code is to implement the two interfaces we have, GraphInterface and GraphAlgointerface. 
Digraph implements GraphInterface and GraphAlgo implements GraphAlgoInterface. In Digraph we used two dicts, the first is a dict of node. 
The second is a nested dict, which is represented by node id and all the edges of that node. 

## Our code structure <br />
![UML-Ex3](https://user-images.githubusercontent.com/68643157/147404015-a4f46d17-4a1b-4b51-9c4b-1971582e79a4.jpeg)



## classes <br />
1. **Gnode** - This class is our Node object, to create one it needs to get key and location, if it doesn't get location
               it will give it a random location. 
      <br />
2. **Edge** - This class is our Edge object and gets src dest and weight.<br /><br />
3. **DiGraph** -AKA "Directed weighted graph" this class implements the graph interface
            and is build of two different dicts, one for nodes and one is a nested dict for edges.<br /><br />
4. **GrapAlgo** - aka Directed weighted grap algo. This class implements the Graphalgo interface, that is where all the algorithms for the graph are.
                - Shortest path between 2 vertacies.
                - The ideal center of the graph.
                - Travelling salesman problem for a group of vertacies in the graph
                - Plot the graph 
  
## Plot
<br />

This is the plot User Interface, which will show the graph that we have created <br />
This is Graph 1 for example: 

![g1](https://user-images.githubusercontent.com/68643157/147391546-43249bb4-3304-42ef-b563-391a5d45c687.png)
  
## Algorithms<br />

- **IsConnected** - This algorithm will check if all the vertacies are connected.<br />
  We implemented this by usign DFS, and checking if all the nodes were visited.    

- **Shortest_Path** - This algorithm finds the shortest path between two Nodes and return the weight and the route it travels between them.
  We used the Dijkstra algorithm. <br /><br />
    
- **CenterPoint** - Find the Node that is the most center in the graph.<br />
  We use the Dijkstra algorithm and find the minimum distance for each Node. <br /><br />

- **Tsp** - Travelling Salesman Problem. 
  Given a list of Nodes, find the shortest way to visit all Nodes at least once. 
  In the tsp we first initialized a matrix. 
  Each index in the matrix represented the weight between two nodes.
  We than ran the 'Dijkstra' algorithem, minimizing each index to the shortrst path between the two nodes.
  We then initialized a boolean array, where each index represents a node key from the givin graph.
  The index in the boolean array is true if the node was visited and false if not.
  Since the rout is cyclic there is no importance to the starting point.
  We used the tsp_helper function. It recursivly computes the tsp for each node.
  The helper returns the lowest path by weight.
  
- **Load from json** - Given a path of a json file, load it to a GraphAlgo

- **Save to json** - Given a graph that we want to save, it will save it in a json format. 

- **Plot** - Given a graph plot it as a Gui. 

- **Get graph** - return the graph that is in the GraphAlgo

## Three graphs: 
  **G1 as seen above**
  ![g1](https://user-images.githubusercontent.com/68643157/147391546-43249bb4-3304-42ef-b563-391a5d45c687.png)
  
  **G2**
  ![G2_python](https://user-images.githubusercontent.com/68643157/147391664-5f0d00fd-3425-40c1-af24-84f00d46c4da.png)

  
  **G3**
  ![G3_python](https://user-images.githubusercontent.com/68643157/147391692-46320e0a-3682-462d-b411-39ab0064402d.png)
      

## Algorithms Results<br />
![final resutls](https://user-images.githubusercontent.com/68643157/147500595-3f6d75a1-ce99-430d-9a25-b47cad56edf7.jpeg)
<br />

## Running the programme <br />

1. Clone the project from [here](https://github.com/Arieh-code/OOP-EX3.git) . <br />
2. Open the project and go to main.py and read the remarks

The graphs that you can play with are [here:](https://github.com/Arieh-code/OOP-EX3/tree/master/src/data)

