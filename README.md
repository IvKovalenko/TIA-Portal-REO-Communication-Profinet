# TIA-Portal-REO-Communication-Profinet
___
This project is designed for integration into TIA Portal (recommended with S7-1200 and S7-1500), where it can be used as a module for Profinet-based communication with REO devices.
___
## 🛠 Description

This project implements communication between Siemens PLCs (TIA Portal) and REO devices via Profinet, supporting two operating modes:


- Normal Mode — standard data exchange
- Parameter Mode — parameter configuration mode


Communication is handled using standard Siemens functions:

- DPRD_DAT — for reading data from the device
- DPWR_DAT — for writing data to the device

The code performs:

- Reading and writing REO device registers
- Sending a sequence of commands:
  - Write Enable
  - Parameter Write
  - Release Write Enable
  - Read back and confirmation
- Transmitting and receiving status and diagnostic information

Note: Code is written by a German developer and may contain German words and comments.
___
## 🔧 Usage

1. Extract the Global Library archive included in this repository.
2. In TIA Portal, open your project.
3. Import the extracted Global Library.
4. Add the Function Block(FB) "FB_REOComm", Function(FC) "FC_DecodeREOStatus" and Type "typeREOStatus" from the library to your program.
6. Configure Profinet connection according to your hardware setup.

For parameter address mapping, refer to the official REO Profinet documentation, which provides register addresses in hexadecimal format.
___
## 📁 Contents

SCL FB code for parameter transmission and mode control
___
## 📌 Requirements

Siemens TIA Portal (version V18 or newer)
Compatible PLC (e.g., S7-1500)
Profinet connection to the REO device
REO documentation with parameter register addresses
___
## 📄 License

This project is licensed under MIT.
___
## Reference links

- [REO Official Website](https://reo.de/) — for product information and documentation.
