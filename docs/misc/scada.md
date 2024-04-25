Supervisory Control and Data Acquisition (SCADA) is a system used for controlling industrial processes and infrastructure systems. SCADA systems are crucial for managing large-scale, complex processes that require real-time monitoring and control, often spread over large geographical areas. These systems are widely used in utility management (like water and power distribution), manufacturing, and processing industries.

SCADA (Supervisory Control and Data Acquisition) systems play a crucial role in the broader landscape of [[industrial control systems (ICS)]], interacting with and often complementing other systems like [[Distributed Control Systems (DCS)]] and Programmable Logic Controllers (PLC).

Some key components include:

1. [[Human-Machine Interface (HMI)]]: The interface through which human operators interact with the SCADA system, monitoring processes, and issuing commands.
2. **Supervisory Computers**: These are the central processing units that communicate with the field devices and gather data. They also send control commands to the field.
3. [[Remote Terminal Units (RTUs)]] and [[Programmable Logic Controllers (PLC)|Programmable Logic Controllers (PLCs)]]: RTUs and PLCs are located at remote sites and are responsible for interfacing with sensors and actuators, converting sensor signals to digital data, and sending control commands.
4. **Communication Network**: This network facilitates data exchange between the supervisory computers and the field devices (RTUs/PLCs).
5. **Data Acquisition System**: This system collects, processes, and stores the data for later use.

The following is how SCADA works:

- Data Collection: RTUs and PLCs collect data from sensors in the field and send it to the central supervisory system.
- Data Processing: The supervisory system processes this data, which can then be displayed on the HMI, alerting operators to current conditions or issues.
- Control: Operators can issue control commands through the HMI, which are then relayed to the RTUs and PLCs to implement changes in the process or system.
- Automation: SCADA systems can also automate responses to certain conditions without human intervention, based on predefined parameters.

SCADA systems provide comprehensive monitoring and control over large-scale processes, leading to increased efficiency. They improve safety by enabling the remote operation of dangerous processes and provide alarms and shutdown mechanisms in case of failures.

SCADA systems collect vast amounts of data, which can be analyzed to improve operational efficiency and aid in predictive maintenance.