# 2 ways to control Arduino(MCU)

## 1. run code in arduino (cpp)
### 1. put code in mcu
### 2. robot reads arduino code
    rosrun rosserial_arduino serial_node.py </dev/ttyACM0(port_name)> __name:=<custom_topic_name>

## 2. run code in robot (python)
### 1. put code in sbc & make custom package
    <custom code to send to arduino>
### 2. arduino reads robot code
    <sbc reading code>
    
