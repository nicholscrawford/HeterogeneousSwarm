#Heterogeneous Swarm Literature Review
---
*Included Papers:*

1. [Cooperative Heterogeneous Multi-Robot Systems: A Survey](https://dl.acm.org/doi/pdf/10.1145/3303848)
1. [Cooperative Self-Organization in a Heterogeneous Swarm
Robotic System](https://dl.acm.org/doi/pdf/10.1145/1830483.1830501)

---
*Notes on Paper 1:*

**Cooperative Heterogeneous Multi-Robot Systems: A Survey**

- Focuses on automating complex tasks, and lacks in credit assignment, consensus, containment control, and communication protocols. Though ref 30, 56 have more info.
- In intro suggest applications such as "health care, transportation systems, emergency response systems, household chores, and elderly
care, among others".
- Few "end-to-end frameworks have been presented", notes **swarmanoids** as one that tackles task automation. *"Natural language ontology and dictionaries could help automate complex task decomposition and big data advancements could be leveraged to improve perception and, consequently,
decision making."*
- Other reviews have covered aspects of tasks like "foraging,
formation control, cooperative object manipulation and displacement, path planning, and soccer". In manipulation, unknown objects make robots struggle, what about swarms for object scanning/locating/recognition?
- Writes of the multi-robot system workflow, and notably *"To the best of our knowledge, there are no implementations of fully automated
systems, i.e., a complex task was given to the MRS, and the system autonomously decomposed this
complex task to sub-tasks, formed coalitions, and assigned and executed these sub-tasks."*
- Illustrates two MRS tasks in disaster response search robots with different specializations can search debris, larger robots can retrive, and transport robots can communicate with transportatio information, and traffic lights (robots?) to generate fastest routes to health care. In smart cities, elderly care could be enhanced with robotic monitoring/care in communication with health care robotics and transportation, and several independent sections of this system include previous work.
- Lists various MRS and their tasks and levels of autonomy. Many done in simulation only.
- Details approaches to coalition formation and task allocation, MAS planning and control, perception.
- Heterogeneous systems can increase the scope of solvable tasks, and lead to better performance with simpler agents through parallelism and robustness. More complex design.

**Struggles and Direction Notes**

*Big Data* - ML is beneficial, but limited on less capbable robotics, and cloud accessabillity may be limited in some environments. *"Future research should investigate methods to incorporate big data models into computationally constrained and communication restricted MRS applications to improve task planning and execution"*

*IoT* - Robot systems could be enhanced by IoT, sensor fusion and distributed sensing could aid perception for robotics.

*Task Complexity* - Decision making algorithms sturggle to recognize and decompose complex tasks autonomously. Suggests incorperating option for robots to contact humans. RL incorperating human operators to improve accuracy.

*Autonomous ML* - Could be incorperated to general angents that handle dynamic environments. Consider applying or extending algorithms developed for mobile devices to MRS. 

*Scalability and Heterogeneity Tradeoff* - Many robots acting on a system increases uncertainty in a system, and planning and control algorithms struggle with scalability and heterogeneity in very dynamic environments. Efficient planning balancing scalabillity and heterogeneity will help for applications like smart cities. Potentially hierarchical approaches where local interactions are dense, and global interactions are sparse could improve scalability with heterogeneity.

*Coalition Formation and Task Allocation* - *"Simultaneous coalition formation and task allocation could lead to more optimal mappings and
should be investigated further, since only a few works have considered this approach but obtained
promising results."*

*Human-in-the-Loop* - Human in the loop systems/architectures have potential benefits, and potential drawbacks, so figuring out if including humans in a sytem is beneficial or detrimental could be useful.

*Transfer Learning* - *"Transfer learning has been applied to MAS [151, 212] and MRS [50] but has yet to be tested in end-to-end systems deployed in the real world on complex tasks. Furthermore, transfer learning for RL has been mainly tested on benchmark problems and gaming environments but not in real-world environments.*"

*Unified Framework* - Deployments are limited by the lack of interaction between work on various sections of MRS. Work on sections of MRS task completion should be viewed as parts of a whole, and it should be possible to interact between sections of the problem. E2E sim and real world experiments should be used to improve and validate formulated models.

*Other* - Communication and connectivity constraints complicate problems. Evaluation standards for MRS are also very underdeveloped.






