# Landmark_Detection_Tracking_SLAM
In this project, we'll be localizing a robot in a 2D grid world. The basis for simultaneous localization and mapping (SLAM) is to gather information from a robot's sensors
and motions over time, and then use information about measurements and motion to re-construct a map of the world.

## Installation
Clone the repository and download the Jupyter Notebook through **https://jupyter.org/**. It is highly recommended to open and run this project through Jupyter Notebook
```
git clone https://github.com/zilinli0130/Landmark_Detection_Tracking_SLAM

```
 
## Usage

1. The `1. Robot Moving and Sensing.ipynb` file loads in our resources and defines the robot class. You can see that this class initializes the robot's position and 
adds measures of uncertainty for motion.

2. The `2. Omega and Xi, Constraints` contains an example of Omega matrix and Xi vector. To implement Graph SLAM, a matrix and a vector (omega and xi, respectively) are introduced. The matrix is square and labelled with all the robot poses (xi) and all the landmarks (Li). Every time you make an observation, for example, as you move between two poses by some distance dx and can relate those two positions.

3. The detail of implementation of Graph SLAM is in `3. Landmark Detection and Tracking.ipynb` file. SLAM gives us a way to both localize a robot and build up a map of its environment as a robot moves and senses in real-time. This is an active area of research in the fields of robotics and autonomous systems. Since this localization and map-building relies on the visual sensing of landmarks, this is a computer vision problem.
In a real SLAM problem, you may be given a map that contains information about landmark locations, and in this example, we will make our own data using the `make_data` function, which generates a world grid with landmarks in it and then generates data by placing a robot in that world and moving and sensing over some numer of time steps. The `make_data` function relies on a correct implementation of robot move/sense functions, 
which, at this point, should be complete and in the `robot_class.py` file. The data is collected as an instantiated robot moves and senses in a world. Your SLAM function will take in this data as input.
