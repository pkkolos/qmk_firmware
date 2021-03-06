# Singa


![Singa](https://i.imgur.com/VVO27Tr.jpg)


A short description of the keyboard/project


Keyboard Maintainer: [amnesia0287](https://github.com/amnesia0287)  
Hardware Supported: TGR-Elaine v1.0 PCB  
Hardware Availability: http://singakbd.com/


Make example for this keyboard (after setting up your build environment):

    make singa:default

Flashing

ps2avr(GB) boards use an atmega32a microcontroller and a different bootloader. It is not flashable using the regular QMK methods. 

Windows: 
1. Download [HIDBootFlash](http://vusb.wikidot.com/project:hidbootflash).
2. Place your keyboard into reset. 
3. Press the `Find Device` button and ensure that your keyboard is found.
4. Press the `Open .hex File` button and locate the `.hex` file you created.
5. Press the `Flash Device` button and wait for the process to complete. 

macOS:
1. Install homebrew by typing the following:   
    ```
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```
2. Install `crosspack-avr`.  
    ```
    brew cask install crosspack-avr
    ```
3. Install the following packages:
    ```
    brew install python
    brew install pyusb
    brew install --HEAD`https://raw.githubusercontent.com/robertgzr/homebrew-tap/master/bootloadhid.rb

4. Place your keyboard into reset. 
5. Flash the board by typing `bootloadHID -r` followed by the path to your `.hex` file. 


See [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) then the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information.
