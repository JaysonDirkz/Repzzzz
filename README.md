# Repzzzz (v1.0 - v1.1)

A four channel stereo looper.

## Specs

**Panel**
- Width: 6 hp<br>
- 2 Audio inputs
- 2 Audio outputs
- 1 Clock input
- 1 Clock output
- 1 Temp/div knob
- 4 Volume knobs
- 4 Arm/Rec pushbuttons with LEDs
- Sync mode switch

**Electrical**
- Current draw on +12V rail: 83mA to 104 mA
- Current draw on -12V rail: 6 mA
- Audio I/O are AC coupled
- Clock out: 0V to 10V

**Digital**
- Audio signal processing runs at 48 kHz and 32-bits
- Block size is 8
- Audio I/O are sampled at 48 kHz 24-bits
- Clock I/O and human controls are sampled at blockrate (48 / 8 => 6 kHz)
- Latency from audio input to audio output: ...
- Max loop length per loop: 30 seconds

## Manual

**Internal sync mode:**
- Tempo knob: 30 - 220 bpm, slightly logarithmic
- Clock output: 16th note pulses.

**External sync mode:**<br>
- Clock division kob sets the division for the clock output.
- Division range: x4 - x2 - 1 - /2 - /4

**Arming and Recording:**<br>
Record a loop using the pushbuttons.
1. First push: Arms this channel
    - LED blinks slow
    - Hearing audio input
2. Second push: Recording starts
    - LED blinks fast
3. Third push: Finishes recording
    - Mutes audio input
    - Recorded loop now hearable
    - LED intensity follows phase of the loop.

**Some facts**<br>
- The arm/recording buttons snap to the closest clock trigger of the output clock.
- You can cancel arming/recording at any time by pushing a button of another channel. This will keep the old recorded loop.
- Recording is not retained after power reset.
- Muting or deleting of the recorded loop is not implemented. Simply mute by turning down the volume knob. And you can always hear the audio input again by pushing a button.

**Settings menu:**<br>
Long hold the pushbutton of the first or second channel to go to the settings menu.
When all lights start rapidly blinking you are in the settings menu.

Here you can change several settings. These are not retained after power reset.

Channel 1:
  * Button: Turn quantize on or off.
  * Led: ON = quantize on, OFF = quantize off.

Channel 2: 
  * Not used.

Channel 3:
  * Button: When externally clocked, reset the output clock pulse on the current input clock pulse
  * Led: Output clock pulse.

Channel 4:
  * Button: not used.
  * Led: Input clock pulse (when externally clocked).

## Version info

Hardware v1.1: Pushbuttons with yellow LEDs<br>
Hardware v1: Pushbuttons with green LEDs
