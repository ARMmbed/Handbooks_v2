#API Breakdown


The mbed library provides the C/C++ software platform and libraries to build your applications. 

<span style="background-color:lightgray; color:purple; display:block; height:100%;padding:10px;">
Note: Not all platforms have the resource required to implement these APIs or have them implemented.
</span>

###Memory Model

* [Memory Model](http://developer.mbed.org/handbook/Memory-Model) - The memory model used by the mbed Library.

###Analog I/O

* [AnalogIn](http://developer.mbed.org/handbook/AnalogIn) - Read the voltage applied to an analog input pin.
* [AnalogOut](http://developer.mbed.org/handbook/AnalogOut) - Set the voltage of an analog output pin.

###Digital I/O

* Digital
	* [DigitalIn](http://developer.mbed.org/handbook/DigitalIn) -  Configure and control a digital input pin.
	* [DigitalOut](http://developer.mbed.org/handbook/DigitalOut) -  Configure and control a digital output pin.
	* [DigitalInOut](http://developer.mbed.org/handbook/DigitalInOut) - Bi-directional digital pins.
* Bus
	* [BusIn](http://developer.mbed.org/handbook/BusIn) -  Flexible way to read multiple DigitalIn pins as one value.
	* [BusOut](http://developer.mbed.org/handbook/BusOut) - Flexible way to write multiple DigitalOut pins as one value.
	* [BusInOut](http://developer.mbed.org/handbook/BusInOut) - Flexible way to read/write multiple DigitalInOut pins as one value.
* Port
	* [PortIn](http://developer.mbed.org/handbook/PortIn) -  Fast way to read multiple DigitalIn pins as one value.
	* [PortOut](http://developer.mbed.org/handbook/PortOut) - Fast way to write multiple DigitalOut pins as one value.
	* [PortInOut](http://developer.mbed.org/handbook/PortInOut) - Fast way to read/write multiple DigitalInOut pins as one value.
* [PwmOut](http://developer.mbed.org/handbook/PwmOut) - Pulse-width modulated output.
* [InterruptIn](http://developer.mbed.org/handbook/InterruptIn) -  Trigger an event when a digital input pin changes.

###Digital Interfaces

* [Serial](http://developer.mbed.org/handbook/Serial) -  Serial/UART bus.
* SPI
	* [SPI](http://developer.mbed.org/handbook/SPI) - SPI bus master.
	* [SPISlave](http://developer.mbed.org/users/mbed_official/code/mbed/docs/tip/classmbed_1_1SPISlave.html) - SPI bus slave.
* I²C
	* [I2C](http://developer.mbed.org/handbook/I2C) - I²C bus master.
	* [I2CSlave](http://developer.mbed.org/users/mbed_official/code/mbed/docs/tip/classmbed_1_1I2CSlave.html) - I²C bus slave.
* [CAN](http://developer.mbed.org/handbook/CAN) - Controller-area network bus.

###Timers

* [Timer](http://developer.mbed.org/handbook/Timer) - Create, start, stop and read a timer.
* [Timeout](http://developer.mbed.org/handbook/Timeout) - Call a function after a specified delay.
* [Ticker](http://developer.mbed.org/handbook/Ticker) - Repeatedly call a function.
* [Wait|wait](http://developer.mbed.org/handbook/Wait) - Wait for a specified time.
* [Time|time](http://developer.mbed.org/handbook/Time) - Get and set the realtime clock.


###Real-time Operating System

* [RTOS](http://developer.mbed.org/handbook/RTOS) - Official mbed Real Time Operating System based on the RTX implementation of the CMSIS-RTOS API open standard.

###File System

* [LocalFileSystem](http://developer.mbed.org/handbook/LocalFileSystem) -  Using the mbed disk as storage from within a program.
* [SDFileSystem](http://developer.mbed.org/handbook/SDFileSystem) -  Using the mbed disk as storage from within a program.

###USB

* [USBDevice](http://developer.mbed.org/handbook/USBDevice) - Using mbed as a USB Device.
	* [USBMouse](http://developer.mbed.org/handbook/USBMouse) - Emulate a USB Mouse with absolute or relative positioning.
	* [USBKeyboard](http://developer.mbed.org/handbook/USBKeyboard) - Emulate a USB Keyboard, sending normal and media control keys.
	* [USBMouseKeyboard](http://developer.mbed.org/handbook/USBMouseKeyboard) - Emulate a USB Keyboard and a USB mouse with absolute or relative positioning.
	* [USBHID](http://developer.mbed.org/handbook/USBHID) - Communicate over a raw USBHID interface, great for driverless communication with a custom PC program.
	* [USBMIDI](http://developer.mbed.org/handbook/USBMIDI) - Send and recieve MIDI messages to control and be controlled by PC music sequencers etc.
	* [USBSerial](http://developer.mbed.org/handbook/USBSerial) - Create a virtual serial port over the USB port. Great to easily communicate with a computer.
	* [USBAudio](http://developer.mbed.org/handbook/USBAudio) - Create a USBAudio device able to receive audio stream from a computer over USB.
	* [USBMSD](http://developer.mbed.org/handbook/USBMSD) - Generic class which implements the Mass Storage Device protocol in order to access all kinds of block storage chips.

* [USBHost](http://developer.mbed.org/handbook/USBHost) - Using mbed to act as USBHost.
	* [USBHostMouse](http://developer.mbed.org/handbook/USBHostMouse) - Receive events from a USB mouse.
	* [USBHostKeyboard](http://developer.mbed.org/handbook/USBHostKeyboard) - Read keycode-modifier from a USB keyboard.
	* [USBHostMSD](http://developer.mbed.org/handbook/USBHostMSD) - Read-write a USB flash disk.
	* [USBHostSerial](http://developer.mbed.org/handbook/USBHostSerial) - Communicate with a virtual serial port.
	* [USBHostHub](http://developer.mbed.org/handbook/USBHostHub) - You can plug several USB devices to an mbed using a USB hub.

###Networking
* [Ethernet](http://developer.mbed.org/handbook/Ethernet) - Ethernet network.
	* [Ethernet Interface](http://developer.mbed.org/handbook/Ethernet-Interface) - mbed IP library over Ethernet.
	* [TCP/UDP Socket API](http://developer.mbed.org/handbook/Socket) - A simple and consistent way to communicate using bsd-like TCP and UDP sockets over various transports such as ethernet, wifi and mobile networks.
	* [TCP/IP Protocols and APIs](http://developer.mbed.org/handbook/TCP-IP-protocols-and-APIs) - A list of libraries and applications, developed by mbed users, implementing different protocols and services API.