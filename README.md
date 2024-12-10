# Magical Toys (magicaltoys.com) Charging PCB

This PCB is meant to be used in tandem with their talking stuffed dinosaur as a charging dock to make recharging the dino easier. It is meant to fit into the 3d printed housing in the 3d-files directory.

The PCB uses an op-amp and shunt resistor in series with the power connectors on the low side to detect when current is flowing through the trace. When a dino stuffed animal is placed on top of the dock, the barrel plug attached to the center connector supplies power to the stuffed animal. The dino charges at 5V at a nominal current of 1.8A. When 1.8A flows across the shunt resistor, it generates a voltage difference of about 0.2V. The op-amp takes in this voltage measurement and compares its difference to Ground at 0V. The op-amp is set to have a threshold of 0.15V. When a voltage greater than that is supplied, it outputs a logical HIGH and turns on the LED at the other end of the PCB. Hence, the LED is only illuminated when the dino is connected to the dock and charging. The LED automatically turns off when the dino is no longer charging or disconnected from the dock.

![Image-of-PCB](/rev1-pcb-pic.png)
