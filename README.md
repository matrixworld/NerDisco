NerDisco
========

Is a simple VJ tool leveraging Qts' QML/JavaScript libraries to provide live-editing functions and is meant to be connected to a [Boblight](https://code.google.com/p/boblight/)display of the ["Adalight"](http://www.adafruit.com/product/461) type via a serial port. It was tested with an Arduino Pro connected to an LEDstrip using [LPD8806 chips](http://www.adafruit.com/product/306). The code running on the Arduino was [Adalights' LPD8806 LEDstream sketch](https://github.com/adafruit/Adalight/blob/master/Arduino/LEDstream_LPD8806/LEDstream_LPD8806.pde). The code was compiled and tested on a Windows 7 and Ubuntu 14.04 machine and may or may not work on other systems.
It is in parts inspired by the live shader-editing tool [quint](https://gitorious.org/quint). So hats off to those guys...

Please note that the tool was rather quickly hacked together for a party and obviously needs some heavy refactoring and improvements. Planned features are some audio input facilities, so e.g. the music spectrum can be used in the scripts and MIDI controller input for the dials/triggers for better interaction.

License
========

[BSD-2-Clause](http://opensource.org/licenses/BSD-2-Clause), see [LICENSE.md](LICENSE.md).

Building
========
Atm a .pro file for Qt Creator / QMake is provided, so use that until CMake is working...

**Use CMake:**
<pre>
cd NerDisco
cmake .
make
</pre>

The Qt framework with version 5.3 or higher is required for GUI, audio and serial port functionality.
G++ 4.7 (for C++11) is needed to compile NerDisco. For installing G++ 4.7 see [here](http://lektiondestages.blogspot.de/2013/05/installing-and-switching-gccg-versions.html).

Overview
========
![GUI overview](NerDisco_gui.png?raw=true)  

FAQ
========
**Q:** I'm on linux and I can not access the serial port somehow...  
**A:** You might need to add your USERNAME to the dialout group: ```sudo usermod -a -G dialout USERNAME```.  

I found a bug or have a suggestion
========

The best way to report a bug or suggest something is to post an issue on GitHub. Try to make it simple, but descriptive and add ALL the information needed to REPRODUCE the bug. **"Does not work" is not enough!** If you can not compile, please state your system, compiler version, etc! You can also contact me via email if you want to.
