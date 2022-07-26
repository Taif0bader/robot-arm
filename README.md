# installing robot arm

### Follow the following steps
#### 1: open Oracle VM VirtualBox
#### 2: open ubuntu 
#### 3: open termainal then copy and paste the following steps:

#### 1.Install catkin:
   ```
       sudo apt-get install ros-noetic-catkin
   ```
#### 2.Make workspace:
   ```
       -     mkdir -p ~/catkin_ws/src
       -     cd ~/catkin_ws/
       -     catkin_make
       -     cd ~/catkin_ws/src
   ```
#### 3.To can acsses packages of robot:
```
       -     git clone https://github.com/smart-methods/arduino_robot_arm.git
       -     cd ~/catkin_ws
       -     rosdep install --from-paths src --ignore-src -r -y
       -     sudo apt-get install ros-kinetic-moveit
       -     sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui
       -     sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher
       -     sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control
       -     sudo nano ~/.bashrc
       -     at the end of the (bashrc) file add the follwing line
             (source /home/SystemName/catkin_ws/devel/setup.bash)
        then 
             ctrl + o
       then
            ctrl + x

      -     source ~/.bashrc

      -     roslaunch robot_arm_pkg check_motors.launch
 ```
#### Now, Rviz program will open on Ros to work on robot arm
![image](https://user-images.githubusercontent.com/106008150/181117549-6bc434b6-192d-47d4-a3e4-3b64291af4f2.png)

