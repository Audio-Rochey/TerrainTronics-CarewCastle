# Carew Castle LED Cloner
## Introduction

Carew Castle boards are tiny 10mmx10mm boards that are designed to power big LED's, other boards (like Conwy Castles) or Vibration Motors with up to 2Amps of current. (way more than a what you find on an output of a Wemos D1 or Arduino!)
Additionally, it can be used to "clone" the flicker pattern of a small 3mm candle flickering LED to a larger 1 Watt LED (any color) or even to Flexileds.
<img src="https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/b9ae9c61-ba5b-4f18-a80d-68170daa03aa](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/b9ae9c61-ba5b-4f18-a80d-68170daa03aa.jpg" width="400" >
<img src="https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/fc0d4db5-b82f-4338-84fd-ca66112e2ea3](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/fc0d4db5-b82f-4338-84fd-ca66112e2ea3.jpg" width="400" >
![2024-04-09 20_42_06-WIN_20240409_13_45_49_Pro](https://github.com/Audio-Rochey/TerrainTronics-CarewCastle/assets/15720888/94e54b91-9df9-4f28-8fd2-f2d8947b3be5)

INSERT PICTURE OF BOARD, BOTH SIDES and with an LED attached.
![MainImage](https://github.com/Audio-Rochey/blob/master/TerrainTronics-Wiston-Castle/pictures/IMG_1923.jpg)
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



Key components:
  
SL1603SL

> Written with [StackE

List item

dit](https://stackedit.io/).

> Written with [StackEdit](https://stackedit.io/).
