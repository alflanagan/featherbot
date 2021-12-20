# Featherbot -- A Robot Walker Powered By ESP32-S2 Microcontroller
Code to drive an ESP32-S2 based robot.


## Why not CircuitPython

[CircuitPython](https://circuitpython.org/) is a project to allow you to run [python](https://www.python.org) on microcontrollers. In fact, as received, the [Adafruit ESP-32S2 Feather Development Board](https://www.adafruit.com/product/4769) has CircutPython already installed. When you plug the board in, it shows up as a drive on your PC, and to update the programming you can just copy a file to the drive.

This is _awesome_. It makes programming a microcontroller almost trivial for anyone who knows Python, which is a lot of people.  (Don't know python? Go learn. It's relatively easy, and it's everywhere.) Python on a microcontroller is about as far as you can get from the environment Python was designed for, but we've now got enough memory on microcontrollers to run it.

So why on Earth wouldn't I use it? Well, this project involves using I2C to drive _twelve_ servo motors, and I expect to need precise timing and some interrupt handling. I'm not sure CircuitPython is quite up to the task, and I'd hate to figure that out after many hours of development work. On the other hand, I may rue the choice someday.