# Predbat-for-Growatt-SPH - Work In Progress

This aim of this project is to optimise the use of a family member's Growatt SPH hybrid inverter with Intelligent Octopus Go tariff.

![image](https://github.com/user-attachments/assets/935202ee-259b-4bde-a70e-6350fbf2fb35)

As I already have a working GivEnergy installation with Home Assistant and Predbat, I decided to try to set up the same kind of system on their Growatt.
The main challenges here are:
a) to set up local monitor and control of the Growatt
b) to integrate it into PredBat

Steps to solution:
1. Install HA on available (spare) Raspberry Pi4 platform
2. Access Growatt Modbus port for local monitor
3. Access Growatt Modbus port for local control
4. Create new apps.yaml for Predbat
5. Create new service for Predbat

Background reading here:

https://community.home-assistant.io/t/esp8266-rs485-on-growatt-inverter-spurious-data-between-updates/529913/22

https://springfall2008.github.io/batpred/inverter-setup/#i-want-to-add-an-unsupported-inverter-to-predbat

![2025-02-02 08 37 40](https://github.com/user-attachments/assets/602e5737-80f4-4e65-9c46-14f665097cab)
You need to set com2 to VPP the front panel
![2025-02-02 08 37 56](https://github.com/user-attachments/assets/2daa8f3c-ccf5-40b3-ab1f-a3443b6f3552)
This is where I found the monitor/control yaml code
![image](https://github.com/user-attachments/assets/e294425d-d9e0-490e-b2d5-5172f848da38)
From the manual
I just used a spare ethernet cable and picked out the orange/white and blue/white cores. Note some reports of cores 4/5 being used
![image](https://github.com/user-attachments/assets/ce5a64e6-fa42-4f35-a223-ef3faf8afa93)
Fritzing sketch
![2025-03-03 13 44 24](https://github.com/user-attachments/assets/04073b04-0117-4aab-b2e4-b2d62618f2ae)
The back
![2025-03-10 17 57 36](https://github.com/user-attachments/assets/1afcfa83-dcc8-4636-941d-321ef46f877c)
The front
One of the key points from CRC private diysolarforum group yaml is that ESP2866 is underpowered
![image](https://github.com/user-attachments/assets/0a69f93d-d1b2-47fd-bf5e-b47522f1143f)
This is the first pass ESP32 - mqtt running
![image](https://github.com/user-attachments/assets/233d5743-a03c-4373-9b63-47a71f7e2477)
As viewed in MQTT explorer

