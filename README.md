I built a fire-fighting robot and named it Pyro Protector, Pyro comes from the Greek word (πῦρ) (pyr), meaning fire. so Pyro Protector should save you from fire.

This project is under the Capstone project subject at MMU University. I built the robot using Raspberry Pi as its microcontroller. it's a bad choice. however, I wanted to learn to use the Raspberry Pi especially since my university had provided it to use and give back after finishing the project. Thus I can learn using this technology without paying money. A better choice for this robot can be something like ESP32 as it uses significantly less power than the Raspberry Pi and it has WIFI and Bluetooth capabilities plus it's way cheaper. I'm gonna redo the whole project later with ESP32. stay tuned for that.

Pyro Protector requirement: To be able to put off small fires (let's say a tissue paper on fire) autonomously To be able to avoid obstacles and walls to connect it through an IoT cloud server such as BLYNK or ThingSpeak to connect the IoT server with a mobile app

As you can see that's a lot of requirements to cover in one project. This project is supposed to be done by 4 people. however, I was working on it alone. As a result, most of the functionalities were not working properly. that's why I didn't want to document my project and wanted to do it when I completed or redo the project, which is perfectionism. however, I came across a very encouraging video that taught me the importance of documenting your project and sharing it with others to spread knowledge even though your project has failed or is complete.

in this docs, I don't want to list all the items and connections only I want to teach you how to think like a proper engineer and how to think when you are working on a project.

let's also agree on one thing I will not be explaining every term you see here. if you find that there is a word or term you don't understand I highly recommend you search on some articles as if I explain those things this tutorial would be lengthy and I would waste time explaining things that other people explained better than me.

I see reading articles is way better than YouTube videos as you can learn much more information this way and believe it or not you will save time this way. I was being conceived by YouTube videos and thought I could learn from them faster but this is not true at all. written documentation is always better than video documentation. so keep that in mind

ok when you talk about a robot usually a lot of things can come to your mind for instance you may think of a robot car or a

in our case, the robot will be like a robot car. so you have to think of how many wheels your robot will be using, what type of motors you need, what type of batteries are required, and of course, what motor driver you will be using. a motor driver is a device that allows you to control the motors using a microcontroller. it sets between your microcontroller and your motors. since you can't control motors directly with a microcontroller as it will not be able to supply enough current to the motors. also connecting motors directly to a microcontroller can damage it and cost you a lot of money. now you understand the purpose of a motor driver. now what about the wheels? for the wheels, you have to consider the following. you need to consider the number of wheels, size, and types. wheels come in a lot of types such as
- Mecanum wheels
- Omni wheels
- Caster wheels
- Fixed wheels
- tracked wheels
we gonna use a fixed 65mm wheel for the Pyro Protector. take note that different types of wheels require different hardware setups and motor driver setups so make sure you fully understand how the wheels work before choosing them.

now we can choose 2 wheels setup with one caster wheel or we can use 4 wheels setup.
I chose the 4-wheel setup as I want to use 4 small DC motors.

And Then comes a very important question how are you gonna connect the 4 motors to the motor driver? the motor driver I choose is the L298n motor driver and it's a dual channel motor driver meaning you can control 2 motors independently with it. in our case, we are using 4 motors. you have two options either buy two motor drivers or use one and connect each to the motors in one channel.
