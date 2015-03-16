#Blinky

The first program we'll use is a test program - it's meant to show you that your board is functional and that you're compiling for the right platform. It's called [Blinky](http://developer.mbed.org/teams/mbed/code/mbed_blinky/). 

#What you need

To get this program going, all you need is: 

+ A BLE-enabled mbed board.

+ A user on [developer.mbed.org](developer.mbed.org) to access the compiler.

#Getting Blinky on your board

You can get Blinky working in just a few minutes.

1. Open the compiler and select or add your board. If you forgot how that's done, see the [Platform Registration section](/1_Getting_Started/3_User_Plat_Reg#Platform/).

2. Import [``Blinky``](http://developer.mbed.org/teams/mbed/code/mbed_blinky/) to your compiler. If you forgot how that's done, see the [IDE section](/1_Getting_Started/4_Using_IDE/).

3. Compile the code. It will be downloaded to your Downloads folder (on some browsers you may need to specify a download location).

4. Drag and drop the compiled file to your board.

5. Restart the board.

6. The LED will flash.

#Understanding and changing the code

The [next section](#understand) explains the code line by line, and assumes you've never worked with C++ before. If you're comfortable with the code, skip to the fun bits - [changing the code](#change) - to see some more possibilities. 

<a name="understand">
##Understanding the code
</a>

``Blinky`` is a very short piece of code. In the compiler, click ``main.cpp`` to see the code.

<span style="text-align:center; display:block;">
![Blinky main.cpp](/1_Getting_Started/Images/Blinky/OpeningBlinky.png)
</span>

Let's review it line by line:

``DigitalOut myled(LED1);``

DigitalOut is the [API class](http://developer.mbed.org/handbook/DigitalOut) that handles output to digital pins. In this line, we created a new object of type ``DigitalOut``, call it "myled" and specify that it refers to ``LED1`` - the first LED on the board.

<span style="background-color:lightgray; color:purple; display:block; height:100%; padding:10px">
**Tip:** exactly which LED is LED1 depends on your board. You can see the full schematics, including LEDs, on your board's [platform page](http://developer.mbed.org/platforms/).
</span>

``int main()``

This line declares that we've reached the main function - the function that runs be default every time the board is switched on (or restarted). You'll see soon that it contains a loop; if it didn't, it would stop running when it reached the last line of the code.

``while(1)``

While is a type of loop that says "keep running the code I contain so long as my condition is met, ie held to be true". The condition of this particular loop is "1". "1" means "TRUE", to a computer, so this loop's condition is always met, and the loop will never stop running. If we didn't use this loop, we'd turn the LED on and off only once, instead of continuously.

``myled = 1;``

As we said above, "1" to a computer means "TRUE". In the context of output (sending a command) to a digital pin (our LED), this means "send current", meaning the LED will be on.

``wait(0.2);``

"Wait" is a delay in the function's run. Since the program runs from line to line (sequentially) as fast as it can, if we want the LED to be on or off for a period that the human eye can actually perceive, we have to ask the program to wait between turning the LED on and off. In this case, we tell it to wait 0.2 seconds.

<span style="background-color:lightgray; color:purple; display:block; height:100%; padding:10px">
**Tip:** we don't need to specify that it's seconds; the ``wait`` function, as defined on the API, simply assumes that any value you send is in seconds. There are other functions that use different values, such as microseconds (``wait_us``) or milliseconds (``wait_ms``).
</span>

``myled = 0``

"0" is the opposite of "1", and means "FALSE". In the context of output (sending a command) to a digital pin (our LED), this means "stop current", meaning the LED will be off.

``wait(0.2)``

We again ask the program to wait before moving on to the next line. 

This is the end of the loop; since the loop's condition is "1", meaning it's always TRUE and never stops running, we'll now go back to our first line: ``myled = 1``, and turn the LED on again. And so on and so forth.
 
<a name="change">
##Changing the code
</a>

###Sequential LEDs

Your board likely has more than one LED; you can have your LEDs blink in sequence:

```c

	#include "mbed.h"

	DigitalOut myled1(LED1);
	DigitalOut myled2(LED2); //adds another myled object, referring to the second LED on the board

	int main() {
    		while(1) {
        		myled1 = 1; //turn on first LED
        		wait(0.2);
        		myled1 = 0; //turn off first LED
        		wait(0.2);
        		myled2 = 1; //turn on second LED
        		wait(0.2);
        		myled2 = 0; //turn off second LED
        		wait(0.2);
    		}
	}
```

###Concurrent LEDs

Alternatively, you can have both LEDs blink at the same time:

```c

	#include "mbed.h"

	DigitalOut myled1(LED1);
	DigitalOut myled2(LED2);


	int main() {
    		while(1) {
        		myled1 = 1;
        		myled2 = 1; //although these lines are executed one after the other, not both at once, the time between them is so short that to us it seems concurrent
        		wait(0.2);
        		myled1 = 0;
        		myled2 = 0;
        		wait(0.2);
    		}
	}
```


