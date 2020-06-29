---
name: Servo Motor Block
behaviours:
 - name: GoTo
   arguments:
    - int angle
   tooltip: /assets/images/wiggle.gif
 - name: GoAndReturn
   arguments:
    - int angle
    - int pauseMillis
   tooltip: /assets/images/placeholder.jpg
 - name: Wiggle
   arguments:
    - int angleOfSweep
   tooltip: /assets/images/placeholder.jpg
image: /assets/images/servo_block.png
---
Get your project moving with the Servo Motor Block. You could try using the `GoTo` behaviour to build a barometer, or maybe the `Wiggle` behaviour to jingle a bell every time a space rocket is launched.
