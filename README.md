# Robot-arm
## First task
- First step: install Ros melodic system:<br/>

 ```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

sudo apt-get update

sudo apt-get install ros-kinetic-desktop-full

apt-cache search ros-kinetic

echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

sudo apt install python-rosdep

sudo rosdep init

rosdep update
```

- Second step: install the catkin for the work space:<br/>
<br/>`sudo apt-get install ros-melodic-catkin`
- Third step: Creat the work space:

```
mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make
```
- Fourth step: Go to the source folder:<br/>
<br/>`cd ~/catkin_ws/src`
- From the "source" folder, we access the packages for robot arm:<br/>
<br/>`git clone https://github.com/smart-methods/arduino_robot_arm.git`
- Fifth step: We go back to the catkin folder to install some of the commands for the rose:<br/>
<br/>`cd ~/catkin_ws`
- Sixth step: write commands:<br/>
```
rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-kinetic-moveit

sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control
```
- After adding all the commands, we go to the file:<br/>
 <br/>`sudo nano ~/.bashrc`
- In the end we add:<br/>
 <br/>`source /home/maryam/catkin_ws/devel/setup.bash`
 <br/> and then ctrl + o
inter and then ctrl+x 
- updating the "source" file:<br/>
<br/>`source ~/.bashrc`
-  Final step: We run the emulator through the command:<br/>
<br/>`roslaunch robot_arm_pkg check_motors.launch`
- ![robot-arm](https://user-images.githubusercontent.com/85634146/129487558-2b859587-1245-4c33-8943-12af839c1fcd.png)
-![arm-robot](https://user-images.githubusercontent.com/85634146/129487680-5833dfea-6628-4a7d-980d-ea1353121924.png)















