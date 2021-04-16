1. Setup the SMB simulation  
   see Lecture1/catkin_ws/src/READEME.md
2. Launch the simulation with roslaunch and inspect the created nodes and their topics  
rosnode list  
rostopic list  
rostopic echo [TOPIC]  
rostopic hz [TOPIC]  
rqt_graph   
![avatar](catkin_ws/src/rqt_graph.png)
3. Command a desired velocity to the robot from the terminal  
rostopic pub /cmd_vel geometry_msgs/Twist   
"linear:   
  x: 0.0  
  y: 0.0  
  z: 0.0  
angular:   
  x: 0.0  
  y: 0.0  
  z: 1.0"  

4. Use ​ teleop_twist_keyboard ​ to control your robot using the keyboard  
rosrun teleop_twist_keyboard teleop_twist_keyboard.py  

5. Write a launch file with the following content :
- smb simulation with a different world:
Include ​ smb_gazebo.launch​ file and change the ​ world_file ​ argument to a
world from the directory ​ /usr/share/gazebo-9/worlds  
see smb_gazebo_robocup.launch