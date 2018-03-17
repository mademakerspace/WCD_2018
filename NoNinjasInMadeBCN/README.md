# NoNinjas motion-detection system with RCWL-0516, ESP8266, and MQTT

This project is aimed at detecting when there are members active in our makerspace. This system could let others know when the space is open, as well as giving us a way to quantify and visualize the frequency of activity in different areas of the space. 

## Testing the RCWL-0516
We found that the maximum range of detection was approximately 3-4 meters, depending on the orientation of motion to the PCB. As we are concerned that the neighbors' movement will trigger the system, we wanted to see if we could use microwave opaque materials to block the sensor. We started with the closest thing we had on hand- a beer can. After cutting a hole, we put the RCWL inside the can and.... it worked! The sensor only detected movement that passed in front of the opening in the beer can. This means we can easily shield our neighbors from ~~dangerous microwave radiation~~ accidentally triggering our ninja detection system.

## Setting up Node Red

Using [this tutorial](https://randomnerdtutorials.com/esp8266-and-node-red-with-mqtt/) as a guide, we will set up some ESP8266 nodes around the space which will communicate with a Raspberry Pi using MQTT (Node Red)
