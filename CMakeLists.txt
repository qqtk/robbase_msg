cmake_minimum_required(VERSION 2.4.6)
project(robbase_msg)

find_package(catkin REQUIRED COMPONENTS std_msgs message_generation)

#generate messages in the msg folder
add_message_files(
  FILES 
  encoders.msg
  Encoder.msg
  WheelSpeed.msg
)

#generate added messages with any dependencies listed here
generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS std_msgs message_runtime)
