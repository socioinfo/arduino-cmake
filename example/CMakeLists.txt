# Set a variable for commands below
set(PROJECT_NAME example)

# Define your project and language
project(${PROJECT_NAME} C CXX)

#set(${PROJECT_NAME}_BOARD pro)
set(${PROJECT_NAME}_BOARD uno)

# Define the source code
set(${PROJECT_NAME}_SRCS example.cpp)

# Define the port for uploading code to the Arduino
set(${PROJECT_NAME}_PORT /dev/ttyUSB0)

# If you set ${PROJECT_NAME}_BOARD to pro, you need to specify ARDUINO_CPU.
# Please see the following file for what to choose as ARDUINO_CPU:
# C:\Program Files (x86)\Arduino\hardware\arduino\avr\boards.txt
# This is windows path. For other OS'es it will look similar to
# "your_install_path/hardware/arduino/avr/boards.txt".
# ex. /opt/ardunio/hardware/arduino/avr/boards.txt
# For Arduino UNO where is no need to define anything, just comment out the CPU ID line,
# because Arduino UNO does not have different CPU options
#set(ARDUINO_CPU 16MHzatmega328)

# Command to generate code arduino firmware (.hex file)
generate_arduino_firmware(${PROJECT_NAME})
