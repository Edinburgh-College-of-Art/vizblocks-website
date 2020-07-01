---
name: Servo Motor Block
behaviours:
 - name: GoTo
   arguments:
    - int angle
   tooltip: /assets/images/placeholder.jpg
   tooltip_alt:
 - name: GoAndReturn
   arguments:
    - int angle
    - int pauseMillis
   tooltip: /assets/images/placeholder.jpg
   tooltip_alt:
 - name: Wiggle
   arguments:
    - int angleOfSweep
   tooltip: /assets/images/wiggle.gif
   tooltip_alt: Servo block wiggling a star attachment back and forth.
image: /assets/images/servo_block.png
image_alt: Servo block with a feather attached as a pointer.
---
Get your project moving with the Servo Motor Block. You could try using the `GoTo` behaviour to build a barometer, or maybe the `Wiggle` behaviour to jingle a bell every time a space rocket is launched.
