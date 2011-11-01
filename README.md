Hi!

Chances are that if you're here, you have an STM32 board that you are trying to get to work under linux. This git repo contains a template project that I use to build all my projects for the STM32F100 (128KB Flash, 8KB RAM). By default, this will build the demo application that comes with the STM32.

Getting it to work:

1.  Summon the arm toolchain ([look here](https://github.com/esden/summon-arm-toolchain))
2.  Clone this repo
3.  Run `make`
4.  Use your favourite tool to get the ELF onto the board (I use ST Visual Programmer in a windows VM, trying to get [stlink](https://github.com/texane/stlink) working, but it's pretty buggy for STLINKv1)

Using it for your own projects:

1.  Put your .c files in src
2.  Put your .h files in inc
3.  Edit the Makefile and change the `OBJS= ...` line at the top of the file
4.  Run `make`

`OBJS= ...` should contain each of your .c files but with .o extensions. So if you wanted to build the files main.c, party.c, cake.c your line would be:

`OBJS= main.o party.o cake.o`

Let me know if this is useful for you!

jeremy dot 006 att gmail dot com

