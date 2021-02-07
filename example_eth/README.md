# Basic Ethernet Example for STM32H743 using FreeRTOS and lwIP
Most of the stuff is generated using CubeMX (v6.1.1 with HAL library v1.8.0).  
Caveats:
* Generating the project using CubeMX with both FreeRTOS and lwIP in a single step leads to compilation errors. Workaround: Activate FreeRTOS, generate code and then add lwIP and regenerate the code in second step
* Changes/additions described in: https://community.st.com/s/article/How-to-create-project-for-STM32H7-with-Ethernet-and-LwIP-stack-working need to be implemented. However, make sure that pin-definitions, clock-settings etc. need to be adapted to the eLITe-Board.
* Pinging the board (with a fixed IP set to 192.168.10.2) works, but ST's drivers might still contain some bugs. No stability or throughput tests were run for this project. See https://community.st.com/s/question/0D50X0000C6eNNSSQ2/bug-fixes-stm32h7-ethernet for further information.
