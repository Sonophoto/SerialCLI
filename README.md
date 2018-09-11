# SerialCLI

## Unfortunately this project has been concelled for opensourcing :-( but you can still run with the idea! :-)


## Project is in development, post an issue if you have a question about anything.

A UART Serial CLI framework for ATMegaxxxxP class processors using Wiring/Arduino it allows rapid prototyping of serial based device control interfaces. May not fully support ATMega328/P based "Unos"(tm)

Design implements a framework for sending and receiving commands via 3 wire serial (tx/rx/gnd @115200+ kbps)

The user provides in their implementation:

    1. Command name string, ASCII "C" String.
    2. Callback function that implements the command.
    3. Usage message returned on errors
    
SerialCLI provides a function that can be called in a loop [Simple Serial Server](http://) or driven by an interupt [ISR Serial Server](http://) to service a hardware serial port and implement the command set that the user has specified in their implementation.

Essentially this allows you to rapidly and consistently develop serial based command interfaces for sensors, motor controllers, simple robots, remote controllers, etc. AND then use this same interface to have another program on another computer talk to the SerialCLI interface of your device.

Quick and easy distributed computing with no timing quirks and deterministic response times from dedicated sensor controllers.
