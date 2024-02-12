LED Cube - Hardware
===================

_To be completed..._

Checkout the [main repository](https://github.com/francoisgeorgy/led-cube) to get more information about the LED Cube.

BOM
---

See [BOM.md](BOM.md).

Brackets and chassis design
---------------------------

There's an ongoing onShape design available [here](https://cad.onshape.com/documents/eb233c4f247d5269fe5ad74c/w/e5c8d36a0c3e44b3f1d693f6/e/4bf935a9030cdb6dc0eedcf4?renderMode=0&uiState=65ca1be860cfac3fed548dd4).

This design is not final and will evolve. The main change is that the main chassis (which houses the RPi and the batteries)
will no longer be fixed with screws but with magnets. 

Long term goal: 100% screw-free assembly, using magnets only.

3D print
--------

I printed everything with https://jlcpcb.com/

### Corner brackets : 

- STL : [LED-Cube-corner-bracket-v1.stl](3d-print%2FLED-Cube-corner-bracket-v1.stl).
- 3D Technology: MJF
- Material: PA12-HP Nylon
- Colors: -
- Surface Finish: Color :-Dyed Black

### Main chassis : 

- STL : [LED-Cube-base-support.stl](3d-print%2FLED-Cube-base-support.stl)
- 3D Technology: SLS
- Material: 3201PA-F Nylon
- Colors: Black
- Surface Finish: No

This chassis can not be used as-is. You'll have to cut the four corner brackets and fix the chassis with magnets instead of screws. 

I'm designing a new chassis. I will update this page as soon as it is ready.

Panels connections
------------------

![panels-chains.jpg](images%2Fpanels-chains.jpg)

The panels are connected as 2 chains or 3 panels. 

Each chain is connected to the Hub75 RGB interface. The third RGB interface connector is not used. 

Using only 2 of the 3 available Hub75 interface leave some GPIO free to be used for I2C sensors (accelerometer, etc.)

If we had used all 3 Hub75 chains, then there would be no GPIO signal available.

If, however, you wish to use the 3 available Hub75 channels, then there would always be the possibility of using the 
Raspberry Pi's USB ports to communicate with external sensors.

Power distribution
------------------

![power-distribution.jpg](images%2Fpower-distribution.jpg)


