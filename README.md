# Create a catkin workspace

 $ mkdir -p ~/catkin_ws/src   # Replace `catkin_ws` with the name of your workspace
 $ cd ~/catkin_ws/
 $ catkin_make
 # Download Following  code
1.  cd ~/catkin_ws/src
2.  git clone https://github.com/NVlabs/Deep_Object_Pose.git dope
3.  git clone https://github.com/ros-perception/camera_info_manager_py
4.  git clone https://github.com/OTL/cv_camera
5.  git clone https://github.com/ros-perception/vision_opencv
6.  git clone https://github.com/ros-drivers/usb_cam
# Install python dependencies

1. cd ~/catkin_ws/src/dope
2. pip install -r requirements.txt
# Install ROS dependencies
```shell
cd ~/catkin_ws
rosdep install --from-paths src -i --rosdistro melodic
sudo apt-get install ros-melodic-rosbash ros-melodic-ros-comm
```

# Install opencv 3.2
this version required for python 2
download source code from https://github.com/opencv/opencv/archive/3.2.0.zip
unzip code and move into unzip new folder 
create build folder and run following commands
1. cmake -DCMAKE_BUILD_TYPE=RELEASE -DCMAKE_INSTALL_PREFIX=/usr/local -DENABLE_PRECOMPILED_HEADERS=OFF -DWITH_FFMPEG=OFF ..

2. make -j4
3. sudo make install
