# 概述

这是一个在ROS Kinetic上创建多机器人/多智能体模拟环境，并实现导航的配置文件。

在使用前需要下载ROS Kinetic相关包，例如turtlebot，及navigation导航包等。

如果有什么问题，欢迎在issue里提问。



# Instruction

下载myprofile文件到你的ROS工作空间中。



# Launch 

Step 1: launch mp.launch

`roslaunch myprofile mp.launch robot_count:=5`

Step 2: launch amcl.launch

`roslaunch myprofile amcl.launch robot_count:=5`

After launch two **launch** files above, you should see the same windows as pics in **Screenshots**

> tip: in myrviz.rviz file, I saved 5 model of robots in it, so you'd best keep the *robot_count:=5* , otherwise  a modification of rviz config file (myprofile/launch/includes/myrviz.rviz) OR some items in GUI is needed



####  the overview calling sequence of files

As you can see multi files in this repo, the main calling sequence is as below:

> mp.launch -> one_robot_recur.launch ->  kobuki.launch.xml
>
> amcl.launch -> amcl_recur.launch && rviz ->  astra_amcl.launch.xml && move_base.launch.xml 



# Screenshots



![gazebo](C:/Users/LV1/Documents/GitHub/ROS-Multi-Robots/readme.assets/image-20201012101022913.png)



![image-20201012101105756](C:/Users/LV1/Documents/GitHub/ROS-Multi-Robots/readme.assets/image-20201012101105756.png)



**Point 5 goals for 5 robots**

![image-20201012102059190](C:/Users/LV1/Documents/GitHub/ROS-Multi-Robots/readme.assets/image-20201012102059190.png)



