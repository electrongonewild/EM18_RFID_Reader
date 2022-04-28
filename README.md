# EM18 RFID Reader
```RFID(Radio Frequency Identification)``` is a form of wireless communication that incorporates the use of electromagnetic coupling in the radio frequency portion.<br>
RFID reader is a device used to gather information from an RFID tag which can further used for various apllications which include e-payment, e-toll road pricing, e-ticketing for events/public transport, access control, authentication.<br>
Okay! Now let’s see how to read RFID tag using EM18 RFID reader and USB to TTL(CP2102)!
## Table of Contents
* [Documentation](README.md#documentation)
* [Prerequisites](README.md#prerequisites)
* [Connection Diagram](README.md#connections)
* [Getting Started](README.md#getting-started)
* [Implementation](README.md#implementation)
* [Contributions](README.md#contributions)
## Documentation
It is highly recommended to go through the Documentation first.<br>
Here is direct link for same.<br>
* [Datasheet](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiAnsWJnbb3AhWLIbcAHYoWCMMQFnoECAUQAQ&url=https%3A%2F%2Fcomponents101.com%2Fsites%2Fdefault%2Ffiles%2Fcomponent_datasheet%2FEM18%2520RFID%2520Reader%2520Datasheet.pdf&usg=AOvVaw1-NdYUcDfC8h57j6CnI9kd) 
## Prerequisites
* [Realterm](https://realterm.sourceforge.io/index.html#downloads_Download) or any other serial terminal
* USB to TTL (CP2102)
* EM18 RFID Reader Module
* Jumpers
* Basic knowledge of UART and serial communication
## Connections
![Alt text](Images/EM18CircuitDiag.PNG?raw=true "Title")
(Application Circuit referred from EM18 RFID reader [Datasheet](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiAnsWJnbb3AhWLIbcAHYoWCMMQFnoECAUQAQ&url=https%3A%2F%2Fcomponents101.com%2Fsites%2Fdefault%2Ffiles%2Fcomponent_datasheet%2FEM18%2520RFID%2520Reader%2520Datasheet.pdf&usg=AOvVaw1-NdYUcDfC8h57j6CnI9kd))
* Tx(EM18 RFID Reader) ---> Rx(USB to TTL)
* Power Supply (5V and GND)
* SEL pin ---> 5V
## Getting Started
Follow the steps for getting started:
* Connect the USB to TTL(CP2102) to USB port of PC and open device manager to check the port connected to serial bridge (USB to TTL).<br>
![Alt text](Images/deviceManager.png?raw=true "Title")
* Open Realterm or any other serial terminal you want to use.
* Open the port to which your serial device is connected make sure to check serial configuration as follows:<br>
    Baudrate : 9600<br>
    Data Bits : 8<br>
    Parity : None<br>
    Stopbits : 1<br> 
![Alt text](Images/serialConfig.PNG?raw=true "Title")
* That's it!!! Now you can send AT commands using realterm directly to Wi-Fi Module and also receive its response.
* Firstly check whether you receive ```OK``` in response to ```AT\r\n```, to make sure that your connections and configurations are fine.
* Now you can further proceed to other AT commands according to your application.
## Implementation
![Alt text](Images/wifiSerial.PNG?raw=true "Title")
## Contributions
For reporting any ```technical issue``` or proposing ```new feature```, please create new [issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue).



