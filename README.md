# Predbat-for-Growatt-SPH - Work In Progress

This aim of this project is to optimise the use of a family member's Growatt SPH hybrid inverter with Intelligent Octopus Go tariff.

![20240830092644](https://github.com/user-attachments/assets/5f19ee7a-f41a-4229-8dd7-e4bd9c4d5664)

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
You need to enable this through the front panel
![2025-02-02 08 37 56](https://github.com/user-attachments/assets/2daa8f3c-ccf5-40b3-ab1f-a3443b6f3552)

![2025-02-02 08 38 09](https://github.com/user-attachments/assets/e0dd59e3-0c1a-4c7a-8fdf-267a9f8e29b8)
![2025-02-02 11 28 45](https://github.com/user-attachments/assets/9225d55e-b4ef-4e6c-9bc2-fb8c27ead925)
![2025-02-05 12 29 36](https://github.com/user-attachments/assets/0b3cd294-e97e-4e80-a23f-e26ba250af47)
![image](https://github.com/user-attachments/assets/0a69f93d-d1b2-47fd-bf5e-b47522f1143f)
