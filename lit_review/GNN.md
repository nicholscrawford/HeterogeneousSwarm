#Swarm Literature with GNNs Review
---
**Research Questions**

1. LSTM Planning for GNNs - Investigate accounting for path dependence using lstm gnn predictor. This could excel at things where swarms have to complete sequnced tasks? I.E. A set of robots has to push a button in a maze in order to get to/map another section. Having all robots swarm to the button is not as optimal as leaving most robots by the door, and having one robot go to the button. This is a very different type of co-ordination task than formation control; the policy for each robot has to be co-ordinated, but very dissimilar. I'm not sure how an LSTM fits in, but the control system would need to be able to do coalition formation, and long term planning. My guess is that decenteralization is bad for long term planning, and hierarchical systems could be better?
2. Object-Actor GNN for multi-robot-heterogenous manipulation. Model objects and actors as nodes in a GNN, with action primitives for actors, and none for objects. Heterogeneus in the sense of differeing robot specializations like how in construction environments specialized robots could be very useful, and planning would need to account for that. Most GNN MRS use GNNs for communication improvements.
3. Layered GNNs for Heirarchical Robot Control. Have more powerful robots hold a GNN for controlling the smaller robots, and use a GNN to synchronize the larger robots facing limited communication. This seems like a pretty straightforeward extension from some of these papers, and I'm not sure it's academically interesting, though distilling it to the core ideas could be useful. 
---
**Summary of My Thoughts**

---
*Included Papers:*

1. [Learning Decentralized Controllers for Robot Swarms with Graph Neural Networks](http://proceedings.mlr.press/v100/tolstaya20a/tolstaya20a.pdf)
2. [Graph Neural Networks for Decentralized Multi-Robot Submodular Action Selection](https://arxiv.org/pdf/2105.08601.pdf)
3. [Multi-Robot Coverage and Exploration using Spatial Graph Neural Networks](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9636675)
4. [Graph Policy Gradients for Large Scale Robot Control](http://proceedings.mlr.press/v100/khan20a/khan20a.pdf) (Formation Control)
5. [Neurosymbolic Transformers for Multi-Agent Communication](https://proceedings.neurips.cc/paper/2020/file/9d740bd0f36aaa312c8d504e28c42163-Paper.pdf)
6. [Graph Neural Networks for Decentralized Multi-Robot Path Planning](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9341668)
7. [Message-Aware Graph Attention Networks for Large-Scale Multi-Robot Path Planning](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9424371)
8. [Neural-Swarm2: Planning and Control of Heterogeneous Multirotor Swarms Using Learned Interactions](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9508420)
9. [Learning scheduling policies for multi-robot coordination with graph attention networks](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9116987)
10. [Decentralization of multiagent policies by learning what to communicate](https://arxiv.org/pdf/1901.08490.pdf) (Perimeter Defence)

---
*Notes on Paper 1:*

**Learning Decentralized Controllers for Robot Swarms with Graph Neural Networks**

Problem: Finding distributed controllers for robots that can't constantly communicate.

Approach: Use ground truth of a global controller to train local controllers.

How can this be extended to heterogenous systems?

---
*Notes on Paper 2:*

**Graph Neural Networks for Decentralized Multi-Robot Submodular Action Selection**

Decentralized submodular maximization is a decenteralized version of robots selecting motion primitives to maximize team objectives with only local communication. 

This is useful for large scale co-ordination in 'looking' tasks, and manipulation isn't really mentioned? This could be extended with action primitives that change the environment?

---
*Notes on Paper 3:*

**Multi-Robot Coverage and Exploration using Spatial Graph Neural Networks**

Graph represets locations and robots as nodes in a graph, and edges as literal paths that can be traveled by the robots. (How does the gnn account for changing edges?)

*A mean aggregation operation helps stabilize training of GNNs with larger receptive fields.*

This is very specific to exploration/coverage, and seems like it would be very intuitive to generalize to heterogeneous systems. Maybe interesting questions could involve interactions between different spatial graphs, as ground/air robots would have different spatial graphs, and there would have to be a co-ordination effort between the robots. Lots of the other methods for communication could be useful. They note this flaw at the end:

*One possible solution could be the evaluation of the GNN on the contents of a robot’s local buffer containing the estimated state of the system, and allowing intermittent communication among robots to update each other...*

---
*Notes on Paper 4:*

**Graph Policy Gradients for Large Scale Robot Control**

Uses Graph Convolutional Network (GCN, How is this different from a GNN? Presumably the output is not a graph, but I'll do more reading) to learn local policies for an overarching goal. Communication is then learned between one-shot local robots. In this case, the overarching goal is formation control. 

This approach seems to make a lot of sense for formation control, but what about long term planning? 

---
*Notes on Paper 8:*

**Neural-Swarm2: Planning and Control of Heterogeneous Multirotor Swarms Using Learned Interactions**

- This is specific to multi-rotor dynamics, using a physics model + deep nets (MLP?) (Trained in a permutation invariant manner.)

So this paper helps multi-rotors fly specifically in close proximity, overcoming the specific challenge of complex aerodynamic forces.

---