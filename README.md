# gigatron_emulator
Emulator of Gigatron TTL Computer using SDL2

Found this nice and small SDL2 gigatron emulator (in directory emulator - main repo is FPGA implementation here):

https://github.com/hsnaves/gigatron

This is 99% coded by Humberto Silva Naves. MIT License - see file: LICENSE and header of main.c 
Nice and clean coding style!

Works excellent!

I just implemented loading of gt1 file by dropping file on window event.

Now one can simply drop a gt1 file on the emu window and it is loaded.
Before new gt1 file can be loaded, a reset is mandatory (Press PgUp until reset)!

arecibo64.gt1 is example file.

