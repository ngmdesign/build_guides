# Crkbd v3

Available at: https://keyhive.xyz/shop/corne-v3

Additional images at: https://imgur.com/a/p1oGbG0

1. Solder
   - [diodes](#solder-diodes)
   - [hot swap sockets](#solder-hot-swap-sockets)
1. [Flash controller](#flash-controller)
1. [Solder controller](#solder-controller)
1. [Solder the reset button](#Solder-reset-button)
1. [Test the keyboard](#test-the-keyboard)
1. Break PCBs from scaffold
1. Solder remaining components
   - [Underglow LEDs](#solder-underglow-leds)
   - [per-key LEDs](#solder-per-key-leds)
   - [OLEDs](#Solder-OLEDs)
   - [TRRS jacks](#Solder-TRRS-jacks)
1. [Remove from scaffolding](#Remove-from-scaffolding)
1. [Assemble into case](#Assemble-into-case)

## Solder diodes

Soldering diodes is relatively straightforward. Refer to [Soldering diodes](../basic/soldering-diodes.md) if you need further guidance.

## Solder Kailh hot swap sockets

Refer to [Soldering Kailh hot swap sockets](.../basic/soldering-diodes.md) if you need further guidance.

## Flash controller

Flash the controller (pro micro, Elite C, nice!nano, etc) with the firmware. This ensures that the controller works completely **before** soldering it permanently to the board.

The default crkbd firmware does not have LEDs enabled so if you plan on having LEDs this would be the time to modify the firmware to enable it.

## Solder controller

Refer to [Soldering the controller](../basic/soldering-the-controller.md) if you need further guidance.

## Solder reset button

Insert into holes. Solder in place on the bottom side of the pcb.

## Test the keyboard

At this point it should function as a keyboard. When you plug it in, the on-board LEDs should turn on. Insert a switch into a hot swap socket and [test that a keycode is pressed](https://www.keyboardtester.com/tester.html). You might consider testing every key in case there are problems with the diodes or hot swap sockets.

After this, solder remaining components.

## Solder underglow LEDs

> ⚠︎ LEDs can be very temperature sensitive. Be _very careful_. Consider setting your soldering to a low temp (about 200 C), using a fine tip, adding flux, and/or using a hot air station.

Tin all the pads with a small bubble of solder, not too much. Place the 5050 LED on top and center. With some light pressure, hold the led in place while you flow the solder bubbles. I use an aluminum screwdriver which also acts as a heat sink to protect the LED from burning out. Test each LED as you go.

### Troubleshooting

If an LED pixel does not turn on, there are a few points of failure to verify:

1. Are all 4 pads properly soldered?
   - Reflow the solder, careful when applying heat
   - Add more solder
1. Is the LED damaged?
   - Replace the LED
1. Is the PCB damaged?
   - Review the WS2812B wiring, and create a jump that completes the circuit per the schematic

## Solder per-key LEDs

> ⚠︎ LEDs can be very temperature sensitive. Be _very careful_. Consider setting your soldering to a low temp (about 200C), using a fine tip, adding flux, or using a hot air station.

Tin two pads on one side. Place the LED. Flow the solder on the tinned pads. Add solder to pads on other side. Test each LED as you go.

## Solder OLEDs

> If you've socketed the controller, also consider socketing the OLEDs else the controller will be trapped underneath it.

Insert into holes. Consider using electrical tape to secure in place while you solder the holes on the bottom side of the PCB.

> ⚠︎ The OLED is not required but **if you omit it, you must disable it in the firmware**. If you do not, you will experience "jittery" keystrokes as if some keys were lost while in transit. Disabling it in the firmware will fix this behavior.

## Solder TRRS jacks

Insert into holes. Solder in place on the bottom side of the pcb.

## Remove from scaffolding

The keyboard should be fully functional at this point. Remove the scaffolding around the PCBs by using pliers placed close to the drill holes and break.

## Assemble into case

At this point, you are ready to assemble the rest of the keyboard. These steps may include the following depending on the case you've chosen.

- Install OLED covers
- Remove protective paper on acrylic plates
- Install standoffs onto the switch plate
- Install the switches into plate and into the pcb
- Screw bottom plate
