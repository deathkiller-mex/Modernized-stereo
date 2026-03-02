# Modernized-stereo
I was gifted an old stereo, and I thought it would be fun to give it an upgrade and a fresh look, so I will add Bluetooth capabilities to an old portable stereo and might give it a new look with a new 3D printed case.

The stereo I will be using has a CD, a cassette, and a radio player. All these features will be left untouched; the only change that I will make is that I will remove the recording option, as the Bluetooth audio will be connected here.
TO power everything up, find a place where there are 12V, e.g., on my stereo, there were 2 cables that went from the power supply to the main board. I cut this cable and added two additional cables, which go to my board.

# ⚠⚠WARNING⚠⚠
Some stereos, like mine, may have an old transformer and some diodes connected afterward to transform the current from AC to DC. MAKE SURE TO NOT TOUCH ANYTHING BEFORE THE DIODES WHEN THE STEREO IS ON, OR YOU WILL BE SHOCKED. Additionally, DO NOT CONNECT YOUR BOARD BEFORE, AS THE BOARD WORKS WITH DC CURRENT, AND ANYTHING BEFORE THE DIODES IS AC. IF YOU CONNECT YOUR BOARD HERE, YOU WILL DAMAGE YOUR COMPONENTS!!!

# How to connect:
1. If your stereo has connectors like mine, cut the cables (+ & -), grab your own cables (the ones connected to the custom PCB), and connect them. Make sure you have the polarity right, or you will fry both the PCB and the stereo.
<img width="2000" height="1500" alt="image" src="https://github.com/user-attachments/assets/24296f50-331d-4a4c-85b8-187b7c8922c7" />

2. Now wire every component following the schematic and connect it to the power. MAKE SURE EVERYTHING IS CONNECTED CORRECTLY OR YOU WILL DAMAGE THE COMPONENTS!!

3. Now, if you can find the amplifier chip, connect L, R and GND to the labeled pins (if the pins are not labeled but the chip has its, look the pin layout on the internet and connect accordingly), IF your stereo is like mine and has a giant heatsink soldered into the pcb ignore the aplifier and connect into the volume knob, find the GND of the volume and connect the AUDIO GND in there, then connect L and R in the pins that are not wiper. You can connect to the wiper pins, but you will have no control over the volume, which is what I did since my stereo is a cable mess and not a single pin of anything is labeled.
If you did what I did, make sure you have the stereo in radio mode; otherwise, the Bluetooth and CD/Cassette signals will interfere, creating distortion. If radio mode is on, this will not happen (I have no idea why, but it works).

4. Now that everything is connected, try it out, turn everything on, look for the Bluetooth on your phone, and connect. play some audio and see if and how it plays. If the audio is dissorted or sounds weird turn it off and check all the connections.

# Now, if everything is up and working lets start some programming.
1. First, go into Arduino IDE and select the ESP32 board and install it if necessary.
2. Select ESP32 dev board.
3. Now, copy the code and paste it into the Arduino IDE. (Look for the code in the files).
4. You won't need to download any libraries since these are already in the code, so just. 
5. Turn on the power and connect the ESP32 to your computer via USB (make sure you DO NOT use a just charge cable, use a cable that also transfers data).
6. Now, click upload in Arduino IDE and wait for it to load.
7. Once loaded click the BOOT button on the ESP32.
8. Thats it everything should be working now.


BOM:

|Materials|Amount|Cost|Link|
|:-------:|:----:|:--:|:--:|
|ESP32    |1     |$5  |asdas|
|PCB 5x6cm|1|$2|asdad|
|Bluetooth Receiver|1|$1|12eads|
|Buck DC-DC 12V-5V|1|$1|dAdsad|
