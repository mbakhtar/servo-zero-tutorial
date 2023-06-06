# Servo Tutorial

```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
```

## Step 1 @showdialog
Plug your USB cable into the micro:bit. 
Insert the micro:bit into the Climate Action Board.
![breakout board with microbit](![breakout board](https://raw.githubusercontent.com/mbakhtar/wind-turbine-lesson-tutorial/master/breakout-resized.png))

## Step 2 @showhint 
Click on the button to the right of the download and follow the steps to pair our micro:bit.
![pairing gif](https://raw.githubusercontent.com/mbakhtar/iste-wind-energy-v1/master/pair%20microbit-280x203.gif)

## Step 3
Click on the ``||fwdMotors:Motors||`` drawer and find the 
``||fwdMotors:set servo1 to 0'||`` block. 
Nest it under the ``||basic:on start||`` block.

```blocks
fwdMotors.servo1.fwdSetAngle(0)
```
## Step 4
Click on the ``||input:Input||`` drawer. Find the ``||input:on button A pressed||``
block. Drag and drop the ``||input:on button A pressed||`` onto the coding workspace.
Next click on the ``||fwdMotors:Motors||`` drawer and find the 
``||fwdMotors:set servo1 to 0'||`` block. Nest it under the ``||input:on button A pressed||``

```blocks
fwdMotors.servo1.fwdSetAngle(0)
input.onButtonPressed(Button.A, function() {
    fwdMotors.servo1.fwdSetAngle(0)
})
```

## Step 5
Change the angle of the ``||fwdMotors:set servo1 to 0'||`` nested under 
``||input:on button A pressed||`` to ``||90||``. Right click
on the ``||input:on button A pressed||`` block and duplicate it. Change 
the greyed |on button A pressed| to ``||input:B||``. Next change the angle 
of the ``||fwdMotors:set servo1 90'||`` nested under ``||input: on button B pressed||``
to ``||-90||``. 
```blocks
fwdMotors.servo1.fwdSetAngle(0)
input.onButtonPressed(Button.A, function () {
    fwdMotors.servo1.fwdSetAngle(90)
})
input.onButtonPressed(Button.B, function () {
    fwdMotors.servo1.fwdSetAngle(-90)
})
```
## Step 6
Congratulations on completing the code. Click ``|Download|`` and test.
Go back to the lesson for more activities and extensions.
