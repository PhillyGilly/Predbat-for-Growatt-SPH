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
![2025-01-17 09 57 58](https://github.com/user-attachments/assets/fbfd019a-c932-41ad-980f-0ae884f000dc)
I just used a spare ethernet cable and picked out the orange, orange/white and green cores 
![2025-02-02 11 28 45](https://github.com/user-attachments/assets/9225d55e-b4ef-4e6c-9bc2-fb8c27ead925)
I haven't addressed the issues raised here but I am using an auto-control TTL-RS485 board
![2025-02-05 12 29 36](https://github.com/user-attachments/assets/0b3cd294-e97e-4e80-a23f-e26ba250af47)
This is my ESP2866 running WEMOSD1....yaml
One of the key points from CRC private diysolarforum group yaml is that ESP2866 is underpowered
![image](https://github.com/user-attachments/assets/0a69f93d-d1b2-47fd-bf5e-b47522f1143f)
This is the first pass ESP32 - mqtt running
![image](https://github.com/user-attachments/assets/233d5743-a03c-4373-9b63-47a71f7e2477)
As viewed in MQTT explorer

