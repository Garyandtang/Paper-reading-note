[toc]

# Robotics others

Expect for robotic perception, planning and control, robotics also has other research topics, like system integration, modeling and various applications.

## Dimensionality Reduction in Controlling Articulated Snake Robot for Endoscopy Under Dynamic Active Constraints
[PDF](https://ieeexplore.ieee.org/document/6381527)    [code by me]()                                                 By Ka-Wai Kwok, Kuen Hung Tsoi, Valentina    Vitiello, James Clark, Gary C. T. Chow, Wayne Luk, Guang-Zhong Yang

This paper presents a real-time control framework for a snake robot with hyper-kinematic redundancy under dynamic active constraints for minimally invasive surgery. The key contributions here are the modeling and a proximity query formulation to compute the deviation of the robot motion.

* The snake robot is formulated as joint-link structure, then the transformation form start vertex to each link can be calculated with forward kinematics.
* The constraint pathway is formulated as a series of contours with different size (here they formulated the contours as circle). The proximity query is used to identify whether the snake robot deviate the constraints or not (By calculating the distance between the joints to contours).
* Authors of this paper also provided a detailed (*Question: I am not pretty sure good or not?*) motion modeling and control framework for snake robot.
* I did not read in detail on modeling and control and Visual-Motor and Haptic Interaction Under Dynamic Active Constraints.
* If some need to learn more about snake robot, referring to the works in [Biorobotics Lab at CMU](https://www.ri.cmu.edu/robotics-groups/biorobotics/) may be a good chooses, as they really built a physical snake robot.