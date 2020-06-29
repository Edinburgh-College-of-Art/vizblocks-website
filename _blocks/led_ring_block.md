---
name: LED Ring Block
behaviours:
 - name: LightAll
   arguments:
    - int red
    - int green
    - int blue
   tooltip: /assets/images/lightall.gif
 - name: LightSome
   arguments:
    - int red
    - int green
    - int blue
    - int numLEDs
   tooltip: /assets/images/lightsome.gif
 - name: Breathe
   arguments:
     - int red
     - int green
     - int blue
     - float frequency
   tooltip: /assets/images/breathe.gif
image: /assets/images/led_ring_block.png
---
Light up your project with our LED Ring Block. Using the `Breathe` behaviour you could make the block glow green when there are city bikes available near your home, or with the `LightSome` behaviour, you could use it to count down to your next calendar event.
