# Predbat-for-Growatt-SPH - WIP

This aim of this project is to optimise the use of a family member's Growatt SPH hybrid inverter with Intelligent Octopus Go tariff.

![20240830092644](https://github.com/user-attachments/assets/5f19ee7a-f41a-4229-8dd7-e4bd9c4d5664)

As I already have a working GivEnergy installation with Home Assistant and Predbat, I decided to try to set up the same kind of system on ther Growatt.
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

