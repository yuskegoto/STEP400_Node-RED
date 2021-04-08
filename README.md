# STEP400 example network for Node-RED
[STEP400](https://ponoor.com/en/products/step400/) is an high quality stepper controller for hobbist and installation developpers.
This Node-RED network demonstrates sample commands. For the complete functionality for the STEP400, please refer [the doc](https://ponoor.com/en/docs/step400/) and [sample files](https://ponoor.com/en/docs/step400/tutorial/). The [MAX patch](https://github.com/ponoor/step-series-example-Max) was created by kanta, the creater of the STEP400 and has covered most of its functionalities.

## About this Node-RED network
While the MAX-MSP and other tools are powerful and complehensive for most of users, we do have situations want to control the STEP400 from controllers with small footprints, like Raspberry Pi or Beaglebone. Node-RED is suitable for this purpose, so I created an example file, actually taken from actual project I worked on recently.
### Dependencies
- [node-red-dashboard](https://flows.nodered.org/node/node-red-dashboard)
- [node-red-contrib-osc](https://flows.nodered.org/node/node-red-contrib-osc)

## Description
### Boot sequence
This network demonstrates seqential boot procedure.
Each parameter (e.g. KVAL) can be set within the node.
On the right side you can find the OSC node and UDP out.
![Boot sequence](../main/pic/boot_sequence.png "Boot sequence")

### Individual control
Setting parameters can be send individually
![Individual control](../main/pic/individual_control.png "Individual control")

### Servo mode
In servo mode the motor follows continuous position setting command from controller, while normal movement commands does not accept further positional setting while in transition. Please refer [the documentation](https://ponoor.com/en/docs/step400/functional-description/servo-mode/) for more detail.
![Servo mode](../main/pic/servo_mode.png "Servo mode")
![Servo slider](../main/pic/servo_slider.png "Servo slider")
