# Radiosignalreceiver
## Step 1

In the menu on the left, click on the ``||Radio:Radio||`` menu and drag the ``||Radio:radio set group 1||`` block inside the ``||Basic:on start||`` block.
 ```blocks
 radio.setGroup(1)
```

## Step 2
In the menu on the left, click on the ``||Variables:Variables||`` menu, make a variable and call it light level.  

## Step 3
In the menu on the left, click on the ``||Variables:Variables||`` and drag the ``||Variables:set light level to 0||`` block inside the ``||Basic:forever||`` block. 
```blocks
let light_level = 0
radio.setGroup(1)
basic.forever(function () {
    light_level = 0
})
```

## Step 4
In the menu on the left, click on the ``||Input:Input||`` menu and drag the ``||Input:light level||`` block and replace it with the 0 inside the ``||Variables:set light level to 0||`` block inside the ``||Basic:forever||`` block. 
```blocks
let light_level = 0
radio.setGroup(1)
basic.forever(function () {
    light_level = input.lightLevel()
})
```

## Step 5
In the left menu, click the ``||Radio:Radio||`` block and drag the ``||Radio:radio send number 0||``  inside the ``||Basic:forever||`` block under the ``||Variables:set light level to||`` ``||Input:light level||``. 
```blocks
let light_level = 0
radio.setGroup(1)
basic.forever(function () {
    light_level = input.lightLevel()
    radio.sendNumber(0)
})
```
 
## Step 6
Click on ``||Variables:Variables||``, and drag the ``||Variables:light level||`` block and replace the 0 inside the ``||Radio:radio send number||`` ``||Variables:light level||`` block.   
```blocks
let light_level = 0
radio.setGroup(1)
basic.forever(function () {
    light_level = input.lightLevel()
    radio.sendNumber(light_level)
})
```

## Step 7
Connect the Micro:bit to the USB port on your computer. Then click on ``||LED:Download||`` (Make sure that you download the file to the Micro:bit drive")
```blocks
let light_level = 0
radio.setGroup(1)
basic.forever(function () {
    light_level = input.lightLevel()
    radio.sendNumber(light_level)
})
```
## Step 8
Congratulations, you did it!