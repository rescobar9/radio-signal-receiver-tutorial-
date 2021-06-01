# Radiosignalreceiver
## Step 1

In the menu on the left, click on the ``||Radio:Radio||`` menu and drag the ``||Radio:radio set group 1||`` block inside the ``||Basic:on start||`` block.
 ```blocks
 radio.setGroup(1)
```

## Step 2
In the menu on the left, click on the ``||Radio:Radio||`` menu and drag the ``||Radio:on radio received receivedNumber||`` block to the block panel.
```blocks
radio.onReceivedNumber(function (receivedNumber) {
	
})
radio.setGroup(1)
```

## Step 3
In the menu on the left, click on the ``||Basic:Basic||`` menu and drag the ``||Basic:show number 0||`` block inside the ``||Radio:on radio received receivedNumber||`` block. 
```blocks
radio.onReceivedNumber(function (receivedNumber) {
    basic.showNumber(0)
})
radio.setGroup(1)
```

## Step 4
Drag the ``||Variables:receivedNumber||`` that is on the ``||Radio:on radio received||`` block and replace the 0 inside the ``||Basic:show number 0||``.
```blocks
radio.onReceivedNumber(function (receivedNumber) {
    basic.showNumber(receivedNumber)
})
radio.setGroup(1)
```

## Step 5
Connect the Micro:bit to the USB port on your computer. Then click on ``||LED:Download||`` (Make sure that you download the file to the Micro:bit drive")
```blocks
radio.onReceivedNumber(function (receivedNumber) {
    basic.showNumber(receivedNumber)
})
radio.setGroup(1)
```
## Step 6
Congratulations, you did it!