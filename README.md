# Carew Castle LED Cloner
## Introduction

Carew Castle boards are tiny 10mmx10mm boards that are designed to power big LED's, other boards (like Conwy Castles) or Vibration Motors with up to 2Amps of current. (way more than a what you find on an output of a Wemos D1 or Arduino!)
Additionally, it can be used to "clone" the flicker pattern of a small 3mm candle flickering LED to a larger 1 Watt LED (any color) or even to Flexileds.

<img src="https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/b9ae9c61-ba5b-4f18-a80d-68170daa03aa](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/b9ae9c61-ba5b-4f18-a80d-68170daa03aa.jpg" width="400" >
<img src="https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/fc0d4db5-b82f-4338-84fd-ca66112e2ea3](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/fc0d4db5-b82f-4338-84fd-ca66112e2ea3.jpg" width="400" >
<img src="https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/94e54b91-9df9-4f28-8fd2-f2d8947b3be5](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/94e54b91-9df9-4f28-8fd2-f2d8947b3be5).jpg" width="400" >


Please take a minute to read through the uses - there's usability hints throughout that will inspire creative usage!

## Maximum limits etc

| Parameter              | Value     | Notes                                                                                                              |
| ---------------------- | --------- | ------------------------------------------------------------------------------------------------------------------ |
| Input Voltage Min      | 2.7 Volts | Can be run from a coin cell, but not optimal, as coin cells have limited power capability                          |
| Input Voltage Max      | 5.5 Volts | Can be run from a USB Batter/Wall adapter.                                                                         |
| Output Current         | 3 Amps    | Any more current than this will cause some self heating of the transistor and potential cause failure.             |
| 30AWG Wire Wrap Rating | 0.8Amps   | Wire Wrap Wire is only rated for 0.8Amps. Care should be taken pulling more than this.                             |
| 26AWG Wire Wrap Rating | 3.5Amps   | If you plan on pulling the maximum current through the device, consider using thicker 26AWG wire. (not wire wrap!) |

Notes:

> [!IMPORTANT]
> - If you're planning on connecting the **GATE** pin to an Arduino, the +5V solder tab should be connected to the same voltage as the the processor IO.
>     - Arduino Uno uses 5V. Connect the 5V solder tab to the Arduino 5V Power Source
>      - Wemos D1 Mini's actually run their inputs and outputs at 3.3V. Run the board

<BR><BR><BR>

## Example Use Cases



### Example 1 - Cloning a 3mm Candle LED to a 1Watt LED.
![2024-04-09 20_38_37-Clipboard](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/153f9ea5-1b00-4d8c-8bfc-234d88b19d45)

Many high power Leds are unable to do clever things like Flickr. MOst folks solve problems like this by using an arduino or a programmable solution. 
Using the Carew Castle circuit board in this manner clones the High speed candle flickering effect to its output, which drives much larger leds. It's a completely software free solution. 
Such a solution also allows you to synchronize lights by running them all in parallel from the same output - giving an awesome effect, such as a candle on the table being in sync with a high power LED shining at hte back wall.

![Screenshot 2024-04-09 171053](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/e36c786a-2380-4522-9a8c-378b62a1a413)

### Example 2 - Cloning a 3mm Candle to all outputs of a Conwy Castle
INSERT PICTURE
2 methods here: 
- One as a straight power switch
- Cloning the Candle to all 4 outputs. (flicker will be synchronous)

### Example 3 - Using an Arduino or a Wemos D1 to power a larger load (e.g. 1W LED, Conwy or Vibration Motor) 
INSERT BLOCK DIAGRAM

<BR><BR><BR>

## Hooking up LED's or motors?


### Large LED's (such as the STar 1W LED's or Flexileds)

[Amazon Search Link for 1W LED's](https://www.amazon.com/s?k=1W+LED)

[TerrainTronics for Flexiled Noodle LED's](http://www.terraintronics.com)

> *Every LED needs some method of limiting the current through it*. 

This is typically done with a resistor. The higher power the LED, the more power needs to be dissipated in the resistor as well.
Some LED's can be purchased with a resistor already soldered/connected, if that's the case the resistor should be connected between LED+ and one of the ground pads

![Screenshot 2024-04-11 101735](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/ac9b94d5-a0de-40e0-9fb3-660670c321d9)

By default, a 100Ohm resistor is between the LED- and GND on the board, so if your LED needs a current limiting resistor, you should wire it between LED+ and LED-.

Adding a solder bridge on each of these triangular pads will each add an additional 100Ohm resistor in parallel, effectively reducing the overall resistance, and making the LED brighter.
- Adding one bridge will half the overall resistance (to 50Ohm). This will double the current through the LED.
- Adding both bridges will reduce the resistance to 33Ohm (one third). This will increase teh current (brightness) through the LED further.

If higher power capability is needed (and therefor a lower resistance), an external power resistor should be used. Many of the 1 Watt LED's come with this resistor onboard (and well heatsinked). 


> [!TIP]
> The LED and inline resistor should be connected between LED+ and GND.

<table align="center">
<tr>
<th>1 Watt LED with External Resistor</th>
<th>1 Watt LED *without* a resistor</th>
</tr>
<tr>
<td>
  
![Screenshot 2024-04-09 155659](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/ca05e5fd-fde2-4a98-8637-b17aa9bcebfe)

</td>
<td>
  
![Screenshot 2024-04-09 155534](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/9ecabdf6-f0f1-4c2c-af8a-8046f59300d0)

</td></tr> </table>


## How does it work?

![CarewSchematic](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/6b70ce80-64cf-497b-9c26-00268dbbe7d2)

The main part doing the heavy lifting is the Power MOSFET on the board. **(Q2)** It is switched ON when the signal at the **GATE** pin is pulled low to GND from it's VDD (5V or 3.3V) Voltage.

Flickering Candle style LED's work by switching on and off thousands of times a second. Every time they switch on, they force the **GATE** pin low, which switches on the transistor, passing electric current through to LED+. This happens on and off, hundreds and thousands of times a second.

This is why and how the board can clone the flickering candle to any type of LED or Conwy Castle board. 


