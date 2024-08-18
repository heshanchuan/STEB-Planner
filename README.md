# STEB-Planner
STEB-Planner is a spatio-temporal elastic bands-based trajectory planner for autonomous vehicles using semantic graph  optimization

> The paper of this method is submitted to the IEEE Robotics and Automation Letters (RA-L)



## Performance Display
### Static obstacle avoidance

<div style="display: flex; justify-content: center;">
    <div style="text-align: center; margin-right: 20px;">
        <img src="docs/img/static_obstacle_avoidance_1.png" width="250"/>
        <p>Scenario 1: Static Obstacle Avoidance</p>
    </div>
    <div style="text-align: center;">
        <img src="docs/img/static_obstacle_avoidance_2.png" width="250"/>
        <p>Scenario 2: Static Obstacle Avoidance</p>
    </div>
</div>

<p align="center">
    <img src="docs/img/static_obstacle_avoidance_2.png" width="300"/> <img src="docs/img/static_obstacle_avoidance_2.png" width="300"/>
    
</p>



### Dynamic traffic Interaction
<div style="text-align: center; margin-right: 0px;">
     <img src="docs/gif/overtaking.gif" width="520"/>
    <p style="text-align: center;">Scenario 3: Overtaking a slow car ahead</p>
</div>

Some other scenes (the gif will be uploaded later)
<div style="display: flex; justify-content: center;">
    <div style="text-align: center; margin-right: 20px;">
        <img src="docs/img/Up_left_turn.png" width="250"/>
        <p>Scenario 4: Unprotected Left Turn (Scenario 3)</p>
    </div>
    <div style="text-align: center;">
        <img src="docs/img/merge.png" width="250"/>
        <p>Scenario 5: Merge Into the Traffic (Scenario 4)</p>
    </div>
</div>





## Installation

### Prerequisites

Our software is developed and tested in Ubuntu20.04 with ROS2 galactic. Follow [this link](https://docs.ros.org/en/galactic/Installation.html) to install galactic.

### Simulation environment

We use **Carla-0.9.15** as the simulator (download via this [link](https://github.com/carla-simulator/carla/releases/tag/0.9.15)).

To use the Carla PythonAPI, you need to export the path or install it

```bash
export CARLA_ROOT=<path-to-carla>
export PYTHONPATH=$PYTHONPATH:/carla_directory/PythonAPI/carla/dist/carla-0.9.15-py3.7-linux-x86_64.egg
```



## Installation
### Required Library
- Eigen3
- PCL
- OpenCV

### Download & Compile
```bash
# Download
cd ~/your_workspace/src
git clone https://github.com/heshanchuan/STEB-Planner.git

# Compile
cd ../
source /opt/ros/galactic/setup.bash
colcon build  --symlink-install  --cmake-args -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DCMAKE_BUILD_TYPE=Release

```


## Usage example

```bash
source install/setup.bash
ros2 launch steb_planner steb_planner_test.launch.xml
```



## Release History
Notes: 1.0.0 will be our first elegant version.
* 0.1
    * CHANGE: First upload readme and some multimedia files


## Contributing

1. Fork it (<https://github.com/heshanchuan/STEB-Planner/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

## License

The source code is released under [MIT](https://opensource.org/licenses/MIT) license.

## Disclaimer

This is research code, it is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of merchantability or fitness for a particular purpose.