# CS 350 Final Project - Smart Thermostat

This repository holds all the pieces for my final project in my Emerging Systems (CS 350) course. The main goal was to build a working smart thermostat from scratch using a Raspberry Pi.

The key files I'm submitting for my portfolio are:
*   `Thermostat.py`: This is the main Python code that makes the whole thing run.
*   `state_machine_diagram.pdf`: A visual chart I made in draw.io that shows how the thermostat switches between being off, heating, and cooling.
*   *(I also submitted a video of the project working as part of the assignment. Video file was too big for gitHub)*

---

### My Project Reflection

For this project, I had to build a smart thermostat that could solve a simple problem: keeping a room at a specific temperature. I wrote a Python program that reads the current room temperature using a sensor, and then based on a target temperature that I can change with up/down buttons, it decides what to do. It shows everything on a little LCD screen, like the time, the current temperature, and the target temperature. To show whether it's working, a red light pulses when it's "heating," and a blue light pulses when it's "cooling." A third button switches the whole system between heating, cooling, or just being off.

Looking back, I think what I did particularly well was sticking with the debugging until everything worked. At first, I had some simple typos in my code that I had to fix. But the hardest part was when the code seemed right, but the program kept crashing. I eventually figured out that it wasn't a software bug, but a hardware issue where the sensor would stop working when the LEDs drew power. Realizing the difference between a code problem and a physical circuit problem was a big step for me.

Where I could improve is in making my code more robust against errors. Right now, if a wire comes loose and the sensor disconnects, my program might crash. If I were to do it again, I would add some `try...except` blocks in my code. That way, if the sensor stops responding, the program could just show an error on the screen instead of stopping completely. It would make the final product much more reliable.

Through this project, I've added some great tools to my skill set. I got really comfortable using Python libraries like `gpiozero` to control the hardware, which makes things a lot easier. I also learned how to use `diagrams.net` to create professional-looking diagrams like the state machine chart. Most importantly, I learned how to search online forums and read documentation from places like Adafruit to solve real hardware problems, which is a skill I know I'll need in the future.

A lot of the skills from this project will be super useful in other courses and future jobs. The biggest one is just knowing how to make software interact with the real world through sensors and other components, which is the basis of the Internet of Things (IoT). The process of debugging a system where the bug could be in the code OR the hardware is something I know I'll face again. Also, using a state machine to organize the "off," "heating," and "cooling" modes is a really clean way to handle program logic that I plan on using in other projects.

Finally, I really tried to make my code easy for others (and my future self) to read and update. I used simple, descriptive names for my variables (like `redLight` instead of `led1`) and broke the code into smaller functions with specific jobs (like `updateLights`). I also used comments to explain why I did things a certain way. By using a state machine, the project is also easy to adapt. If we wanted to add a new "fan only" mode, we could just add it as a new state without having to rewrite everything. This makes the whole project much cleaner and easier to maintain over time.
