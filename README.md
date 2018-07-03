# Quasaar-Box
A small sound/music project for Arduino

*** This sketch uses the Arduino pitch.h library. ***
You will need to download that library and add it to your sketch folder.
Read more notes in the Arduino Sketch file.

MATERIALS
3 POTENTIOMETERS
(3x) 10K Ohm Linear B potentiometer
P1 - A3 - value determines the baseline of our tone
P2 - A4 - value determines the high-point modulation
P3 - A5 - value determines the delay between playing tones

2 BUTTONS
(1x) Momentary button
(1x) Continuous on/off SPST switch - or button 
--- 2 momentary will work, however the switch allows us to hold one button in the on state ---
(2x) 10K resistors for buttons
B1 - p12 - plays the tone quickly and stops playing when released
B2 - p8 - plays the tone continuously until it is switched off
//-- if  B1 and B2 are pushed simultaneously, the tone jumps up one octave 

1 LED
(1x) LED
(1x) 220 resistor for LED
L1 - p2 - LED to provide visual feedback when a note is playing.

1 SPEAKER
1 Arduino NANO
1 Breadboard
Jumper wires
(cats – optional)

HOW IT WORKS
P1 selects a low value. P2 selects a top value. The device will randomize a number between the two and select that to play. Delay setting is for between notes.
Some interesting results can be obtained when we drop the delay down to nearly nothing. If we drop P1 down to zero and change the value of P2, the device will produce a squelching sound. Some sounds can even bring us back to the days of dial up modems. Dropping P2 down to zero and changing the value of P1 will produce a steady note from the scale. My friend Mark Morpurgo, who is a musical genius, helped me to decipher the pitch library. We were able to put together a number of different arrays based on the library. These allow us to harness an individual musical scale and embed that inside our project. This is a major benefit to our project. Our device now resembles more of a musical instrument that one can play - to forsake other saw-wave devices that seem to merely annoy. I have included one scale in the code. It is possible to use a potentiometer to select from a number of scales. For simplicity, I use only one scale in this demo.
