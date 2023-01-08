
**Sensing Modules:**

In this Sensing Modules we are using two sensors like: Water level sensor and Temperature sensor. Liquid level monitoring system with different levels indicated by using water level sensor. It also signifies when the water level is below and above the requirement. And the temperature sensor is used to know whether the temperature of the liquid is hot, mild, or cold.

\\

**Voice Module:**

This module uses the ISD1820 voice record and playback IC to record a single voice message of up to 10 seconds in length. The recorded message is stored in its specialized analogue flash memory that will keep the message stored even when power is removed.
Monitoring and detecting the level and the temperature of the liquid in a cup or a glass by instructing them through voice assistant whenever the container full or nearly full or whether the liquid is hot, mild, or cold. So, that they can avoid unnecessary spilling or overflowing of liquid.
1. VCC– 3.3V power supply 
2. GND– Power ground 
3. REC – The REC input is an active‐HIGH record signal. The module starts recording whenever REC is HIGH. This pin must remain HIGH for the duration of the recording. REC takes precedence over either playback(PLAYL or PLAYE) signal.
 4. PLAYE – Playback, Edge‐activated: When a HIGH‐going transition is detected on continues until an End‐of‐Message (EOM) marker is encountered or the end of the memory space is reached. 
5. PLAYL – Playback, Level‐activated, when this input pin level transits for LOW to HIGH, a playback cycle is initiated. 
6. Speaker Outputs – The SP+ and SP‐ pins provide direct drive for loudspeakers with impedances as low as 8Ω. 
7. MIC – Microphone Input, the microphone input transfers its signals to the on‐chip preamplifier. 
8. FT – Feed Through: This mode enable the Microphone to drive the speaker directly. 
9. P‐E – Play the records endlessly.

\\

Record Operate Guide:
1. Push REC button then the RECLED will light and keep push until record end. 
2. Release the REC button 
3. Select Playback mode:   PLAYE, just need push one time, and will playback all of the record or power down ; PLAYL, you need always push this button until you want to stop playback record or end, When short P‐E jumper the record will playback time a time until jumper off or power down 
4. FT mode, when short FT jumper, that means all of you speak to MIC will direct playback to Speaker.

\\

**Power Module:**

A lithium-ion or Li-ion battery is a type of rechargeable battery which uses the reversible reduction of lithium ions to store energy. It is the predominant battery type used in portable consumer electronics and electric vehicles. It also sees significant use for grid-scale energy storage and military and aerospace applications. Compared to other rechargeable battery technologies, Li-ion batteries have high energy densities, low self-discharge, and no memory effect (although a small memory effect reported in LFP cells has been traced to poorly made cells).

\\

**IoT Module:**

ESP8266-01 module communicates with the Arduino board over the Serial communication, which means that we need to connect it with the Arduino’s Serial pins 0, 1(Tx, Rx). But the problem here is that these pins will be busy because we will use the Arduino Serial monitor alongside the ESP8266-01 for debugging purposes. So, we need to find another two Serial communication pins to use them with the ESP8266-01.
Fortunately, Arduino made this easy. For this we are creating a library called “SoftwareSerial” which developed to allow serial communication on other digital pins of the Arduino, using software to replicate the functionality.
