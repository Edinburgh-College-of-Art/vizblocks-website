---
name: Programming a VizBlock
difficulty: Intermediate
description: This tutorial goes through the process of programming your VizBlock using Arduino, allowing you to add custom behaviours and code.
image: ../assets/images/arduino_code.png
image_alt:
---

# Intro
This tutorial teaches you how to program your VizBlocks using Arduino. You will need the following items for this tutorial:

- A VizBlock
- A micro usb cable to connect the VizBlock to your computer
- A computer


# Getting Started
First off, we need to install some software and libraries, which we will use to program the VizBlock

## Install Arduino and Packages
1. Go to [this website](https://www.arduino.cc/en/software) and download the appropriate Arduino IDE for your operating system.
2. Open the downloaded file and follow the installation instructions (more detailed instructions [here](https://www.arduino.cc/en/Guide)).
3. Open the Arduino software and then open the preferences window (*Arduino>Preferences* on Mac OR *File>Preferences* on Windows).
4. In the preferences window enter `https://arduino.esp8266.com/stable/package_esp8266com_index.json` into the *Additional Boards Manager URLs* field. If there are already entries in this field then you can separate them with commas.
<img style="height: 400px" src="{{ "/assets/images/arduino_preferences.png" | prepend: site.baseurl }}" alt="Image showing the preferences window in the Arduino IDE." />
5. Open the Board Manager from *Tools>Board:>Boards Manager...* then enter `esp8266` in the search bar, and install the esp8266 package (see image below).
<img style="height: 400px" src="{{ "/assets/images/esp8266_package.png" | prepend: site.baseurl }}" alt="Image showing the package installation window in the Arduino IDE." />
6. Go to *Tools>Board:>ESP8266 Boards* and select **LOLIN(WEMOS) D1 R2 & mini**, as shown in the image below.
<img style="height: 400px" src="{{ "/assets/images/board_selection.png" | prepend: site.baseurl }}" alt="Image showing the board selection window in the Arduino IDE." />

## Install Required Libraries
1. In Arduino go to *Tools>Manage Libraries*
2. In the Library Manager, search for **adafruit neopixel** then click to install the Adafruit Neopixel library.
<img style="height: 400px" src="{{ "/assets/images/arduino_library.png" | prepend: site.baseurl }}" alt="Image showing the Library Manager in the Arduino IDE." />
3. In the Library Manager, search for **adafruit mqtt** then click to install the Adafruit MQTT library. If prompted to install missing dependencies, select *Install all*.

## Install the VizBlocks Framework
1. Download the VizBlocks Framework Library [here](https://git.ecdf.ed.ac.uk/design-informatics/vizblocks/vizblocksframework/-/archive/master/vizblocksframework-master.zip).
2. Unzip the file, then move the unzipped file `vizblocksframework-master` to your `Documents/Arduino/libraries` folder.
3. Quit and re-open the Arduino software.

## Check that Everything is Installed
1. In Arduino, go to *File>Examples>VizBlocks>BasicBlock*. This will open an example sketch.
2. Click the tick button (verify) in the top left of the Arduino window. It should say **Compiling sketch...** in the status bar below the code.
3. If the status eventually says **Done compiling** then everything is installed correctly and you're good to go! If not then you may be missing a required library. Check the error messages for clues, and check that you followed all of the steps above.

# Uploading Code to a VizBlock
You should now be ready to upload code to your VizBlocks. This gives you a lot of scope to customise what your blocks are capable of. We'll start by uploading a basic example sketch that includes the basic configuration and behaviours.

1. Open the BasicBlocks example sketch from *File>Examples>VizBlocks>BasicBlock*. Let's take a look at some important parts of this sketch.
2. The following lines are where we configure the basic settings for our block:
{% highlight C++ linenos %}
VizBlock block(
  "null",         // Our ID (default: null)
  "VizBlocks",    // Wifi Access Point (default: VizBlocks)
  "password",     // WiFi Password (change this to the password for your VizBlocks server)
  "192.168.4.1",  // IP address of Node RED server (default: 192.168.4.1)
  1883            // Port for Node RED server (default: 1883)
  );
{% endhighlight %}

... to be continued