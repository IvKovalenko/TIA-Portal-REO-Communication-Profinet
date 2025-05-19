# TIA-Portal-REO-Communication-Profinet
This project is designed for integration into TIA Portal (recommended with S7-1500), where it can be used as a module for Profinet-based communication with REO devices.

🛠 Description
This project implements communication between Siemens PLCs (TIA Portal) and REO devices via Profinet, supporting two operating modes:

Normal Mode — standard data exchange
Parameter Mode — parameter configuration mode

Communication is handled using standard Siemens functions:

DPRD_DAT — for reading data from the device
DPWR_DAT — for writing data to the device

The code performs:

Reading and writing REO device registers
Sending a sequence of commands:

Write Enable
Parameter Write
Release Write Enable
Read back and confirmation

Transmitting and receiving status and diagnostic information

Code is written by german developer and can consist german words and commmentaries.

🔧 Usage
The repository contains an archive of the Global Library. You need to extract this archive and add the Function Block (FB) from the library into your own project.
For parameter address mapping, refer to the official REO Profinet documentation, which provides register addresses in hexadecimal format.

📁 Contents
SCL FB code for parameter transmission and mode control

📌 Requirements
Siemens TIA Portal (version V18 or newer)
Compatible PLC (e.g., S7-1500)
Profinet connection to the REO device
REO documentation with parameter register addresses

📄 License
This project is licensed under MIT.
