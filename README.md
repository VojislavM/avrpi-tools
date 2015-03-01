AVRPi setup
===========

This setup script makes it easy to install everything you need to program AVR microcontrollers from a Raspberry Pi. It installs (or has options to install):

- Arduino IDE 1.0.1 (with patches for board and programmer)
- avrdude-6.1 (with linuxgpio support)
- avrpi (tool to interact easily with your ATmel microcontroller)
- Arduino-Makefile (because friends don't let friends use the Arduino IDE)
- wiringpi (Gordon's superduper handy tool to interact with the Raspberry Pi GPIO)

ATmega32U4 specific:

- LUFA (the library to use if you're serious about creating a USB Device out of your AVR)
- dfu-programmer (to use a USB enabled board standalone with a custom bootloader)

install
-------

To install the AVRPi setup tool:

	cd
	git clone https://github.com/onandoffables/avrpi-tools
	cd avrpi-tools
	./setup

setup
-----

After you run ./setup, a menu appears. Depending on the board selected, the menu changes a little. You have the option of changing the board.

	#######################################################################
	#                          avrpi-tools                                #
	#######################################################################
	
	  Install everything in 1 easy step:
	    e)    Arduino IDE + avrdude
	
	  First time - fuses and test:
	    s)    change to different board/chip
	    f)    set fuses for atmega32u4 on avrpi32u4
	    t)    make + upload test/blinky.hex
	
	  Custom install:
	    a)    apt-get all dependencies
	    p)    patch arduino
	    b)    install pre-compiled avrdude binary
	    c)    compile + install avrdude from source
	
	  Optional extra:
	    w)    install wiringPi
	    v)    install avrpi tool
	    d)    install dfu-programmer
	
	  Software and projects:
	    m)    install Arduino-Makefile
	    l)    install LUFA-AVRPI32U4
	
	    q)    quit
	
	Enter your choice:

You have the option of installing everything in 1 easy step. Choose 'e' for this. That patches the Arduino IDE and libraries and installs a pre-compiled version of avrdude. But you can also compile avrdude from source. This will only take a couple of minutes anyway.

Use the 'custom install' options to tweak the installation process. For example, if you only want to install linuxgpio-enabled avrdude without the Arduino IDE and library.
