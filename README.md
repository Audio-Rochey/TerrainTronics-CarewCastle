# Carew Castle LED Cloner
## Introduction

Carew Castle boards are tiny 10mmx10mm boards that are designed to power big LED's, other boards (like Conwy Castles) or Vibration Motors with up to 2Amps of current. (way more than a what you find on an output of a Wemos D1 or Arduino!)
Additionally, it can be used to "clone" the flicker pattern of a small 3mm candle flickering LED to a larger 1 Watt LED (any color) or even to Flexileds.

<img src="https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/b9ae9c61-ba5b-4f18-a80d-68170daa03aa](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/b9ae9c61-ba5b-4f18-a80d-68170daa03aa.jpg" width="400" >
<img src="https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/fc0d4db5-b82f-4338-84fd-ca66112e2ea3](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/fc0d4db5-b82f-4338-84fd-ca66112e2ea3.jpg" width="400" >

![2024-04-09 20_42_06-WIN_20240409_13_45_49_Pro](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/94e54b91-9df9-4f28-8fd2-f2d8947b3be5 | width=100)

Please take a minute to read through the uses - there's usability hints throughout that will inspire creative usage!




## Uses



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


## How does it work?


### Limiting current through the big LED externally, or onboard

*Every LED needs some method of limiting the current through it*. This is typically done with a resistor. The higher power the LED, the more power needs to be dissipated in the resistor as well.
Some LED's can be purchased with a resistor already soldered/connected, if that's the case the resistor should be connected between LED+ and one of the ground pads 
![Screenshot 2024-04-11 101735](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/ac9b94d5-a0de-40e0-9fb3-660670c321d9)

By default, a 100Ohm resistor is between the LED- and GND on the board, so if your LED needs a current limiting resistor, you should wire it between LED+ and LED-.

Adding a solder bridge on each of these triangular pads will each add an additional 100Ohm resistor in parallel, effectively reducing the overall resistance, and making the LED brighter.
- Adding one bridge will half the overall resistance (to 50Ohm). This will double the current through the LED.
- Adding both bridges will reduce the resistance to 33Ohm (one third). This will increase teh current (brightness) through the LED further.

If higher power capability is needed (and therefor a lower resistance), an external power resistor should be used. Many of the 1 Watt LED's come with this resistor onboard (and well heatsinked).


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







Key components:
  
SL1603SL

> Written with [StackE

List item

dit](https://stackedit.io/).

> Written with [StackEdit](https://stackedit.io/).
