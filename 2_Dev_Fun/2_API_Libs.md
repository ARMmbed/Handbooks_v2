#High-level Peripheral APIs

The mbed SDK gives you an API-driven approach to microcontroller coding.

We've done all the hard work of implementing drivers for the different [mbed platforms](/platforms), so you don't have to. It is liberating to fire up an interface, knowing it'll just work!

You can code using meaningful abstract objects and API calls, so you don't need to learn the microcontroller hardware details to get going. There is even a "Hello World!" example for every peripheral, just to get you started before you know it.

Take a look at some of these interfaces to get a feel of how it works: [digital out](/DigitalOut), [analog in](/Analogin), [SPI](/spi), [USB mouse](/USBMouse), [Timer](/timer), [CAN](/can).

But if needed, you can always bypass the APIs and talk directly to the microcontroller hardware using the low-level Cortex Microcontroller Software Interface Standard (CMSIS) APIs. Ideal when they are fine for most of your project, but one aspect needs specific low-level control.

<span style="background-color:lightgray; color:purple; display:block; height:100%;padding:10px;">
For all the mbed C/C++ SDK APIs, see the [API breakdown](/2_Dev_Fun/2_API_Libs_Breakdown/)<br />
To read more about mbed SDK coding style, see the [mbed SDK coding style guide](/3_Adv_Dev/2_Coding_Style/)
</span>

