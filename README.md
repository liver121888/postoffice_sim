# postoffice_sim
ROS, pedsim, gazebo, navigation, delivery.

## Usage

Initialize git submodules:

    cd postoffice_sim
    git submodule update --init --recursive
    
Change permission for python scripts:

    find . -name *.py -exec chmod +x {} \;
        
Let git ignore permission changes within the repo:

    git config core.filemode false
    git submodule foreach --recursive git config core.filemode false
   
Install ROS dependency in ws:

    cd <your_ws>
    rosdep install --from-paths src --ignore-src -r -y

(Optional) Update submodules to the newest version

    git submodule update --remote

(Important) Follow the instructions in darknet_ros to install YOLO. My GPU is NVIDIA GeForce RTX 3050 Laptop GPU.

Compile the ws

    catkin_make -DCMAKE_BUILD_TYPE=Release