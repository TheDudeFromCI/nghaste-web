
## NG-HASTE, what is it?

NG-HASTE is a program which can be used to generate code at runtime. More specifically, algorithms which solve problems.

The program is designed to take in a stream of unit tests, then search for a solution which meets passes all tests. These tests can be generated at runtime and passed to NGHASTE, which can run as a background service. As flaws or bugs are discovered in the generated algorithm, new unit tests can be generated and further tweak the algorithm to be more stable. Once this algorithm is generated, it can be compiled into regular program code dynamically and reused continuously. Even across shutdowns and restarts! You can even keep searching for solutions after one is discovered to find more optimized solutions, possibly solving the problem faster or using less resources.

### What was the inspiration behind this project?

This project was inspired by the need to solve problems which arise at runtime, without needing to write a solution for each problem. In the field of artifictial intelligence, there are problems which neural networks are extremely good at solving, such as image recognition or vector manipulation. While other problems, such as problem solving and strategizing are much more difficult to achieve. This project aims to work alongside other machine learning algorithms to target areas which involve logical processing and planning ahead. While a neural network might excell in determining the velocities and forces to apply to arm joints and push a button, this project aims to target the act of realizing the button needs to be pressed to open a door and continue.

As the program generates code which is permanitly reusable, standard training phases and optimization phases still apply. Instead of this program being used to solve a Rubiks Cube, it could instead be used to write an algorithm to solve all Rubiks Cubes. If a solution fails to solve the cube in a specific instance, a test case can be generated and passed back to ensure it doesn't happen again.

### How does it work?

At it's core, NGHASTE works as a search tree which attempts to sift through all possible algorithms that could be written up to a given complexity value. The tree is structured in such as way so that if one node fails a test, then all child nodes are also garenteed to fail that test. Through this method, the search space can be drastically narrowed down to only consider relivant combinations. On top of this, a set of heuristics can be applied to prioritize searching nodes which are more likely to contain a solution within the remaining search space.
